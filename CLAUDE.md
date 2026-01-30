# Project Operating System (Claude Code)

## Goals
- Ship small increments fast.
- Keep Claude Code stable (avoid giant sessions).
- Always leave the repo in a working state.

## Workflow (mandatory)
1) Start in **Plan mode** first for any multi-file change.
2) Write/refresh `PLAN.md` (or a section in it) *before* edits.
3) Implement **one step only**.
4) Run `npm run verify` (or equivalent) and fix failures.
5) Commit with a clear message.
6) Repeat.

## Definition of Done (DoD)
- Lint passes
- Tests pass (if any)
- Build passes
- No secrets committed (.env, keys)
- README updated if behavior changed

## Safety
- Never read or commit `.env*` or `secrets/**`.
- Ask before destructive commands.
- Ask before `git push`.

## Notes
- Prefer explicit file lists in prompts.
- Use `/compact` regularly.
