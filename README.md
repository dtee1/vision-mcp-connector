# vision-mcp-connector
Local MCP connector for Claude Deskttop to discover, control, and stream from GigE Vision cameras with beginner-focused GenICam support. 

## Status
Early-stage public learning project. The goal is to build this connector in a deliberate, educational way with clear architecture, disciplined commits, and minimal MVP scope.

## MVP Scope

Version 0 focuses on the smallest useful slice:

- Scan for GigE Vision devices on the local network
- Connect to one device
- Start streaming
- Stop streaming
- Expose only beginner-level GenICam features
- Support one camera at a time
- GigE Vision only for the initial MVP

Out of scope for the first version:

- USB3 Vision
- Multi-camera support
- Full GenICam feature coverage
- Recording workflows
- Production-grade UI
- Advanced diagnostics beyond basic connection and stream state

## Architecture

This project is split into two main layers:

- `connector-cpp/`: local C++ connector responsible for GigE discovery, control, stream handling, and GenICam interaction
- `mcp-server-ts/`: TypeScript MCP server that exposes connector capabilities to Claude Desktop

Planned flow:

1. Claude Desktop calls MCP tools
2. MCP server forwards requests to the local connector
3. Connector scans, connects, configures, and streams from the camera
4. Results and state are returned back through MCP

## Tech Stack

- C++20
- CMake
- TypeScript
- Node.js
- Claude Desktop MCP integration

## Learning Workflow

This project is intentionally being built as a learning process, not an autopilot AI build.

Development is guided by the following rules:

- Understand each subsystem before implementing it
- Build in small milestones
- Prefer short readings, quizzes, and small coding tasks
- Keep the human actively writing code
- Use AI as a mentor, reviewer, and explainer rather than a blind code generator

## Repository Structure

Current tracked structure:

    vision-mcp-connector/
      docs/

Planned top-level directories (will appear as the MVP is implemented): `connector-cpp/`, `mcp-server-ts/`, and `extension/`.

## Roadmap

### Phase 1
- Repository bootstrap
- Architecture notes
- C++ GigE discovery prototype

### Phase 2
- Single-device connection flow
- Beginner GenICam feature listing and read/write

### Phase 3
- Stream start/stop
- Basic frame acquisition and state reporting

### Phase 4
- MCP tool exposure
- Claude Desktop local integration

## Contributing

This repository follows a disciplined workflow for public development:

- Small, atomic commits
- Conventional Commits
- Feature branches for all changes
- Architecture-first development for major features

See `CONTRIBUTING.md` for details.

## License

Licensed under Apache License 2.0. See `LICENSE` and `NOTICE`.