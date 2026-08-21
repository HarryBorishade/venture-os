# Architecture

## Why file-based

State lives in git. That gives version history, diffs, rollback, and human
readability for free. No infrastructure to run or pay for. Any session can pick
up where the last one stopped by reading files.

The trade-off: no real-time coordination, no parallel writes. Acceptable — the
work is deliberative, not high-throughput.

## Roles

```
              orchestrator
                    |
     +--------------+--------------+-------------+
     |              |              |             |
  research       product        growth       finance
  manager        manager        manager      controller
     |              |              |
  scout         builder        copywriter
  analyst       qa-reviewer    experimenter
```

`peer-reviewer` is called by any manager and is deliberately adversarial.

## Delegation contract

A manager delegating to a specialist must supply:

- The question, stated as a question
- What a good answer looks like
- What is out of scope
- Where to write the output

A specialist returns a written artefact and a one-paragraph summary. Nothing
else. Managers do not read specialist scratch work.

## Model tiering

| Role | Tier | Why |
|---|---|---|
| Scouts, copywriters | Haiku | Volume work, narrow scope |
| Managers, analysts, builders | Sonnet | Judgement with structure |
| Peer reviewer, gate prep | Opus | Where being wrong is expensive |

Start one tier lower than feels right. Escalate on demonstrated failure.
