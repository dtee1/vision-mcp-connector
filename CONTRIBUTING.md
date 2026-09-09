# Contributing

Thanks for your interest in contributing to `vision-mcp-connector`.

## Development Principles

This project is intentionally developed as a public learning-oriented engineering project with high standards for clarity, structure, and trust.

Key principles:

- Keep changes small and focused
- Prefer clarity over cleverness
- Explain architectural decisions
- Avoid large unreviewable code dumps
- Document tradeoffs and assumptions
- Build the MVP before expanding scope

## Branch Strategy

Do not commit directly to `main`.

Use topic branches:

- `docs/...` for documentation work
- `feat/...` for new features
- `fix/...` for bug fixes
- `chore/...` for maintenance and tooling
- `refactor/...` for internal cleanup without behavior change

Examples:

- `docs/project-bootstrap`
- `feat/gige-discovery`
- `feat/device-connect`
- `feat/stream-start-stop`
- `chore/cmake-bootstrap`

## Commit Style

This repository uses Conventional Commits.

Examples:

- `docs(readme): define MVP scope`
- `chore(repo): add editorconfig and gitignore`
- `feat(connector): add GigE discovery skeleton`
- `feat(mcp): add scan_devices tool schema`
- `fix(connector): handle socket timeout during discovery`

Guidelines:

- Use the imperative mood
- Keep subject lines concise
- Make each commit do one thing
- Add a body when the reasoning matters

## Pull Requests

Pull requests should:

- Have a narrow scope
- Explain what changed
- Explain why the change is needed
- Note any follow-up work
- Avoid mixing docs, refactors, and feature work unless tightly related

## Coding Expectations

For now, contributors should favor:

- Minimal dependencies
- Readable code
- Small modules
- Straightforward interfaces
- Clear error handling
- Incremental progress over premature abstraction

## Early MVP Constraints

Until the MVP is complete, contributions should stay aligned with the following limits:

- GigE Vision only
- One camera at a time
- Beginner GenICam features only
- Minimal scan/connect/start/stop functionality

Anything outside this scope should be discussed first.

## Questions and Discussion

If a contribution changes architecture, protocol boundaries, or public interfaces, document the reasoning in `docs/` before or alongside implementation.