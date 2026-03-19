---
name: skill-builder
description: >
  Decide whether work should become a skill, stay a plain edit, use an existing
  tool, or be delegated to a subagent. Use when creating, tightening, or auditing
  a skill folder, especially to remove bloat, sharpen triggers, or decide what
  belongs in SKILL.md versus references or scripts.
---

# Skill Builder

Use this skill when the job is to **create, trim, or audit a skill itself**.

This is a narrow builder, not a meta-agent and not a skill factory. Prefer the
smallest useful answer.

## Use when

- deciding whether a new skill is justified at all
- tightening an existing skill's trigger description or scope
- moving detail out of `SKILL.md` into `references/`
- auditing a skill for bloat, stale instructions, duplicate content, or spec drift

## Do not use when

- a plain file edit will solve the problem faster
- an existing tool or installed skill already covers the work
- the problem is implementation labor across many files rather than reusable guidance
- you are inventing process theater to justify a skill

## Default workflow

1. **Run the decision tree first**
   Read `references/decision-tree.md` and decide between plain edit, existing tool/skill,
   subagent, or a lean skill.

2. **If a skill is justified, keep SKILL.md minimal**
   Include only:
   - clear frontmatter (`name`, `description`)
   - scope and non-scope
   - default workflow
   - reference pointers when optional detail is useful

3. **Place detail intentionally**
   Read:
   - `references/frontmatter-patterns.md` for naming and description patterns
   - `references/supporting-files-guide.md` for what belongs in `SKILL.md`, `references/`, and `scripts/`

4. **Audit before expanding**
   Use `references/audit-checklist.md` to remove bloat, stale claims, weak triggers,
   duplicate guidance, and files that do not earn their keep.

5. **Apply the Tool Addition Gate lightly**
   If the proposed skill is compensating for a missing primitive, check this order:
   existing tools → lean skill → subagent/retrieval pattern → new tool only if clearly needed.

## Good outcomes

- A plain edit stays a plain edit
- An existing skill gets tightened instead of replaced
- A new skill has a sharp trigger description and a short `SKILL.md`
- Supporting files exist only when they reduce context load or improve reliability

## Avoid

- turning one-off work into a permanent skill
- adding README, changelog, or setup clutter inside the skill unless publishing truly needs it
- stuffing examples, schemas, and edge cases into `SKILL.md`
- creating scripts for things that are better as instructions
- inventing governance layers, registries, dashboards, or lifecycle systems

## References

- `references/decision-tree.md` — choose skill vs tool vs subagent vs plain edit
- `references/frontmatter-patterns.md` — lean frontmatter and description patterns
- `references/supporting-files-guide.md` — what belongs in each folder
- `references/audit-checklist.md` — fast bloat/spec-drift review

## Output style

Lead with the recommendation:
- **Use a skill**
- **Use the existing tool/skill**
- **Use a subagent**
- **Do nothing special; just edit it**

Then give the smallest set of file changes needed.
