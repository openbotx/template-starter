# Agents

## Main Agent

The main agent handles all conversations. It has full access to tools and workspace.

## Subagents

Subagents are spawned via the `spawn` tool for background tasks. They have restricted access:

- File operations (read, write, edit, list)
- Shell execution
- Web search and fetch
- HTTP client (with auth profiles)
- RSS reader
- Image generation

Subagents cannot: send messages to the user, spawn other subagents, manage cron jobs, or access memory tools.
