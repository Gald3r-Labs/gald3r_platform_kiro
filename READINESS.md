# gald3r Readiness Report — Kiro (Amazon)

> An honest accounting of how much of the gald3r framework installs natively on this
> platform, what degrades to an approximation, and what has no native home yet.
> Generated from a live documentation crawl on 2026-06-02.

**Overall readiness: ✅ Full.** Kiro ships as an agentic IDE (VS Code-based) and a Kiro
CLI, sharing config under `.kiro/` (workspace) and `~/.kiro/` (global). Every gald3r layer —
commands, rules, agents, skills, and hooks — lands on a first-class native mechanism, and
MCP is supported out of the box. gald3r installs without compromise.

## C.R.A.S.H. capability grid

| | Capability | Native? | What gald3r gets here | The gap |
|---|---|:---:|---|---|
| **C** | Commands | ✅ | Slash commands + user-defined prompts (`.kiro/prompts/`, invoked `@name`); skills, hooks, and steering files also surface as slash commands | None — gald3r's `@g-*` set installs as native prompts/slash commands |
| **R** | Rules | ✅ | Steering markdown in `.kiro/steering/` with four inclusion modes (Always / Conditional / Manual / Auto); native `AGENTS.md` support | None — gald3r rules load as first-class steering files |
| **A** | Agents | ✅ | Custom subagents (IDE: `.md` + YAML front matter in `.kiro/agents`; CLI: JSON configs), parallel, own context window, also exposed as slash commands | None — gald3r's `g-agnt-*` roles map directly to native subagents |
| **S** | Skills | ✅ | Agent Skills on the open `agentskills.io` standard — `SKILL.md` + `scripts/`/`references/`/`assets/` in `.kiro/skills/`, progressive disclosure | None — gald3r skill packages are directly portable (same SKILL.md standard) |
| **H** | Hooks | ✅ | Agent Hooks: IDE triggers on save/create/delete, prompt submit, turn complete, before/after tool + spec task; CLI lifecycle `agentSpawn`/`userPromptSubmit`/`preToolUse`/`postToolUse`/`Stop` | None — gald3r's `g-hk-*` session-start / pre-tool / pre-commit wiring fires natively |

_Legend: ✅ native · ⚠️ partial / approximated · ❌ no native mechanism · ❓ unverified_

**Beyond C.R.A.S.H. — MCP: ✅** Native Model Context Protocol support via
`.kiro/settings/mcp.json` (workspace) and `~/.kiro/settings/mcp.json` (global), merged with
workspace precedence; per-agent access through the `mcpServers` field, subagents can scope
tools with wildcards (`@figma/*`), and MCP servers can expose reusable prompts. gald3r's MCP
backend connects directly.

## Adoptable extras (non-C.R.A.S.H.)

Platform-native strengths gald3r can lean on, and which need wiring:

| Feature | Status | gald3r fit |
|---|:---:|---|
| Specs — spec-driven workflow (`requirements.md` / `design.md` / `tasks.md` per feature in `.kiro/specs/`) | ✅ present | Strong native home for gald3r task / PRD parity; hooks can fire before/after spec tasks |
| Config root parity (`.kiro/` + `~/.kiro/`, with `steering/` `skills/` `agents/` `prompts/` `settings/mcp.json`) | ✅ present | Mirrors the `.gald3r_sys` per-platform install pattern — clean, addressable install targets |
| Skills on the open Agent Skills standard (`SKILL.md` + `scripts`/`references`/`assets`) | ✅ present | gald3r skill packages drop straight into `.kiro/skills/` — no adaptation |
| Structured output (JSON/TOON) chat mode | ➖ n.a. | No documented structured chat-output mode found; gald3r's `--json`/`--toon` flags stay framework-side |

## The ceiling, and what's beyond it

gald3r runs at full strength on this platform — commands, rules, agents, skills, and hooks all map onto native mechanisms, so the framework installs without compromise. As third-party adaptation goes, this is the high end: nothing here has to be approximated.

But adaptation, however clean, is still gald3r living as a guest inside someone else's tool. The native build goes further — **gald3r_agent**, running on the **gald3r throne** over the **gald3r_world_tree** — where these primitives aren't mapped onto a host, they *are* the substrate. Same framework, no host in between.

> ### gald3r_agent — coming soon. 🌳

---

<sub>Capabilities verified against the platform's official documentation on 2026-06-02, and
re-verified each release via the gald3r platform-docs crawl. This report describes gald3r's
third-party adaptation surface; it is not an endorsement or critique of the platform itself.</sub>
