# human-general-intelligence

Personal workflow toolkit marketplace for Claude Code, featuring commands for planning, version control, session management, and productivity tools.

## Available Plugins

### human-general-intelligence (v0.1.0)

Personal workflow toolkit with 7 commands and 1 agent for enhancing your Claude Code experience.

**Features:**
- 7 productivity commands (planning, git, code review, daily planning, token optimization)
- 1 specialized agent (Readwise highlight ingestion)
- Pre-configured permissions for safe operation
- Optional Google Calendar integration

See the [plugin README](plugins/human-general-intelligence/README.md) for detailed feature descriptions.

## Installation

### Via GitHub

```bash
claude plugin marketplace add chuyeow/human-general-intelligence
claude plugin install human-general-intelligence@human-general-intelligence
```

### Via Local Path

```bash
claude plugin marketplace add /path/to/human-general-intelligence
claude plugin install human-general-intelligence@human-general-intelligence
```

### Update Marketplace

To get the latest plugin versions:

```bash
claude plugin marketplace update human-general-intelligence
```

## Quick Start

After installation, you'll have access to:

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

## Marketplace Structure

```
human-general-intelligence/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace catalog
├── plugins/
│   └── human-general-intelligence/
│       ├── .claude-plugin/
│       │   ├── plugin.json       # Plugin manifest
│       │   └── settings.json     # Permission rules
│       ├── commands/             # 7 workflow commands
│       ├── agents/               # Specialized agents
│       └── README.md             # Plugin documentation
└── README.md                      # This file
```

## Migration from Standalone Plugin

If you previously installed this as a standalone plugin, you'll need to reinstall using the marketplace format:

```bash
# Uninstall old version
claude plugin uninstall human-general-intelligence

# Install from marketplace
claude plugin marketplace add chuyeow/human-general-intelligence
claude plugin install human-general-intelligence@human-general-intelligence
```

All commands and functionality remain the same - only the installation method has changed.

## Requirements

- Claude Code 2.0+
- (Optional) Google Calendar MCP server for calendar integration in `/today` command

## License

MIT

## Author

Cheah Chu Yeow (chuyeow@gmail.com)

## Links

- [GitHub Repository](https://github.com/chuyeow/human-general-intelligence)
- [Plugin Documentation](plugins/human-general-intelligence/README.md)
