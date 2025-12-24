# human-general-intelligence

Personal workflow toolkit with commands for planning, version control, session management, and productivity tools. Includes specialized agent for processing Readwise highlights.

## Features

### Commands (7)
- **`/follow-plan`** - Follow the active plan from CLAUDE.md
- **`/git-commit`** - Create well-written commits (72-char line limit, explains decisions)
- **`/git-summary`** - Get comprehensive Git repository status
- **`/handoff`** - Create session handoff summary with context and next steps
- **`/multi-perspective-review`** - Review changes from multiple perspectives with ultrathink
- **`/today`** - Chief of Staff daily planning (optional Google Calendar integration)
- **`/token-shortener`** - Minimize token usage while retaining key information

### Agent (1)
- **`@readwise-highlight-ingester`** - Extract and organize highlights from Readwise Reader shared links

## Installation

This plugin is distributed via the human-general-intelligence marketplace. See the marketplace README for installation instructions.

## Quick Start

### Commands

All commands are available via `/` menu:

```
/follow-plan       # Review and follow active plans
/git-commit        # Commit with better messages
/git-summary       # Analyze repo state
/handoff          # Prepare session handoff
/multi-perspective-review  # Multi-agent code review
/today            # Daily planning assistant
/token-shortener  # Optimize token usage
```

### Agent

Use the Readwise agent to ingest highlights:

```
@readwise-highlight-ingester
```

Then provide a Readwise Reader shared link.

## Google Calendar Integration (Optional)

The `/today` command works standalone, but can integrate with Google Calendar for calendar-aware daily planning.

### Setup

1. Install Google Calendar MCP server:
   ```bash
   claude mcp add
   ```

2. Search for "google-calendar" and follow prompts

3. Run `/today` - it will now include calendar context

### Without Calendar

No worries! The command gracefully handles missing calendar:
- Scans your todo list and notes instead
- Provides excellent daily planning without calendar
- Show warning if calendar MCP not available

## Permissions

The plugin includes permission rules for:
- **Allow**: Essential tools (Read, Write, Edit, Bash, Web tools)
- **Ask**: Dangerous operations (rm, sudo, ssh, docker, etc.)
- **Deny**: Secret files (keys, certificates, SSH)

Adjust in `/permissions` if needed for your workflow.

## Components

| Component | Count | Description |
|-----------|-------|-------------|
| Commands | 7 | Daily planning, version control, productivity |
| Agents | 1 | Readwise highlight ingestion |
| Skills | 0 | Commands are self-contained |
| Hooks | 0 | No event-driven automation |
| MCP | 0 | Optional Google Calendar integration |
| Settings | ✓ | Pre-configured permissions |

## Requirements

- Claude Code 2.0+
- (Optional) Google Calendar MCP for calendar integration

## What's Included

```
human-general-intelligence/
├── .claude-plugin/
│   ├── plugin.json               # Plugin manifest
│   └── settings.json             # Permission rules
├── commands/                      # 7 workflow commands
│   ├── follow-plan.md
│   ├── git-commit.md
│   ├── git-summary.md
│   ├── handoff.md
│   ├── multi-perspective-review.md
│   ├── today.md
│   └── token-shortener.md
└── agents/                        # Specialized agents
    └── readwise-highlight-ingester.md
```

## Usage Examples

### Daily Planning
```
/today                    # Start daily planning
/today 2025-12-25        # Plan for specific date
```

### Git Workflow
```
/git-summary             # Check repo status
/git-commit              # Create commit
```

### Code Review
```
/multi-perspective-review    # Multi-angle code review
```

### Readwise Integration
```
@readwise-highlight-ingester
https://readwise.io/reader/shared/01HQ...
```

## License

MIT

## Author

Chu Yeow
