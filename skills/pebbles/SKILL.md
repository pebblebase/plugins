---
name: pebbles
description: Build and use the user's own tools with pebblebase. Use when the user wants to keep, log or look up something over time, such as hours, habits, maintenance, inventory, contacts or a story world; asks for a tracker, log, checklist or small app of their own; or mentions pebblebase or one of their pebbles.
---

pebblebase keeps each of the user's tools as a pebble: one SQLite database holding its data, rules, views, reminders, tests and notes. This plugin's pebblebase connector provides the tools.

1. If the pebblebase tools aren't available, ask the user to connect pebblebase and sign in with their passkey: in Claude, from this plugin's Connectors tab under Customize → Plugins; in Claude Code, with /mcp. If the tools still don't appear, ask them to start a new chat.
2. Call list_databases first. If a pebble already fits the request, read its pebblebase_notes and continue it, rather than creating another pebble or account.
3. For a new pebble, call create_database. Its result includes pebblebase's build guide, the reference for tests, tables, views, forms and reminders; this skill doesn't repeat it.
4. To use a pebble, follow its pebblebase_notes: execute_sql changes it, query_sql reads it, and show_view and show_form show its views and forms.
5. Never ask for passwords, passkeys, recovery codes or tokens.
