# Architecture

## Goal

Build a lightweight local connector for Claude Desktop that can discover a GigE Vision camera, connect to it, start streaming, stop streaming, and expose beginner-focused GenICam functionality.

## MVP Layers

- **Connector (C++)**: handles GigE discovery, control, stream lifecycle, and GenICam interaction
- **MCP Server (TypeScript)**: exposes tool interfaces to Claude Desktop
- **Claude Desktop**: user-facing orchestration layer

## Initial Scope

- GigE only
- One device at a time
- Scan, connect, start stream, stop stream
- Beginner GenICam only

## Planned Flow

1. User asks Claude to scan for devices
2. MCP server calls local connector
3. Connector performs discovery and returns devices
4. User selects a device
5. Connector opens control connection
6. User starts stream
7. Connector manages stream state and reports status