# pebblebase plugin

pebblebase keeps the tools you build with your AI. Each one is a pebble: a small database with its data, rules, views, reminders, tests and notes. This plugin connects your AI app to pebblebase and adds a skill that helps it find, build and use your pebbles. It's packaged for Claude, Cursor and Grok Bot.

## Install

### Claude

In Claude Code:

```
/plugin marketplace add pebblebase/plugins
/plugin install pebblebase@pebblebase
```

Then run `/mcp`, choose pebblebase, and sign in with a passkey.

In Claude on the web or desktop: go to Customize → Plugins → Add → Add marketplace, enter `pebblebase/plugins`, and add pebblebase. Then connect it from the plugin's Connectors tab.

If you already connected pebblebase, the plugin uses the same server, so you see one set of tools.

### Cursor

Not yet tested. pebblebase isn't in the Cursor Marketplace yet. Until it is, paste this link into your browser, confirm in Cursor, and sign in with a passkey when asked:

```
cursor://anysphere.cursor-deeplink/mcp/install?name=pebblebase&config=eyJ1cmwiOiJodHRwczovL21jcC5wZWJibGViYXNlLmRldi9tY3AifQ==
```

This adds the pebblebase server without the skill. On a Cursor Teams or Enterprise plan, an admin can add the whole plugin for the team: Dashboard → Plugins & MCPs → Team Marketplaces → Add Marketplace → Import from Repo, with `https://github.com/pebblebase/plugins`.

### Grok Bot

Not yet tested. Grok Bot adds plugins from the Cursor Marketplace, under Connect apps in its sidebar, and pebblebase isn't listed there yet. If you use Grok Bot through a Cursor team, your admin can add pebblebase to the team marketplace, as described under Cursor.

## What it contains

- `.claude-plugin/`: the Claude plugin and marketplace manifests. Grok Build reads these too, in place of its own `.grok-plugin/` manifests.
- `.cursor-plugin/`: the Cursor plugin and marketplace manifests, used by Cursor and Grok Bot.
- `.mcp.json` (Claude) and `mcp.json` (Cursor): the same pebblebase MCP server at https://mcp.pebblebase.dev/mcp. Nothing runs on your computer.
- `skills/pebbles`: when to use pebblebase and where to start. Every app uses the same skill.
- `assets/logo.svg`: the pebblebase logo.

## Data

Your AI app sends what you ask it to save or look up to pebblebase at mcp.pebblebase.dev, under your pebblebase account. The plugin itself stores nothing. Sign-in uses passkeys, with no passwords or API keys. Pilot notice: https://pebblebase.dev/pebblebase/pilot.md

## Support

support@pebblebase.dev

pebblebase is independent and not affiliated with or endorsed by Anthropic, Anysphere (Cursor) or xAI. Licensed under Apache-2.0.
