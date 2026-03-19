# Audit Checklist

Use this to trim a skill or check for spec drift.

## 1. Trigger quality

- [ ] Is the `description` clear about what the skill does?
- [ ] Does it say when to use the skill?
- [ ] Would normal user phrasing trigger it?
- [ ] Is the scope honest, or is it promising too much?
- [ ] Are there obvious overlaps with another existing skill?

## 2. SKILL.md discipline

- [ ] Is `SKILL.md` easy to scan?
- [ ] Does it contain the core workflow, not every edge case?
- [ ] Are long examples/checklists moved into `references/`?
- [ ] Are references named explicitly so they are discoverable?
- [ ] Does the file avoid policy sprawl and manifesto language?

## 3. Folder hygiene

- [ ] Does every file directly support the skill’s job?
- [ ] Are there unnecessary docs like README, CHANGELOG, or setup notes?
- [ ] Are there stale placeholders or abandoned experiments?
- [ ] Is there any duplicated content between `SKILL.md` and `references/`?
- [ ] Are scripts present only when deterministic execution is needed?

## 4. Spec drift and staleness

- [ ] Do instructions still match the current tools/workflow?
- [ ] Are referenced files and paths real?
- [ ] Are examples still accurate?
- [ ] Did the skill accrete side-missions beyond its original purpose?
- [ ] Should some content be deleted instead of updated?

## 5. Do-nothing check

Before expanding the skill, ask:
- [ ] Would a plain edit solve this faster?
- [ ] Would using an existing tool or skill solve it cleanly?
- [ ] Is this really a subagent problem, not a skill problem?
- [ ] Is the proposed addition carrying its own weight?

## 6. Tool Addition Gate (lightweight)

- [ ] Did we check existing tools first?
- [ ] Would a lean skill solve the problem without inventing a new primitive?
- [ ] Is a new script/tool being proposed for a real capability gap rather than convenience theater?

## Recommended outcomes

### Keep as-is
The skill is already sharp, current, and lean.

### Tighten
Trim wording, improve description, move detail into `references/`, delete dead files.

### Restructure lightly
Keep the skill, but separate core workflow from supporting detail.

### Retire / merge
If the skill duplicates another one or no longer earns its context cost, remove or merge it.
