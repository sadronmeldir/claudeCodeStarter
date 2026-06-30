# Claude Code Project Starter

A template for new projects with Claude Code — includes curated skills and working instructions.

## Using this template in a new project

1. Copy the `.claude/` directory and `CLAUDE.md` into your project root.
2. Open the project in Claude Code.
3. The skills below are immediately available via `/skill-name`.

## Included skills

Skills sourced from [mattpocock/skills](https://github.com/mattpocock/skills).

### Grilling & design

| Skill | Trigger | Purpose |
|-------|---------|---------|
| `/grill-me` | Manual | Relentless interview to stress-test a plan or design |
| `/grill-with-docs` | Manual | Same as above, but also maintains your `CONTEXT.md` glossary and ADRs |
| `/grilling` | Auto | Underlying interview loop used by the above two |
| `/domain-modeling` | Auto | Build and maintain the project's domain glossary (`CONTEXT.md`) and ADRs |

### Code quality & architecture

| Skill | Trigger | Purpose |
|-------|---------|---------|
| `/improve-codebase-architecture` | Manual | Scan for shallow modules, generate a visual HTML report, then grill through a fix |
| `/codebase-design` | Auto | Shared vocabulary for deep modules (seam, adapter, leverage, locality) |
| `/diagnosing-bugs` | Auto | Structured 6-phase debugging loop — builds a feedback loop before hypothesising |
| `/review` | Manual | Two-axis review: coding standards + spec conformance, run in parallel sub-agents |

### Workflow utilities

| Skill | Trigger | Purpose |
|-------|---------|---------|
| `/handoff` | Manual | Compact current conversation into a handoff doc for the next session |
| `/triage` | Manual | Move issues/PRs through a state machine; write agent-ready briefs |
| `/git-guardrails-claude-code` | Manual | Install hooks to block destructive git commands (`push`, `reset --hard`, etc.) |

## CLAUDE.md

The included `CLAUDE.md` sets five working principles:

1. Ask before assuming — no silent assumptions about intent or architecture
2. Simplest solution for simple problems; better solutions for harder ones
3. Don't touch unrelated code — surface smells as separate issues
4. Flag uncertainty explicitly; run small experiments rather than guessing
5. Suggest better approaches proactively

## First steps in a new project

```
/grill-with-docs     # sharpen your initial plan and start a CONTEXT.md
/git-guardrails-claude-code  # set up safety hooks (recommended)
```
