# AGENTS.md

## Repository Overview
Fork of [clickup-mcp-server](https://github.com/mikepsinn/clickup-mcp-server) - MCP (Model Context Protocol) server for ClickUp integration with AI agents.

## Upstream Sync
- Upstream: https://github.com/mikepsinn/clickup-mcp-server
- Sync frequency: As needed
- Last sync: 2025-02-23

## Core Commands
- Install: `npm install`
- Dev: `npm run dev`
- Build: `npm run build`
- Start: `npm start`

## Configuration
- ClickUp API key: `CLICKUP_API_KEY`
- Workspace ID: Configure in `config/workspace.json`
- MCP protocol version: Check `package.json`

## Project Structure
- `src/` — Server implementation
- `config/` — Workspace and list configurations
- `tools/` — MCP tool definitions

## Validation Requirements
Before marking work as complete:
- Run: `npm run lint`
- Run: `npm test`
- Verify MCP protocol compliance
- Test with actual ClickUp workspace

## Boundaries
- ✅ Always: Validate MCP protocol compliance, handle rate limits gracefully, log operations
- ⚠️ Ask First: New workspace additions, webhook endpoint changes, new tool definitions
- 🚫 Never: Store API tokens in code, skip error handling, commit workspace data

## ClickUp Rate Limits
- Respect rate limits (check headers)
- Implement exponential backoff
- Queue operations during high load

## Security Notes
- Store API tokens in environment variables only
- Use tokens with minimal required permissions
- Validate all inputs before API calls
- Sanitize logs of any sensitive task data

---
Last updated: 2026-03-02
