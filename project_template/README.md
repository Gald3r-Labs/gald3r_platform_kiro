# {project_name}

This project runs on **[Gald3r](https://github.com/wrm3/gald3r) for Kiro** -- file-based
memory, task management, and agent orchestration that lives inside your editor. All project
state (tasks, bugs, plans, constraints) is plain markdown under `.gald3r/`.

## Getting started

Open this project in **Kiro** and run **`@g-setup`** -- it initializes gald3r and fills in
this project's identity.

## Where things live

| Path | What |
|---|---|
| `AGENTS.md` | Universal instructions -- the source of truth for agent behavior |
| `.gald3r/` | Project memory: tasks, bugs, plans, constraints, subsystems |

## Common commands

`@g-status` - `@g-go` (run the task pipeline) - `@g-task-new` - `@g-bug-report` - `@g-medic`.
Full catalog on the [Gald3r Wiki](https://github.com/wrm3/gald3r/wiki/Commands).

---
*Replace this README with your own as your project grows. Powered by gald3r v1.9.0.*
