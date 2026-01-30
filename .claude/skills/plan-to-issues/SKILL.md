---
name: plan-to-issues
description: Convert a PLAN.md-style plan into GitHub Issues checklist text.
disable-model-invocation: true
allowed-tools: Read, Write
argument-hint: "[optional: focus]"
---

Take the current project plan (PLAN.md if present; otherwise infer from recent context) and produce:

1) A short milestone name.
2) A list of 8–20 GitHub Issues with:
   - Title
   - One-sentence outcome
   - Acceptance criteria checklist
   - Estimate: S/M/L

Rules:
- Keep issues small (1–4 hours each when possible).
- Avoid vague issues like “refactor”. Be specific.
- If missing requirements, ask 3–6 clarifying questions first.

Output format: GitHub-flavored markdown only.

$ARGUMENTS
