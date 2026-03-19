# Skill Builder

**Build lean SKILL.md-based skills without building a skill factory.**

`skill-builder` helps agent builders decide when a skill is actually justified, draft a minimal skill skeleton, and audit existing skills for bloat and drift.

It is built for people who keep hitting the same questions:
- Should this be a **skill**, a **tool**, a **subagent**, or just a plain edit?
- What belongs in `SKILL.md` versus `references/` versus `scripts/`?
- How do I build a useful skill without spawning README/changelog/template junk?
- How do I tighten an existing skill without rewriting everything from scratch?

## Why this exists

Most skill-authoring advice falls into one of two bad buckets:

1. **Too vague** — “just write a good SKILL.md”
2. **Too ceremonial** — giant templates, governance layers, dashboards, policy engines, and file sprawl

`skill-builder` takes the middle path:
- **builder-first** enough to produce a real starting skeleton
- **reviewer-guarded** enough to stop you from overbuilding

It is explicitly designed to help you ship a **small, usable skill** fast.

## What it does

`skill-builder` operates in three modes:

### 1. Decide
Choose between:
- **plain edit**
- **existing tool or existing skill**
- **subagent**
- **lean new skill**

### 2. Build
When a skill is justified, it helps build the smallest useful package:
- minimal folder tree
- draft frontmatter
- `SKILL.md` outline or draft
- 1–3 justified `references/` files only if needed
- optional `scripts/` stub only if deterministic execution is clearly warranted

### 3. Audit
Tighten an existing skill by checking for:
- bloated `SKILL.md`
- weak trigger descriptions
- duplicated guidance
- stale instructions
- unnecessary files
- scope drift

## What makes it different

This skill is intentionally **not**:
- a meta-agent
- a governance engine
- an autonomous skill factory
- a repo/dashboard/lifecycle system
- a boilerplate generator that creates ten files before proving one is needed

It is optimized for one thing:

> **helping you build smaller, sharper skills that are actually worth keeping**

## Typical use cases

Use `skill-builder` when you want to:
- create a new OpenClaw / AgentSkills-compatible skill
- decide whether a repeated workflow should become a skill at all
- restructure a skill that has grown into a wall of text
- split a large skill into `SKILL.md` plus focused references
- tighten a published skill before pushing to GitHub or ClawHub

## Example prompts

- “Should this become a skill or just stay a plain edit?”
- “Build me a lean skill skeleton for OpenClaw config troubleshooting.”
- “Audit this skill for bloat and spec drift.”
- “Tighten this `SKILL.md` and move detail into references.”
- “Decide what belongs in `SKILL.md` versus `references/` versus `scripts/`.”

## Example build output

A typical minimal result looks like this:

```text
Recommendation: Use a skill

my-skill/
├── SKILL.md
└── references/
    └── checklist.md
```

```yaml
name: my-skill
description: Helps with X. Use when the user asks for Y or needs Z.
```

Then `SKILL.md` only needs:
- scope / non-scope
- default workflow
- pointer to the optional reference file

That’s the point: **usable first, elaborate later only if earned**.

## Repository contents

- `skill-builder/SKILL.md` — main skill entrypoint
- `skill-builder/references/decision-tree.md` — choose skill vs tool vs subagent vs plain edit
- `skill-builder/references/frontmatter-patterns.md` — naming and description patterns
- `skill-builder/references/supporting-files-guide.md` — what belongs in each folder
- `skill-builder/references/audit-checklist.md` — fast bloat/spec-drift review

## Who this is for

This is for people building skills in:
- OpenClaw
- AgentSkills-compatible environments
- Claude Code / Codex-style SKILL.md workflows
- local agent workspaces that need discipline, not more abstraction theater

If you care about:
- progressive disclosure
- smaller context footprint
- reusable workflows
- anti-bloat design
- practical skill authoring

this skill is for you.

## Installation

### ClawHub

```bash
clawhub install lean-skill-builder
```

### Manual

Copy the `skill-builder/` folder into your skills directory.

## Positioning in one sentence

`skill-builder` helps you decide when to build a skill, build the smallest viable one, and keep it from turning into prompt sludge.

## License

MIT
