---
name: company-brain
description: Use the team's Company Brain (shared company memory) whenever work touches the company — customers, people, past decisions, promises, product, pricing, strategy, hiring, fundraising, or writing on the company's behalf. Load the brief before such work, search before answering company questions, and save new decisions, commitments and learnings so every teammate and AI tool has them.
---

# Company Brain

Company Brain is this team's shared memory. Everyone on the team and every AI tool they use (ChatGPT, Codex, Claude Code) reads and writes the same brain through the `companybrain` tools.

## When work starts

If the task involves the company, call `brief` once (pass `topic` when the task is about one customer, project or question). Use what it returns instead of asking the user to re-explain their company.

## Before answering

For questions about customers, people, decisions, promises or "why did we…", call `search` first, then `fetch` the best hits. Cite memories with their date and source. If nothing is found, say so; never invent company facts.

## While working, save what matters

Call `remember` when any of these happen:

- **decision** — something was decided. Include the why and who decided.
- **commitment** — someone promised something. Include owner, recipient and `due_date`.
- **customer** / **person** — a durable fact about a customer or contact (role, needs, preferences, status).
- **meeting** — outcomes and next steps of a meeting or call.
- **fact** — a lasting learning (market, product, sales, technical).
- **profile** — what the company is and does (replaces the old profile).

To import notes, a document, a meeting transcript or onboarding answers, split them into one fact per memory and save them with a single `remember_many` call (up to 25 per call).

Rules:

- One fact per memory, in plain language a new teammate could follow.
- Always fill `source` (meeting, Slack channel, email, document, "coding session in repo X").
- Tag customers, people and projects by name.
- Update instead of duplicating: use `update_memory`, or `remember` with `supersedes`. Saving the same kind and title again updates the existing memory. Mark commitments `done` when they are.
- Never save passwords, API keys or other secrets, or personal data that isn't needed for work.
- In coding sessions, save product and architecture decisions and their reasons, not routine code changes.

## Team

`invite_teammate` returns a link that adds a teammate to the same brain. The web view is at https://companybrain.me/brain.
