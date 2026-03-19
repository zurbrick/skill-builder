# Supporting Files Guide

The skill folder should stay small. Every file should earn its keep.

## `SKILL.md`

Put these here:
- frontmatter (`name`, `description`)
- scope and non-scope
- default workflow
- concise rules of thumb
- explicit links to supporting files

Keep in `SKILL.md` only what the agent should likely see whenever the skill triggers.

### Move content out of `SKILL.md` when:
- it is detailed reference material
- it is only needed in some cases
- it is long examples, schemas, checklists, or variant-specific guidance
- it makes the core workflow harder to scan

---

## `references/`

Put these here:
- decision trees
- checklists
- examples and patterns
- schemas or domain notes
- variant-specific instructions

Use `references/` when the material is useful context but not mandatory on every trigger.

Good fits:
- audit checklist
- naming/frontmatter patterns
- folder placement rules
- API or domain reference notes

Bad fits:
- duplicate copies of SKILL.md guidance
- placeholder docs with no concrete use
- README/changelog/process notes for humans

---

## `scripts/`

Put code here only when code is genuinely the better form.

Good fits:
- deterministic transformations
- repeatable helpers that would otherwise be rewritten often
- fragile sequences where exact execution matters

Do **not** add a script when:
- a few lines of instructions are enough
- the script exists only to justify the skill
- nobody is likely to run it more than once
- the environment assumptions are unclear and untested

Rule of thumb: if the main value is judgment, keep it as guidance; if the main value is exact repeatable execution, consider a script.

---

## Minimal folder patterns

### Small skill

```text
skill-name/
└── SKILL.md
```

### Skill with optional detail

```text
skill-name/
├── SKILL.md
└── references/
    └── checklist.md
```

### Skill with deterministic helper

```text
skill-name/
├── SKILL.md
├── references/
│   └── patterns.md
└── scripts/
    └── helper.py
```

Start with the smallest pattern that works.
