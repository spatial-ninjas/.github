# Sprint 1 Planning Meeting Notes

**Project:** LLM Spatial Reasoning: Evaluating and Enhancing Geographic Cognition in Language Models
**Team:** Spatial Ninjas
**Date:** Tue, 10.3.2026 12:00-13:15
**Place:** Room 1004, Ekonominaukio 1 (School of Business)
**Meeting type:** Sprint 1 Planning
**Participants:** Ki Chun, Oliver, Pawel, Topi, Totti, Eemil
**Facilitator:** Ki Chun (Scrum Master)


# 1. Purpose of the Meeting

The purpose of the session was to:

* introduce the team and project topic
* confirm the project workflow and sprint structure
* clarify team roles and responsibilities
* review the GitHub organization and project board setup
* discuss repository and documentation practices
* review the master backlog
* select and refine the Sprint 1 backlog
* assign literature review responsibilities


# 2. Team Introductions

The meeting began with a short round of introductions.

* **Ki Chun** introduced himself as mainly focused on the technical side. He currently acts as **Scrum Master** for Sprint 1 and will also contribute to implementation later in the project.
* **Oliver** introduced himself as mainly technically oriented and already somewhat familiar with the project topic.
* **Pawel** introduced his background in **GIS and Python development**, noting that he is less familiar with artificial intelligence but interested in learning about GeoAI and prompt engineering.
* **Topi** mentioned he had missed the previous meeting and was catching up with the project.
* **Totti** introduced himself as a **surveying engineer** and is acting as the **Product Owner** for this sprint.
* **Eemil** introduced himself as a **geoinformatics master's student** with some coding experience.


# 3. Project Overview

The team confirmed that the project focuses on evaluating and improving the **spatial reasoning abilities of large language models**.

The main objective is to understand:

* whether modern LLMs possess meaningful spatial reasoning abilities
* how these abilities can be evaluated systematically
* what kinds of failures occur when LLMs attempt spatial reasoning
* whether prompting strategies or tool integrations can improve spatial reasoning performance

The four research questions listed in the project description form the overall scope of the project.


# 4. Sprint 1 Goal

The goal of Sprint 1 is to **build a shared understanding of the current research landscape on LLM spatial reasoning and establish the foundation for later experimental work**.

During this sprint, the team will:

* review and summarize key research papers related to LLM spatial reasoning and GeoAI
* identify existing **benchmarks and evaluation approaches** used in prior work
* clarify the **project scope and research questions**
* establish **team practices** for documentation, backlog management, and communication
* identify candidate **LLM APIs, tools, and frameworks** that may be used in later implementation and evaluation phases

The expected outcome of the sprint is a **clear overview of existing methods and tools**, along with initial technical directions for implementing the evaluation experiments in later sprints.


# 5. Project Workflow and Management Approach

The project will follow a **sprint-based workflow**.

The main structure is:

* **Master Backlog**
  Contains all known tasks, research directions, and ideas across the whole project.

* **Sprint Backlog**
  Contains the subset of tasks selected for the current sprint.

At the beginning of each sprint, tasks are moved from the master backlog into the sprint backlog during the sprint planning meeting.

Once a sprint begins:

* tasks should generally not be added to the sprint backlog
* it is acceptable to slightly over-plan work rather than under-plan
* progress will be tracked on the GitHub project board

The team also agreed that **any member can add tasks to the master backlog** when new ideas or research directions arise.


# 6. Roles and Responsibilities

For Sprint 1 the roles are:

* **Scrum Master:** Ki Chun
* **Product Owner:** Totti

Additional development roles discussed:

**Senior Developer**

* responsible for higher-level technical decisions
* helps guide experiment design and architecture

**Developer**

* contributes to evaluation design
* writes code and performs experiments
* analyzes results

**Junior Developer**

* assists with implementation
* helps prepare datasets
* contributes to documentation and pipelines

The team agreed that:

* these roles are mainly used to clarify responsibilities
* roles do **not need to be rigid**
* roles will **rotate between sprints**
* no member should stay in the same role throughout the whole project


# 7. GitHub Organization and Project Board

Ki Chun presented the **Spatial Ninjas GitHub organization** and the project board.

The organization already includes:

* project overview
* project timeline
* onboarding instructions
* research questions
* project management description
* project log instructions
* course deliverables
* key references
* instructions for accessing papers via the **Aalto library proxy**

