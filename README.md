# scope-check

A free Agent Skill (SKILL.md) for Claude Code, Cursor and other Agent Skills-compatible tools. Paste a vague client request and get back: unclear requirements, assumptions, missing information, dependencies, risks, exclusions, acceptance criteria and up to 8 client questions (blockers first), before you quote or write code.

## Install

Claude Code (project):

    mkdir -p .claude/skills && cp -R skills/scope-check .claude/skills/

Cursor (project):

    mkdir -p .cursor/skills && cp -R skills/scope-check .cursor/skills/

Then type `/scope-check` and paste the client's brief.

## Example

Input: "Build a booking site for my salon, like Calendly. Needs to look modern. Launch next month."

Output (abridged):

- Unclear: payments or free bookings? reminders (email/SMS)? who can cancel or reschedule, and until when?
- Risk: "like Calendly" is open-ended (calendar sync, time zones, staff schedules). Mitigation: list exactly which features are in v1.
- Out of scope until confirmed: native mobile app, multi-location, loyalty points.
- Accept when: a customer can book, pay and receive a confirmation email within 1 minute.
- First client question: "Do customers pay online at booking, or in the salon?"

## Next steps in the workflow (paid, optional)

- Turn the answers into a one-page fixed quote: Scope-to-Quote, $15 - https://klipora.gumroad.com/l/onepager
- Project context + review/QA/handoff skills: Client Project Launch Kit, $19 - https://klipora.gumroad.com/l/client-project-launch-kit
- Priced change orders for mid-project requests: Change Order Kit, $15 - https://klipora.gumroad.com/l/change-order-kit
- All three: Scope-to-Cash Bundle, $35 - https://klipora.gumroad.com/l/scope-to-cash

Free listing page: https://klipora.gumroad.com/l/scope-check

## License

MIT for the skill file in this repository. Not legal advice; no income claims.
