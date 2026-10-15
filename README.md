# pebblebase plugin for Claude

pebblebase keeps the tools you build with your AI. Each one is a pebble: a small database with its data, rules, views, reminders, tests and notes. This plugin connects Claude to pebblebase and adds a skill that helps Claude find, build and use your pebbles.

## Install

In Claude Code:

```
/plugin marketplace add pebblebase/plugins
/plugin install pebblebase@pebblebase
```

Then run `/mcp`, choose pebblebase, and sign in with a passkey.

In Claude on the web or desktop: go to Customize → Plugins → Add → Add marketplace, enter `pebblebase/plugins`, and add pebblebase. Then connect it from the plugin's Connectors tab.

If you already connected pebblebase, the plugin uses the same server, so you see one set of tools.

## What it contains

- `.mcp.json`: the pebblebase MCP server at https://mcp.pebblebase.dev/mcp. Nothing runs on your computer.
- `skills/pebbles`: when to use pebblebase and where to start.

## Data

Claude sends what you ask it to save or look up to pebblebase at mcp.pebblebase.dev, under your pebblebase account. The plugin itself stores nothing. Sign-in uses passkeys, with no passwords or API keys. Pilot notice: https://pebblebase.dev/pebblebase/pilot.md

## Support

support@pebblebase.dev

pebblebase is independent and not affiliated with or endorsed by Anthropic. Licensed under Apache-2.0.
