---
applyTo: "docs/**"
---

# Documentation Rules (`docs/`)

## Language and voice

- English only, for every file in this tree. Persistent artifacts must read
  identically to every model and every future session; mixed-language docs
  cause nuance drift.
- Write in the imperative for procedures and in plain declarative sentences
  for facts. State *why* a rule exists when it is not obvious.

## The two tiers are different

- `docs/context/` is an **intake area**: raw, possibly redundant, never
  authoritative. Every file starts with the provenance header defined in
  `.github/skills/context-collection/SKILL.md`. Do not "clean up" raw material
  into conclusions here — that is distillation and it happens elsewhere.
- `docs/agreements/` is **reviewed truth**: requirements (`REQ-###`), ADRs
  (`ADR-####`), glossary, non-goals. What earns a place here is defined by
  `.github/skills/context-distillation/SKILL.md` (§When an agreement is
  warranted) — most changes belong in a Task issue instead. Files here change
  **only via pull request** with at least one human approval, but that PR need
  not be a dedicated one: correcting the wording of a `REQ`, glossary entry, or
  non-goal may ride in the implementation PR that discovered the problem, as
  long as the PR description calls the change out. Reserve a separate
  agreements PR for ADRs and for reversals other in-flight tasks depend on.

## Traceability

- New or changed requirements get the next free `REQ-###` ID; never reuse IDs.
  Superseded requirements are marked `(superseded by REQ-###)`, not deleted.
- ADRs are numbered sequentially from `ADR-0001` and follow
  `docs/agreements/adr/ADR-0000-template.md`. An ADR that reverses a previous
  decision must reference the ADR it supersedes.
- A decision made elsewhere (issue thread, PR review, chat) becomes an
  agreement only once it lands here through a PR — but only decisions that
  clear the bar in `.github/skills/context-distillation/SKILL.md` (§When an
  agreement is warranted) need to land here at all. Copy the conclusion, link
  the discussion.
