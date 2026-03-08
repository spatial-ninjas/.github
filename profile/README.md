<p align="center">
  <img src="https://raw.githubusercontent.com/spatial-ninjas/.github/95099f7cb65705f48a7186c69a1f2b05d5c1214c/profile/space-ninja-logo.svg" height="200" alt="Space ninja logo">
</p>

<h1 align="center">LLM Spatial Reasoning: Evaluating and Enhancing Geographic Cognition in Language Models</h1>

<p align="center">
  <a href="https://github.com/orgs/spatial-ninjas/projects/1">
    📋 Project Board
  </a>
</p>

## Overview

This organization hosts the repositories for the project **LLM Spatial Reasoning: Evaluating and Enhancing Geographic Cognition in Language Models**.

A core question in GeoAI is whether LLMs have developed genuine spatial cognition: the ability to reason about distances, directions, spatial relationships, topological configurations, and geographic context. While LLMs demonstrably encode rich geospatial knowledge, they frequently struggle with tasks requiring contextual deduction, spatial inference, and multi-step geographic reasoning.

This project systematically evaluates the spatial reasoning capabilities of modern LLMs, identifies common failure modes, and explores strategies to enhance geographic cognition.

The repositories in this organization provide the workspace for:
- Project coordination
- Experiment code and evaluation scripts
- Research notes and documentation
- Project log and course deliverables


## Getting Started for New Contributors

If you are joining the project, the following steps will help you get oriented.

1. **Read the project overview and research questions**

   Familiarize yourself with the goals of the project and the key research questions described in this document.

2. **Check the GitHub Project board**

   The project board is available here:  
   **https://github.com/orgs/spatial-ninjas/projects/1**

   The GitHub Project board contains the **master backlog** and the **current sprint backlog**.  
   The master backlog is the main place for collecting tasks, ideas, and possible research directions.

3. **Add proposed work to the master backlog**

   If you have an idea for a task, experiment, literature review item, or implementation effort, add it to the **master backlog** so that it is visible to the team before sprint planning.

4. **Discuss task selection during sprint planning**

   Tasks for the next sprint are selected from the **master backlog** during sprint planning.  
   This is where the team decides what is most relevant and feasible for the upcoming sprint.

5. **Work in the appropriate repository after task selection**

   Depending on the task, work may involve:

   - implementing experiments
   - running model evaluations
   - collecting or preparing datasets
   - writing documentation or literature summaries

6. **Document your work**

   Important steps, results, and decisions should be documented so that experiments remain reproducible and other team members can follow the progress.

7. **Log time and meetings**

   Maintain personal timekeeping with **30-minute precision** and ensure that project meetings are recorded in the **project log**.


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

The board is the primary tool for sprint planning, task tracking, and progress visibility. Repository structure and development workflow will be finalized at the **first sprint planning meeting**.


## Project Log

The course requires a **project log** documenting the development process. Each meeting entry should include:

- Date
- Participants
- Topics discussed
- Decisions made
- Planned next steps

Sprint reviews and other key milestones should also be recorded here.


## Course Deliverables

This project constitutes **50% of the course grade** and requires the following deliverables.

**Project Report**: A final report covering research background, evaluation methodology, experimental results, analysis of spatial reasoning failures, and enhancement experiments.

**Project Materials**: All resources needed to reproduce and reuse results: source code, datasets or prompts, evaluation scripts, and experiment outputs.

**Presentations**: A mid-term seminar demo and a final project presentation.

**Timekeeping**: Each team member must log time with **30-minute precision**, e.g.:

```
2026-03-03  Literature review         1.5 h
2026-03-04  Benchmark implementation  2.0 h
```

Any project-related expenses should be itemized in a separate expenses report.


## Expected Outcomes

A report presenting a structured evaluation of LLM spatial reasoning capabilities across multiple models and task types, with a taxonomy of failure modes. If possible, an experimental demonstration of at least one technique that improves spatial reasoning performance (e.g. OSM-augmented prompting, tool-augmented spatial computation).


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

