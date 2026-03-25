# cc-market

A plugin marketplace for [Claude Code](https://claude.ai/claude-code), providing a structured way to discover, distribute, and install custom skills.

## Overview

cc-market organizes Claude Code plugins into a **marketplace** — a curated collection of plugins, each containing one or more **skills** (custom slash commands).

## Structure

```
cc-market/
├── .claude-plugin/
│   └── marketplace.json        # Marketplace manifest
└── plugins/                    # All plugins live here
    └── quality-review-plugin/  # An individual plugin
        ├── .claude-plugin/
        │   └── plugin.json     # Plugin metadata
        └── skills/
            └── quality-review/
                └── SKILL.md    # Skill definition & prompt
```

### Key concepts

| Concept | Description |
|---|---|
| **Marketplace** | A named collection of plugins, defined by `marketplace.json` |
| **Plugin** | A packaged unit with metadata (`plugin.json`) and one or more skills |
| **Skill** | A slash command backed by a prompt template in `SKILL.md` |

## Available plugins

| Plugin | Skill | Description |
|---|---|---|
| `quality-review-plugin` | `/quality-review` | Review code for bugs, security, and performance |
| `quality-review-plugin` | `/commit-message` | Generate a conventional commit message from staged changes |

## Adding a plugin

1. Create a directory at `plugins/<your-plugin-name>/`
2. Add `.claude-plugin/plugin.json` with `name`, `description`, and `version`
3. Add one or more skills under `skills/<skill-name>/SKILL.md`
4. Register the plugin in `.claude-plugin/marketplace.json`

### `plugin.json` format

```json
{
  "name": "my-plugin",
  "description": "What this plugin does",
  "version": "1.0.0"
}
```

### `SKILL.md` format

```markdown
---
name: my-skill
description: Short description shown in /help
---

Your prompt template here. Claude will execute this when the user runs /my-skill.
```

### `marketplace.json` format

```json
{
  "name": "forge",
  "owner": { "name": "Your Name" },
  "plugins": [
    {
      "name": "my-plugin",
      "source": "./plugins/my-plugin",
      "description": "What this plugin does"
    }
  ]
}
```
