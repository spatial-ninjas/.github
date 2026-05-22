<p align="center">
  <img src="https://raw.githubusercontent.com/spatial-ninjas/.github/95099f7cb65705f48a7186c69a1f2b05d5c1214c/profile/space-ninja-logo.svg" height="200" alt="Space ninja logo">
</p>

<h1 align="center">LLM Spatial Reasoning: Evaluating and Enhancing Geographic Cognition in Language Models</h1>

<p align="center">
  <a href="https://github.com/orgs/spatial-ninjas/projects/1">
    📋 Project Board
  </a>
  |
  <a href="https://github.com/spatial-ninjas/research">research</a>
  |
  <a href="https://github.com/spatial-ninjas/llm-compare-dashboard">llm-compare-dashboard</a>
</p>

## Overview

This organization hosts the repositories for the project **LLM Spatial Reasoning: Evaluating and Enhancing Geographic Cognition in Language Models**.

The broad research theme is whether large language models can reason about real-world geography. This includes directions, distances, topology, map interpretation, place knowledge, and multi-step spatial reasoning.

For the implemented project, we narrowed the scope to a more controlled task: **street-network route finding over an OpenStreetMap-derived Southern Helsinki graph**. The models are given a compact graph-like representation called SSAL, and their generated routes are compared against Dijkstra ground truth computed from the same SSAL-derived graph.

The project focuses on:

- comparing OpenAI and Gemini model families on selected routing tasks
- testing real-world street routing with controlled origin-destination pairs
- evaluating structured-output correctness, path validity, shortest-path agreement, and distance errors
- analyzing failure modes such as invalid JSON, unknown nodes, missing directed edges, non-shortest valid paths, and one-way-street mistakes
- experimenting with prompt templates and SSAL profiles


## Repositories

The project is split into two main repositories.

