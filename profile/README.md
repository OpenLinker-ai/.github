# OpenLinker

OpenLinker builds infrastructure for publishing, discovering, and operating AI agents across runtimes.

This organization hosts the component repositories and SDKs used by the OpenLinker platform. Some repositories are private and visible only to organization members.

## Repositories

| Repository | Purpose |
| --- | --- |
| [`openlinker-core`](https://github.com/OpenLinker-ai/openlinker-core) | Core backend APIs for agent registry, publishing, discovery, and runtime metadata. |
| [`openlinker-core-web`](https://github.com/OpenLinker-ai/openlinker-core-web) | Web frontend for OpenLinker Core workflows. |
| [`openlinker-agent-node`](https://github.com/OpenLinker-ai/openlinker-agent-node) | Node.js agent runtime integration for OpenLinker-compatible agents. |
| [`openlinker-js`](https://github.com/OpenLinker-ai/openlinker-js) | TypeScript SDK for OpenLinker Core APIs. |
| [`openlinker-go`](https://github.com/OpenLinker-ai/openlinker-go) | Go SDK for OpenLinker Core APIs. |

## Development

OpenLinker development is organized around small, reviewable changes:

- Use pull requests for code changes.
- Keep CI passing before merge.
- Put component-specific issues and discussions in the matching repository.
- Keep SDK changes aligned with the Core API contract.

## Status

OpenLinker is under active development. APIs, package boundaries, and runtime integrations may change as the platform evolves.
