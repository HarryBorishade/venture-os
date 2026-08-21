# venture-os

A file-based multi-agent system that discovers, tests, and scales small ventures
with a human acting only as a reviewer at defined gates.

Built on Claude Code subagents. Everything is plain Markdown in git — no server,
no database, no framework. The repo *is* the state.

## Core idea

Agents are organised like a small company:

- **Managers** own a function and delegate to specialists.
- **Specialists** do narrow, cheap, well-scoped work.
- **Peer reviewers** check work before it moves forward.
- **You** approve or reject at gates. You do not run the work.

Agents perform venture discovery themselves. You do not hand them a niche.

## Layout

```
.claude/agents/     subagent definitions (one Markdown file each)
docs/               architecture, operating loop, gates, budget policy
ventures/           one folder per venture under investigation
state/              backlog, decision log, spend ledger
```

## Getting started

1. Open this repo in Claude Code.
2. Read `CLAUDE.md` — it is the standing brief for every session.
3. Run the orchestrator and let it work the loop in `docs/operating-loop.md`.
4. Check `state/decisions.md` for anything waiting on you.

## Status

Scaffold. No ventures running yet.
