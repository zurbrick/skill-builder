# Frontmatter Patterns

Keep frontmatter sharp. The description is the trigger surface.

## Minimum viable frontmatter

```yaml
---
name: skill-name
description: >
  One or two sentences describing what the skill does, when to use it,
  and the kinds of requests that should trigger it.
---
```

Use extra fields only when they match the local style and clearly help. Do not pad.

## Naming guidance

- use lowercase hyphen-case
- prefer short, concrete names
- name for the job, not the aspiration
- avoid vague labels like `workflow-manager` or `universal-helper`

Good:
- `skill-builder`
- `cron-doctor`
- `openclaw-guide`

Weak:
- `skill-system`
- `meta-skill-orchestrator`
- `general-automation-framework`

## Description pattern

A strong description usually covers:
1. **what it does**
2. **when to use it**
3. **what kinds of phrases or tasks should trigger it**

### Simple pattern

```yaml
---
name: example-skill
description: >
  [Primary job]. Use when [situation]. Helps with [2-4 concrete tasks or trigger phrases].
---
```

### Example

```yaml
---
name: skill-builder
description: >
  Decide whether work should become a skill, stay a plain edit, use an existing tool,
  or be delegated to a subagent. Use when creating a new skill, trimming an existing one,
  or auditing a skill for bloat, stale instructions, or unclear triggers.
---
```

## Description quality checks

Good descriptions are:
- specific enough to trigger correctly
- broad enough to catch normal phrasings
- honest about scope
- free of hype

Bad signs:
- no clue when to use it
- promises implementation, review, deployment, and governance all at once
- stuffed with internal jargon
- so narrow it only matches one exact sentence

## Scope wording

It is often worth adding a short body section for:
- **Use when**
- **Do not use when**

This keeps the description clear without cramming everything into frontmatter.
