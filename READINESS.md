# gald3r Readiness Report — Kiro CLI (Amazon)

> An honest accounting of how much of the gald3r framework installs natively on this
> platform, what degrades to an approximation, and what has no native home yet.
> Generated from a live documentation crawl on 2026-06-02.

**Overall readiness: ✅ Full.** Kiro CLI is Amazon's spec-driven, agent-centric terminal
coding assistant (the Q Developer CLI rebrand). Every gald3r layer — commands, rules, agents,
skills, and hooks — maps onto a native `.kiro/` mechanism, and MCP ports straight across.

## C.R.A.S.H. capability grid

| | Capability | Native? | What gald3r gets here | The gap |
|---|---|:---:|---|---|
| **C** | Commands | ✅ | Skills auto-surface as `/skill-name` slash commands; `/prompts create` adds local prompt templates | No dedicated `commands/` file format — gald3r's `@g-*` set maps onto skills rather than a per-command directory |
| **R** | Rules | ✅ | `.kiro/steering/` always-on files (`product`/`tech`/`structure` auto-loaded) + native `AGENTS.md` standard | None — gald3r rules install as steering; non-foundation files just need explicit inclusion |
| **A** | Agents | ✅ | Custom agents as JSON config (filename = agent name) + subagents in isolated context (up to 4 at once) | JSON-only authoring — gald3r's markdown `g-agnt-*` roles need a translation step to JSON |
| **S** | Skills | ✅ | Native Agent Skills engine — `SKILL.md` + YAML frontmatter, progressively loaded from `.kiro/skills/` & `~/.kiro/skills/` | None — open Agent-Skills standard, directly compatible with gald3r's `SKILL.md` format |
| **H** | Hooks | ✅ | Five lifecycle events (`agentSpawn`, `userPromptSubmit`, `preToolUse`, `postToolUse`, `stop`); `preToolUse` can block via exit 2 | Hooks live in each agent's JSON `hooks` field — global/cross-agent automation must be replicated per agent |

_Legend: ✅ native · ⚠️ partial / approximated · ❌ no native mechanism · ❓ unverified_

**Beyond C.R.A.S.H. — MCP: ✅** Native Model Context Protocol via `mcp.json` at project
(`.kiro/settings/mcp.json`) and global (`~/.kiro/settings/mcp.json`) scope; the `mcpServers`
schema matches the common Claude/Cline convention, so gald3r MCP definitions port directly.

## Adoptable extras (non-C.R.A.S.H.)

Platform-native strengths gald3r can lean on, and which need wiring:

| Feature | Status | gald3r fit |
|---|:---:|---|
| Reusable local prompts (`/prompts create`, stored under `.kiro/`) | ✅ present | Extra surface for gald3r prompt templates alongside skills |
| Runtime context rules (`/context show \| add \| remove`, glob-based) | ⚙️ needs customization | Could scope gald3r's `.gald3r/` files into live context per task |
| Spec-driven development (requirements → design → tasks) | ⚙️ needs customization | Aligns with gald3r's PRD/feature/task pipeline; worth mapping |
| Agent output side channels (`$AGENT_DISPLAY_OUT` / `$AGENT_CONTEXT_OUT`, v2.3) | ⚙️ needs customization | Lets gald3r hooks stream into display vs. agent context separately |
| Interactive authoring (`/agent create`, `/guide`) | ✅ present | AI-assisted scaffolding of agents, prompts, and steering into `.kiro/` |

## The ceiling, and what's beyond it

gald3r runs at full strength on this platform — commands, rules, agents, skills, and hooks all map onto native mechanisms, so the framework installs without compromise. As third-party adaptation goes, this is the high end: nothing here has to be approximated.

But adaptation, however clean, is still gald3r living as a guest inside someone else's tool. The native build goes further — **gald3r_agent**, running on the **gald3r throne** over the **gald3r_world_tree** — where these primitives aren't mapped onto a host, they *are* the substrate. Same framework, no host in between.

> ### gald3r_agent — coming soon. 🌳

---

<sub>Capabilities verified against the platform's official documentation on 2026-06-02, and
re-verified each release via the gald3r platform-docs crawl. This report describes gald3r's
third-party adaptation surface; it is not an endorsement or critique of the platform itself.</sub>
