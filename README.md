# Organization Infrastructure (`.github`)

This repository contains the organization-level configuration and public profile assets for the **Spatial Ninjas** GitHub organization.

Unlike the project repositories, this repository is not used for experiment code, datasets, model runs, or route-evaluation logic. Its main purpose is to maintain the organization homepage shown on GitHub.

## Repository Structure

```text
.github/
└── profile/
    ├── README.md
    └── space-ninja-logo.svg
```

## `profile/`

Files inside `profile/` define the organization profile page shown on GitHub.

`profile/README.md` is automatically rendered as the organization landing page:

https://github.com/spatial-ninjas

It contains:

- project overview
- repository links
- current route-finding evaluation scope
- high-level workflow
- public route-evaluation data pointers
- project timeline
- research questions
- key references

The file `space-ninja-logo.svg` is the vector logo used in the organization profile.

## Project Log

The project log is **not stored in this repository**.

Meeting notes, sprint logs, and timekeeping are maintained in the shared Google Docs project log:

https://docs.google.com/document/d/11h-INtL7AyNGRWCvQHuht3CC9ALObqWDDY3mYXxbeNA/edit?usp=sharing

This repository should not duplicate the project log unless a static archive is intentionally added later.

## Related Project Repositories

The main project work is split across two repositories:

- [`spatial-ninjas/research`](https://github.com/spatial-ninjas/research) — reusable SSAL conversion, graph utilities, network loading, route evaluation, cleaned route-evaluation data, and analysis materials
- [`spatial-ninjas/llm-compare-dashboard`](https://github.com/spatial-ninjas/llm-compare-dashboard) — Streamlit dashboard for running OpenAI/Gemini prompt comparisons, storing route-evaluation history, and exporting results

## Related Resources

**Organization profile**

https://github.com/spatial-ninjas

**Project board**

https://github.com/orgs/spatial-ninjas/projects/1

The project board was used for:

- master backlog
- sprint backlog
- task tracking during the course project

**Project log**

https://docs.google.com/document/d/11h-INtL7AyNGRWCvQHuht3CC9ALObqWDDY3mYXxbeNA/edit?usp=sharing

## Purpose of This Repository

This repository exists to keep **organization-level GitHub assets** in one small, focused place.

Specifically, it provides:

- the public GitHub organization profile
- the organization logo used by the profile README
- lightweight organization-level documentation

Experiment code, datasets, cleaned evaluation results, reports, and reusable utilities belong in the project repositories, especially `research` and `llm-compare-dashboard`.

## Notes

- Changes to `profile/README.md` immediately update the **organization homepage**.
- The official project log is maintained in the shared Google Docs document, not in this repository.
- This repository should remain **small and documentation-focused**.
