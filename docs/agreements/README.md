# `docs/agreements/` — Reviewed Truth (Phase 2)

The distilled, human-approved knowledge every agent designs against.
Produced from `docs/context/` by
`.github/skills/context-distillation/SKILL.md`; change control by
`.github/instructions/docs.instructions.md` (**PR + human approval only** —
merge is what makes something an agreement).

| File | Holds |
|---|---|
| `requirements.md` | Verifiable requirements, one `REQ-###` each |
| `non-goals.md` | Explicit "we will not" list |
| `glossary.md` | Project vocabulary |
| `adr/ADR-####-<slug>.md` | One architectural decision per record |
| `retro-log.md` | Ledger of system improvements (`retro:` PRs) |

Task issues cite these by ID (`REQ-###`, `ADR-####`) **when a relevant
agreement exists** — most tasks are fully specified by their own issue and cite
nothing, which is fine. What earns a place here is defined by
`.github/skills/context-distillation/SKILL.md` (§When an agreement is
warranted). If work reveals an agreement is wrong, fix it: a wording fix may
ride in the implementation PR (call it out in the description); an ADR reversal
gets its own PR.
