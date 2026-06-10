<p align="center">
  <img src="logo/Gald3r_Logo_Big.jpg" alt="Gald3r" width="400" />
</p>

<h1 align="center">gald3r for Kiro Cli</h1>

<p align="center">
  File-based memory, task management, and agent orchestration that runs
  <strong>inside Kiro Cli</strong>. Part of the gald3r framework.
</p>

<p align="center">
  <a href="https://github.com/wrm3/gald3r">gald3r (flagship)</a> |
  <a href="https://github.com/wrm3/gald3r_template_adv">gald3r ADV (all 34 tools)</a> |
  <a href="CHANGELOG.md">Changelog</a>
</p>

---

## What is gald3r?

gald3r is a template you drop into any project to give your AI coding assistant a persistent
brain -- tasks, bugs, plans, constraints that survive every session restart.

- **Persistent memory** (`.gald3r/` brain -- tasks, bugs, plans, constraints)
- **110 skills**, **177 commands**, **37 hooks**, **12 rules**
- Works across **Cursor, Claude Code**, and 32 more tools via AGENTS.md

Everything is plain markdown. No server, no database, no Docker required.

---

## This Edition

**Platform:** Kiro Cli | **Support:** Tier 3 -- AGENTS.md + .gald3r/ brain

---

## Install

```bash
git clone https://github.com/wrm3/gald3r_platform_kiro_cli.git
cp -r gald3r_platform_kiro_cli/project_template/. /path/to/your/project/
```

Then open your project in Kiro Cli and run `@g-setup` to initialize.

> **Using a different tool?** [gald3r ADV -- all 34 platforms](https://github.com/wrm3/gald3r_template_adv)

---

## Platform Readiness

See [READINESS.md](./READINESS.md) for the full C.R.A.S.H. capability grid --
which gald3r features install natively on Kiro Cli, which degrade, and what's planned.

---

## The .gald3r/ Brain

Everything gald3r remembers lives in `.gald3r/` -- plain markdown and YAML, fully yours:
tasks, bugs, plans, constraints, features, ideas, learned facts, and release notes.

---

## Contributing & License

See [CONTRIBUTING.md](./CONTRIBUTING.md) and [Fair Source License 1.1 (FSL-1.1-Apache)](./LICENSE).

---

*gald3r v1.11.0 | [Changelog](CHANGELOG.md) | [All platforms](https://github.com/wrm3/gald3r_template_adv)*