The [GitHub Project board](https://github.com/orgs/spatial-ninjas/projects/1) will be used for:

* sprint planning
* backlog management
* tracking progress
* organizing research tasks

Some additional setup was required to ensure all members have the correct permissions to:

* access the organization
* edit the project board
* create and modify issues


# 8. Project Timeline

The team reviewed the planned timeline.

Important dates include:

| Date     | Event                        |
| -------- | ---------------------------- |
| Fri 13.3 | Support session (obligatory) |
| Fri 20.3 | Sprint 1 review              |
| Fri 27.3 | Optional support session     |
| Fri 10.4 | Sprint 2 review              |
| Fri 23.4 | Midterm seminar              |
| Fri 22.5 | Final project delivery       |

Sprint lengths are roughly **two weeks**, although adjustments may occur depending on progress.


# 9. Communication

The team agreed that:

* **Telegram** will be used for team communication
* GitHub will be used for task management and documentation
* meetings will typically be aligned with existing course sessions when possible

Sprint review and next sprint planning may either be separate meetings or combined depending on scheduling needs.


# 10. Repository Structure and Documentation

The team discussed how to organize research notes and documentation.

Key points:

* early in the project, documentation can remain lightweight
* research findings may be written directly in GitHub issues
* text-based documentation inside the repository is preferred over isolated files

However, the team recognized that knowledge could become scattered across many issues.

Therefore the team agreed that:

* during the sprint, notes can be written in issues
* at the **end of the sprint**, results should be consolidated into a structured document

This aligns with the backlog item **Define documentation practices**.


# 11. Sprint 1 Focus

Sprint 1 primarily focuses on:

* reading research papers
* understanding existing benchmarks
* identifying evaluation methods
* clarifying project structure and scope
* preparing the technical direction for later sprints

Heavy coding work is **not expected in Sprint 1**.

However, some groundwork should begin regarding:

* LLM APIs
* programming frameworks
* evaluation pipelines
* benchmark design approaches


# 12. Backlog Review

The team reviewed the current backlog and confirmed that the following tasks belong to **Sprint 1**.

### Administrative and setup tasks

* Set up team communication
* Define documentation practices
* Define backlog management practices
* Decide initial project schedule and scope
* Familiarize with the project topic
* Extract tasks from the project description
* RQ0: Initial administrative questions

### Research tasks

* Read the research papers
* RQ1: Existing benchmarks for spatial reasoning
* Identify benchmarks used in prior work

### Technical exploration tasks

* Identify possible LLM APIs
* Identify programming languages and frameworks
* Identify evaluation and benchmarking tools


# 13. Definition of Done

For literature review tasks, the team agreed that a task is considered **done** when the reader can summarize:

* the research problem addressed in the paper
* the methodology used
* the evaluation benchmark or dataset
* the tools or models used
* the key results and conclusions
* how the paper relates to the project


# 14. Programming Language Decision

During the discussion the team agreed that:

**Python will be the primary programming language for the project.**

The decision was motivated by:

* compatibility with LLM APIs
* availability of evaluation tools
* GIS libraries and tooling
* team familiarity


# 15. Discussion of Possible Implementation Direction

Although Sprint 1 focuses on literature review, the team discussed potential future approaches for experiments.

Ideas included:

* generating prompts automatically rather than manually
* using structured formats such as **JSON** to store prompt templates
* writing **Python scripts** to evaluate model responses
* generating ground-truth answers programmatically
* using GIS tools (e.g., routing algorithms) to compute correct answers
* validating automated evaluations with a small manually verified sample

These discussions will influence later tasks such as:

* designing evaluation benchmarks
* implementing automated evaluation pipelines


# 16. Literature Reading Strategy

The team agreed that:

* everyone should read **all papers at a general level**
* each team member will focus on **one primary paper**

This allows each member to develop deeper expertise while maintaining shared project understanding.


# 17. Paper Assignments

Based on the project board:

| Member  | Paper                 |
| ------- | --------------------- |
| Pawel   | Manvi et al. (GeoLLM) |
| Oliver  | Yang et al.           |
| Ki Chun | Wu et al.             |
| Topi    | Wang et al.           |
| Totti   | Mooney et al.         |
| Eemil   | Xu et al.             |

Each member will summarize their assigned paper and contribute findings to the literature overview.


# 18. Timekeeping and Project Log

The course requires:

* **individual time tracking with 30-minute precision**
* documentation of project meetings
* tracking of any project expenses

Each team member will maintain their own time log.

Meeting notes will be recorded as part of the **project log**.


# 19. Key Decisions

* Sprint 1 focuses on **literature review and project setup**
* **Ki Chun** acts as Scrum Master for Sprint 1
* **Totti** acts as Product Owner for Sprint 1
* roles will rotate between sprints
* **Telegram** will be the primary communication channel
* the **GitHub project board** is the main task management tool
* **Python** will be the primary programming language
* each member reads all papers but focuses on one
* research findings can be documented in issues during the sprint
* results should be consolidated into a shared document at the end of the sprint


# 20. Action Items

### Ki Chun

* finalize GitHub organization membership
* configure project board permissions
* maintain meeting notes and project log

### All Team Members

* read assigned research papers
* skim the remaining papers
* document findings in GitHub issues
* track personal project time

### Team

* identify benchmarks used in prior work
* identify candidate LLM APIs
* identify programming tools and frameworks
* identify evaluation and benchmarking tools


# 21. Closing

The meeting concluded with agreement on the Sprint 1 scope and task assignments.

The team will spend the sprint building a shared understanding of the research field and preparing the technical foundations for later experimental evaluation of LLM spatial reasoning capabilities.
