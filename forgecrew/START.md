# czkawka - Agent Instructions

This document is the entrypoint for AI agents working on czkawka.

## Getting Started

1. Read your role document via `mcp__pride__doc_read` with `docId="role-<name>"` (e.g., `role-engineer`)
2. If you write/review/test code: also read `role-eng-standards` via `mcp__pride__doc_read`
3. Read your assigned task file in `forgecrew-work/tasks/`

## Directory Structure

### Agent Instructions

| Path                  | Purpose                                             |
| --------------------- | --------------------------------------------------- |
| `forgecrew/START.md`  | This file - agent entrypoint                        |
| Built-in role docs    | Via `mcp__pride__doc_read` with `role-<name>` keys  |

### Project Standards (`forgecrew/docs/`)

| Path         | Purpose                                 |
| ------------ | --------------------------------------- |
| `standards/` | Project coding standards (customizable) |

### Work Documents (`forgecrew/.state/work/`)

| Path        | Purpose                                     |
| ----------- | ------------------------------------------- |
| `intake/`   | Incoming work (proposals, issues, breakage) |
| `prep/`     | Planning docs (research, designs, plans)    |
| `tasks/`    | Ready to execute                            |
| `review/`   | Feedback (audits)                           |
| `_archive/` | Archived artifacts                          |

## Commands

### Pride (Agent Lifecycle)

```bash
pride checkin <role>-N    # Create/reactivate agent worktree
pride checkout <role>-N   # Mark agent inactive
pride agents              # List all agents
pride help                # Full command help
```

### Den (Git Workflow)

```bash
den sync                  # Fetch + rebase onto master
den validate              # Run full quality gate (clean + analyze + test)
den push                  # Rebase + validate + push
den submit                # Push + create PR
den help                  # Full command help
```

## Golden Rule

**Agents do not push to the default branch. PRs only. Project owner merges.**
