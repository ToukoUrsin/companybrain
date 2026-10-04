# Company Brain

Your team's shared memory for ChatGPT, Codex and Claude Code. Decisions and why they were made, customers, people, promises and meeting outcomes live in one place, and every teammate's AI tools read and add to it.

Create your brain at **https://companybrain.me/start** (passkey sign-in, invite teammates with a link).

## Install

**Codex**

```sh
codex plugin marketplace add ToukoUrsin/companybrain
codex plugin add companybrain@companybrain
```

or just the MCP server: `codex mcp add companybrain --url https://companybrain.me/mcp`

**Claude Code**

```sh
claude plugin marketplace add ToukoUrsin/companybrain
claude plugin install companybrain@companybrain
```

or just the MCP server: `claude mcp add --transport http companybrain https://companybrain.me/mcp`

**ChatGPT**

Listing in the ChatGPT plugin directory is in review. Until then, turn on Developer mode in ChatGPT settings and add a custom MCP app with `https://companybrain.me/mcp` (OAuth).

## Tools

| Tool | What it does |
|---|---|
| `brief` | Company profile, open commitments, recent decisions, customers, what changed this week |
| `search` / `fetch` | Find and read memories |
| `recent` | What changed in the last N days |
| `remember` | Save a decision, commitment, customer, person, fact, meeting or profile |
| `update_memory` / `forget` | Correct, complete or remove a memory |
| `invite_teammate` | Link that adds a teammate to the same brain |

The bundled `company-brain` skill tells the agent when to read and when to save.

Privacy: https://companybrain.me/privacy · Terms: https://companybrain.me/terms · Support: hello@companybrain.me