| Repository | Purpose |
|---|---|
| [`spatial-ninjas/research`](https://github.com/spatial-ninjas/research) | Reusable SSAL conversion, graph utilities, network loading, Dijkstra baseline, route-response evaluation, cleaned route-evaluation data, and supporting analysis material |
| [`spatial-ninjas/llm-compare-dashboard`](https://github.com/spatial-ninjas/llm-compare-dashboard) | Streamlit dashboard for running OpenAI/Gemini prompt comparisons, route-finding experiments, persisted history, route-evaluation history, and result export |

In the final workflow, the dashboard is used to run prompts and export route history. The `research` repository provides the shared evaluator and contains the cleaned public route-evaluation dataset.

## Project Timeline

| Date | Event | Notes |
|---|---|---|
| Fri, 6.3 | Project kickoff | Initial broad GeoAI / LLM spatial-reasoning scope |
| Tue, 10.3 | 1st sprint planning | Project board and early backlog setup |
| Fri, 20.3 | 1st sprint review | Early literature review and prototype direction |
| Fri, 10.4 | 2nd sprint review | Route-evaluation direction became more concrete |
| Fri, 23.4 | Project midterm seminar | Midterm demonstration and scope refinement |
| Fri, 8.5 | 4th sprint review | Dashboard, evaluation history, and SSAL workflow matured |
| Fri, 22.5 | Project delivery | Final report, presentation, cleaned data, and reproducible materials |


## Current Workflow

```text
GeoPackage
   ↓
SSAL text
   ↓
SSAL-derived graph
   ↓
Dijkstra ground truth
   ↓
OpenAI / Gemini route-generation prompt
   ↓
route-response evaluator
   ↓
dashboard history + cleaned public summaries
```

The core evaluation compares a model-produced node sequence against the SSAL-derived graph. A result can fail because the API call failed, the response was not valid JSON, the route used unknown nodes, the route used missing or wrong directed edges, or the route was valid but not the shortest path.

## Public Route-Evaluation Data

The cleaned route-evaluation data is available in:

```text
spatial-ninjas/research/data/route-evaluation/
```

The folder contains:

- `relevant_route_history_cleaned.json` — cleaned per-run evaluation data with raw provider responses and unnecessary internal metadata removed
- `route_case_config_evaluation_summary.csv` — tabular summary grouped by route case, model/API configuration, prompt template, and SSAL profile
- `route_case_config_evaluation_summary.md` — human-readable GitHub summary of the same grouped results

The route cases are grouped into five categories:

1. Direct routes
2. Long multi-hop routes
3. Junction-heavy routes
4. Near shortest alternatives
5. Routes where the shortest alternative is affected by a one-way street

The summary uses `indices_base0_ranges`, meaning the indices refer to positions in the cleaned JSON using Python/JSON base-0 indexing.

## Getting Started for New Contributors

If you are joining or reviewing the project, start from the two main repositories.

1. **Read the `research` repository README**

   This explains the SSAL representation, graph construction, Dijkstra baseline, route-response evaluator, offline history evaluation, and cleaned route-evaluation data.

2. **Read the `llm-compare-dashboard` repository README**

   This explains how prompts are run against OpenAI and Gemini models, how route tasks are created, and how evaluation history is stored and exported.

3. **Inspect the cleaned route-evaluation data**

   The public data under `research/data/route-evaluation/` is the best starting point for understanding the final experiment results.

4. **Use the GitHub Project board for historical context**

   The project board is available here:  
   **https://github.com/orgs/spatial-ninjas/projects/1**

   It contains the backlog and sprint history used during the course project.

5. **Document any follow-up work**

   Future experiments should record the route cases, prompt templates, SSAL profile, model/API configuration, and evaluation outputs so that results remain reproducible.


## Research Questions

1. What benchmarks and evaluation frameworks exist for assessing LLM spatial cognition and geographic reasoning (e.g. GeoLLM, spatial cognition benchmarks, GIS exam evaluations)? What dimensions of spatial reasoning do they measure?

2. How do different LLMs (GPT-4o, Claude, Gemini, Llama, Qwen, DeepSeek) perform on spatial reasoning tasks such as distance estimation, direction inference, topological relationships, route description, and map-based question answering? Design and run a comparative evaluation.

3. What are the most common failure modes in LLM spatial reasoning? Are failures related to lack of geographic knowledge, inability to perform spatial computation, hallucination of spatial facts, or something else?

4. What strategies can improve LLM spatial reasoning (e.g. augmenting prompts with OSM data as in GeoLLM, chain-of-thought spatial reasoning, Visualization-of-Thought, coupling LLMs with external spatial computation tools)? Implement and test at least one enhancement strategy.


## Project Management

Project management is handled via the [GitHub Project board](https://github.com/orgs/spatial-ninjas/projects/1) associated with this organization, organized into two task collections:

- **Master backlog**: the complete list of known tasks, ideas, and research directions.
- **Sprint backlog**: the subset of tasks selected for the current sprint.

At the start of each sprint, tasks are pulled from the master backlog into the sprint backlog. Progress is tracked and updated on the board throughout the sprint.

The board is the primary tool for sprint planning, task tracking, and progress visibility.


## Project Log

Meeting notes, sprint logs, and project timekeeping are maintained in the shared project log document:

📄 [Project log Google Doc](https://docs.google.com/document/d/11h-INtL7AyNGRWCvQHuht3CC9ALObqWDDY3mYXxbeNA/edit?usp=sharing)

Each entry contains:

- Date
- Participants
- Topics discussed
- Decisions made
- Planned next steps

Sprint reviews and other key milestones are recorded there instead of in the repositories.


## Course Deliverables

This project constitutes **50% of the course grade** and requires the following deliverables.

**Project Report**: A final report covering research background, evaluation methodology, experimental results, analysis of spatial reasoning failures, and enhancement experiments.

**Project Materials**: All resources needed to reproduce and reuse results: source code, datasets or prompts, evaluation scripts, and experiment outputs.

**Presentations**: A mid-term seminar demo and a final project presentation.

**[Timekeeping](https://docs.google.com/spreadsheets/d/1BJou-bTwQKUmrbxb6oVhIHar71k-xp9bX-a6NKKsn0U/)**: Each team member must log time with **30-minute precision**, e.g.:

```
2026-03-03  Literature review         1.5 h
2026-03-04  Benchmark implementation  2.0 h
```

Any project-related expenses should be itemized in a separate expenses report.


## Expected Outcomes

The final project outcome is a route-finding evaluation workflow for comparing LLM-generated routes against SSAL-derived Dijkstra ground truth.

The project materials include:

- a reusable SSAL/graph/evaluation package
- a dashboard for running model comparisons and inspecting history
- selected Southern Helsinki route cases
- cleaned public route-evaluation data
- grouped summaries by route case, model/API configuration, prompt template, and SSAL profile
- a final report and presentation discussing the results and observed failure modes


## Accessing Papers via Aalto Library Proxy

Some of the references listed below are behind publisher paywalls. If you are outside the Aalto University network, you can access them through the **Aalto Library proxy server (libproxy)**.

To do this, prepend the following prefix to the paper URL:

```
http://libproxy.aalto.fi/login?url=
```

After opening the modified link, you will be prompted to log in using your Aalto credentials.

Example:

Original link:

```
https://ieeexplore.ieee.org/abstract/document/5481374
```

Access through the Aalto proxy:

```
http://libproxy.aalto.fi/login?url=https://ieeexplore.ieee.org/abstract/document/5481374
```


## Key References and Tools

| Reference | Focus |
|---|---|
| [Manvi et al. (2024), *GeoLLM: Extracting Geospatial Knowledge from Large Language Models*](https://arxiv.org/abs/2310.06213) | Extracting geospatial knowledge from LLMs using OpenStreetMap data |
| [Yang et al. (2025), *Evaluating and Enhancing Spatial Cognition Abilities of Large Language Models*](https://doi.org/10.1080/13658816.2025.2490701), *International Journal of Geographical Information Science* | Framework for evaluating spatial cognition in LLMs |
| [Wu et al. (2024), *Mind’s Eye of LLMs: Visualization-of-Thought Elicits Spatial Reasoning in Large Language Models*](https://proceedings.neurips.cc/paper_files/paper/2024/file/a45296e83b19f656392e0130d9e53cb1-Paper-Conference.pdf), *NeurIPS* | Visualization-of-Thought prompting for spatial reasoning |
| [Wang et al. (2026), *LLM-GeoTextCog: A Cognitive Enhancement Framework for Geospatial Scene Understanding in Geographic Texts Using Large Language Models*](https://doi.org/10.1111/tgis.70203), *Transactions in GIS* | Cognitive enhancement framework for geographic text understanding |
| [Mooney et al. (2023), *Towards Understanding the Geospatial Skills of ChatGPT: Taking a Geographic Information Systems (GIS) Exam*](https://doi.org/10.1145/3615886.3627745), *ACM SIGSPATIAL GeoAI Workshop* | Evaluating LLMs using a GIS exam |
| [Xu et al. (2025), *Evaluating Large Language Models on Geospatial Tasks: A Multiple Geospatial Task Benchmarking Study*](https://doi.org/10.1080/17538947.2025.2480268), *International Journal of Digital Earth* | Multi-task benchmark for geospatial reasoning |

