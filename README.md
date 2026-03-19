# skill-builder

A lean AgentSkills-compatible skill for deciding whether work should become a skill, stay a plain edit, use an existing tool, or be delegated to a subagent.

## What it does

`skill-builder` helps with four narrow jobs:
- decide **skill vs tool vs subagent vs plain edit**
- draft or tighten a lean `SKILL.md`
- decide what belongs in `SKILL.md` vs `references/` vs `scripts/`
- audit existing skills for bloat, stale instructions, duplicate content, and spec drift

This skill is intentionally **not**:
- a meta-agent
- a governance engine
- a skill factory
- a new runtime/tooling layer

## Included files

- `skill-builder/SKILL.md`
- `skill-builder/references/decision-tree.md`
- `skill-builder/references/frontmatter-patterns.md`
- `skill-builder/references/supporting-files-guide.md`
- `skill-builder/references/audit-checklist.md`

## Packaging

A packaged artifact is also available at:
- `../../dist-skills/skill-builder.skill`

## Publishing notes

This export is ready for GitHub and ClawHub publication.

One thing intentionally left open: **license choice**.
No LICENSE file is included because that should be an explicit decision, not guessed.
