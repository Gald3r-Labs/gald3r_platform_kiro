<p align="center">
  <img src="logo/Gald3r_Logo_Big.jpg" alt="Gald3r" width="400" />
</p>

<h1 align="center">Gald3r for Kiro</h1>

<p align="center">
  The <strong>Kiro edition</strong> of Gald3r -- file-based memory, task management, and
  agent orchestration that runs <strong>inside Kiro</strong>. Part of the Gald3r framework
  for 34 AI coding tools.
</p>

<p align="center">
  <a href="https://www.gald3r.ai">www.gald3r.ai</a> |
  <a href="https://github.com/wrm3/gald3r">All 34 tools</a> |
  <a href="CHANGELOG.md">Changelog</a> |
  <a href="CONTRIBUTING.md">Contributing</a>
</p>

---

## What is Gald3r?

Gald3r is a framework that runs **inside your AI coding tool** -- not alongside it. Drop the
template into your project root and your AI assistant gains:

- **Persistent memory** across sessions (tasks, bugs, plans, constraints)
- **13 specialized agents**, **110 skills**, **179 commands** (`@g-status`, `@g-go`, `@g-medic`)
- **27 hooks** on IDE events, **14 rules** that keep agents disciplined

Everything is plain markdown in your repo. No server, no database, no Docker required.

---

## What's in this repo

This is the **Kiro distribution** of Gald3r. The [`kiro/`](./kiro/) folder is a
complete, ready-to-deploy gald3r setup tuned for Kiro -- drop its contents into your
project and your assistant gains persistent memory, agents, skills, commands, and hooks.

> **Using a different tool?** Gald3r supports 34 AI coding tools. Find yours at the main repo:
> **[github.com/wrm3/gald3r](https://github.com/wrm3/gald3r)**.

---

## Install

**New project** -> [instructions_new_project.md](./instructions_new_project.md)
**Existing project** -> [instructions_existing_project.md](./instructions_existing_project.md)

**TL;DR -- copy the payload into your project root:**

```bash
git clone https://github.com/wrm3/gald3r_platform_kiro.git
cp -r gald3r_platform_kiro/kiro/. /path/to/your/project/
```

Then open the project in Kiro and type `@g-status` to confirm gald3r loaded.

> The `kiro/` payload is **additive** -- it drops in gald3r's config + `.gald3r/` state and
> does not touch your source. Your project keeps **its own** LICENSE and docs; the license in
> *this* repo covers the gald3r framework itself.

---

## What's Inside

| Component | Count | Reference |
|---|---|---|
| Agents | 13 | [wiki / Agents](https://github.com/wrm3/gald3r/wiki/Agents) |
| Commands | 179 | [wiki / Commands](https://github.com/wrm3/gald3r/wiki/Commands) |
| Skills | 110 | [wiki / Skills](https://github.com/wrm3/gald3r/wiki/Skills) |
| Rules | 14 | [wiki / Rules](https://github.com/wrm3/gald3r/wiki/Rules) |
| Hooks | 27 | [wiki / Hooks](https://github.com/wrm3/gald3r/wiki/Hooks) |
| Task system | -- | File-based `.gald3r/` for tasks, bugs, plans, constraints |

Complete, always-current catalogs live on the **[Gald3r Wiki](https://github.com/wrm3/gald3r/wiki)**.
New here? Start with the **[Quickstart](https://github.com/wrm3/gald3r/wiki/Quickstart)**.

---

## The .gald3r/ Folder

Everything gald3r remembers lives in one `.gald3r/` folder in your repo -- plain markdown and
YAML, fully diffable, fully yours: tasks, bugs, plans, constraints, subsystems, features,
ideas, learned facts, release notes, and audit logs.

---

## Releases

See [releases/](./releases/) and [CHANGELOG.md](./CHANGELOG.md). Latest: **v1.9.0** --
[releases/RELEASE_v1.9.0.md](./releases/RELEASE_v1.9.0.md).

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).

---

*Built with gald3r. Runs on gald3r.*
