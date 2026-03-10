# Organization Infrastructure (.github)

This repository contains the organization-level configuration and documentation for the **Spatial Ninjas** GitHub organization.

Unlike the project repositories, this repository is not used for experiments or code. Instead, it provides the infrastructure that supports the organization's public profile and project coordination.


## Repository Structure

```
.github/
├── profile/
│   ├── README.md
│   └── space-ninja-logo.svg
└── project-log/
    └── 2026-03-10-sprint1-planning.md
```

### `profile/`

Files inside `profile/` define the organization profile page shown on GitHub.

`profile/README.md` is automatically rendered as the organization landing page:

https://github.com/spatial-ninjas

It contains:

- project overview
- research questions
- timeline
- contributor onboarding information
- key references

The file `space-ninja-logo.svg` is the vector logo used in the organization profile.


### `project-log/`

The `project-log` directory contains meeting notes and sprint documentation for the project.

Entries typically include:

- date of meeting
- participants
- topics discussed
- decisions made
- next steps

This log serves as the official record of project progress and decisions.


## Purpose of This Repository

This repository exists to keep **organization-level assets and coordination artifacts** in a single place.

Specifically, it provides:

- the **GitHub organization profile**
- the **project meeting log**
- shared documentation relevant to the whole organization

Keeping these files here avoids mixing organization infrastructure with experiment code or datasets.


## Related Resources

**Organization profile**

https://github.com/spatial-ninjas

**Project board**

https://github.com/orgs/spatial-ninjas/projects/1

The project board is used for:

- master backlog
- sprint backlog
- task tracking during sprints


## Notes

- Changes to `profile/README.md` will immediately update the **organization homepage**.
- All major meetings (sprint planning, reviews, seminars) should be recorded in `project-log/`.
- This repository should remain **small and documentation-focused**.
