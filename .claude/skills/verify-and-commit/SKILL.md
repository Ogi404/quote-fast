---
name: verify-and-commit
description: Run verification, summarize changes, and create a git commit.
disable-model-invocation: true
allowed-tools: Bash(git status*), Bash(git diff *), Bash(npm run verify), Bash(npm run lint), Bash(npm run build), Bash(npm test), Bash(git add *), Bash(git commit*) 
argument-hint: "[commit message]"
---

1) Run `npm run verify` if it exists; otherwise run `npm run lint` and `npm run build` (and `npm test` if tests exist).
2) If any command fails, fix the issues and rerun until green.
3) Summarize what changed in 5–10 bullets.
4) Stage files with `git add -A`.
5) Create a commit.

Commit message rules:
- If $ARGUMENTS is provided, use it.
- Otherwise infer a conventional commit message.

Never stage or commit `.env*` or secrets.
