# claude-github-skill

> A polished workspace for designing and refining a unified Claude Code `/github` skill that spans both local Git workflow and remote GitHub operations.

---

## Overview

This repository is the working area for shaping a single `/github` interface around the full day-to-day developer loop:

- **Local Git workflow** — `commit`, `push`, `pull`, `branch`, `checkout`, `merge`, `rebase`
- **Remote GitHub workflow** — pull requests, issues, and CI / workflow runs

The active installed copy currently lives in the global Claude skills directory:

- `/Users/liyao/.claude/skills/github/SKILL.md`

So this repository is best understood as the **design, refinement, and packaging workspace** for that skill.

## Scope

### Local Git operations

- inspect repository state safely
- manage branches and sync flow
- support common Git actions like `commit`, `pull`, `push`, `merge`, and `rebase`
- keep higher-impact actions explicit and controlled

### Remote GitHub operations

- inspect and manage pull requests
- inspect and manage issues
- check CI / workflow status with `gh`
- connect local branch state with GitHub collaboration flow

## Repository contents

| Path | Role |
| --- | --- |
| `README.md` | project overview, current workflow, and repository intent |
| `SKILL.md` | canonical maintained `/github` skill definition for this repository |
| `openclaw-github-SKILL.md` | upstream reference material pulled from OpenClaw for comparison and adaptation |
| `.claude/settings.local.json` | local Claude Code permission/config context used while iterating in this repo |

## Current usage model

The repo-local Claude-discovery copy was intentionally removed after the global install was set up, but the repository still keeps the canonical skill source in `SKILL.md`.

Use the skill from Claude Code through:

- `/github`

As long as the global skill exists at `/Users/liyao/.claude/skills/github/SKILL.md`, the command can be used without depending on a repo-local `.claude/skills/github/` copy.

## Why keep this repository

Even with a global install, this repository remains the right place to:

- refine the skill contract and operating rules
- track reference material and revisions
- shape how local Git and remote GitHub capabilities should be unified
- add examples, verification notes, and future packaging decisions

## Roadmap

- strengthen the skill instructions and safety boundaries
- add concrete usage examples
- document lightweight verification flows
- decide whether to stay global-only or restore a repo-local packaged version later
