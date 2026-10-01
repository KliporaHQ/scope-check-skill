---
name: scope-check
description: "Use when a client request is vague, incomplete, or contradictory — before writing feature code. Turns a messy ask into unclear requirements, assumptions, missing info, dependencies, risks, exclusions, acceptance criteria, and client questions."
---

# Scope Check

## Overview

Turn a vague client request into a practical scope report the client (or you) can confirm before implementation. Prefer concrete lists over essays. Do not invent requirements the client never implied — mark them as assumptions or questions.

## Inputs

- The raw client message / brief (paste or path)
- Optional: existing `project-context.md`, stack notes, prior tickets
- Optional: deadline, budget constraints, or known out-of-scope items

## Steps

1. **Restate the ask in one sentence** — what success looks like if the request were clear.
2. **Unclear requirements** — bullet each ambiguous phrase; say *why* it is unclear (missing actor, missing data, missing UI state, missing edge case).
3. **Assumptions** — only what you must assume to proceed; label each as *safe to assume* vs *needs confirmation*.
4. **Missing information** — facts you cannot invent (API keys source, brand assets, environments, content owners, analytics IDs, legal copy).
5. **Dependencies** — systems, people, third-party services, design files, data migrations, other tickets.
6. **Risks** — technical, schedule, scope-creep, security/privacy; include a short mitigation for each.
7. **Exclusions (out of scope)** — explicit non-goals so the client cannot later claim them were implied.
8. **Acceptance criteria** — testable bullets (Given/When/Then or checklist). Prefer observable outcomes.
9. **Client questions** — max 8 high-leverage questions, ordered by blockers first. Each question should be answerable in one sentence or a choice.
10. **Suggested next step** — e.g. wait for answers / fill project-context / start spike on X only.

## Output format

```markdown
# Scope check — <short title>

## One-sentence restatement
...

## Unclear requirements
- ...

## Assumptions
- [needs confirmation] ...
- [safe] ...

## Missing information
- ...

## Dependencies
- ...

## Risks
| Risk | Impact | Mitigation |
|------|--------|------------|
| ... | ... | ... |

## Exclusions
- ...

## Acceptance criteria
- [ ] ...

## Client questions (blockers first)
1. ...

## Suggested next step
...
```

## Stop conditions

- Stop if there is no client request or brief to analyze.
- Stop after the report; do not start implementing features unless the user explicitly asks.
- If the request is already precise and acceptance criteria exist, say so briefly and offer only gap questions.

## Anti-patterns

- Do not pad with generic "best practices" unrelated to this ask.
- Do not invent fake deadlines, budgets, or stakeholder names.
- Do not turn exclusions into upsells or income claims.
- Do not claim the scope is "approved" — only the client can approve.
