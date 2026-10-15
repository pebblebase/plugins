# pebblebase plugin

pebblebase keeps the tools you build with your AI. Each one is a pebble: a small database with its data, rules, views, reminders, tests and notes. This plugin connects your AI app to pebblebase and adds a skill that helps it find, build and use your pebbles. It works with Claude, Cursor and Grok Bot.

## Install

### Claude

In Claude Code:

```
/plugin marketplace add pebblebase/plugins
/plugin install pebblebase@pebblebase
```

Then run `/mcp`, choose pebblebase, and sign in with a passkey.

In Claude on the web or desktop: go to Customize → Plugins → Add → Add marketplace, enter `pebblebase/plugins`, and add pebblebase. Then connect it from the plugin's Connectors tab.

### Cursor

Once pebblebase is listed in the Cursor marketplace, install pebblebase from it. Until then, add the MCP URL https://mcp.pebblebase.dev/mcp as a custom connector and sign in with a passkey.

### Grok Bot

Grok Bot uses the Cursor marketplace. Once pebblebase is listed there, install pebblebase from it. Until then, add the MCP URL https://mcp.pebblebase.dev/mcp as a custom connector and sign in with a passkey.

If you already connected pebblebase, the plugin uses the same server, so you see one set of tools.

## What it contains

- `.claude-plugin/`: the Claude plugin and marketplace manifests. Grok Build reads these too.
- `.cursor-plugin/`: the Cursor plugin and marketplace manifests, used by Cursor and Grok Bot.
- `.mcp.json` (Claude) and `mcp.json` (Cursor): the same pebblebase MCP server at https://mcp.pebblebase.dev/mcp. Nothing runs on your computer.
- `skills/pebbles`: when to use pebblebase and where to start. Every app uses the same skill.
- `assets/logo.svg`: the pebblebase logo.

## Data

Your AI app sends what you ask it to save or look up to pebblebase at mcp.pebblebase.dev, under your pebblebase account. The plugin itself stores nothing. Sign-in uses passkeys, with no passwords or API keys. Pilot notice: https://pebblebase.dev/pebblebase/pilot.md

## Support

support@pebblebase.dev

pebblebase is independent and not affiliated with or endorsed by Anthropic, Anysphere (Cursor) or xAI. Licensed under Apache-2.0.
