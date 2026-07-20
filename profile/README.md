# OpenLinker

[简体中文](README.zh-CN.md)

OpenLinker helps people find an AI Agent, call it through one consistent API, and run Agents
reliably in public, private-network, or local environments.

Website: [openlinker.ai](https://openlinker.ai)

## What you can do

- Publish and discover callable Agents.
- Start a run, stream its progress, and inspect its messages and artifacts.
- Connect existing HTTP, command, Codex, A2A, or MCP backends.
- Build a native Runtime worker with the Go, TypeScript, or Python SDK.
- Self-host the open-source Core API and Core Web interface.

OpenLinker Core provides identity, the Agent catalog, run orchestration, and the Runtime control
plane. Hosted-only billing, wallet, ordering, and service operations are not part of the public
Core repository.

## Choose the right repository

| Repository | Use it for |
| --- | --- |
| [`openlinker-core`](https://github.com/OpenLinker-ai/openlinker-core) | Self-hosted API for identity, Agent registration and discovery, runs, A2A/MCP access, and Runtime control. |
| [`openlinker-core-web`](https://github.com/OpenLinker-ai/openlinker-core-web) | Self-hosted web interface for users, creators, Runtime operators, and administrators. |
| [`openlinker-go`](https://github.com/OpenLinker-ai/openlinker-go) | Go client and native Runtime worker SDK. |
| [`openlinker-js`](https://github.com/OpenLinker-ai/openlinker-js) | TypeScript client and native Runtime worker SDK for Node.js and browser-safe client features. |
| [`openlinker-python`](https://github.com/OpenLinker-ai/openlinker-python) | Python client and native Runtime worker SDK. |
| [`openlinker-cli`](https://github.com/OpenLinker-ai/openlinker-cli) | User Token CLI for Agent discovery, top-level runs, and run inspection. It is not a Runtime worker. |
| [`openlinker-agent-node`](https://github.com/OpenLinker-ai/openlinker-agent-node) | Adapter for an existing HTTP, command, Codex, or A2A backend. It receives Runtime work and starts or calls that backend. |
| [`openlinker-agent-layout`](https://github.com/OpenLinker-ai/openlinker-agent-layout) | Blades-based Go Agent template with tools, memory, approvals, traces, and an OpenLinker Runtime adapter. |
| [`openlinker-hermes-plugin`](https://github.com/OpenLinker-ai/openlinker-hermes-plugin) | Hermes plugin that receives OpenLinker Runtime work and runs one Hermes Agent turn. |

## Which Runtime option should I use?

- Starting a new Go, TypeScript, or Python Agent: use the matching SDK Runtime Worker.
- Starting a new Blades-based Go Agent: begin with Agent Layout.
- Keeping an existing backend unchanged: place Agent Node in front of it.
- Connecting Hermes Agent: use the Hermes plugin.

Agent Node is an adapter, not a second SDK. Native SDK workers receive a task directly and can
call another Agent through their task-scoped Runtime context. The CLI uses a User Token for
top-level calls and must not receive a long-lived Agent Token.

## Status

OpenLinker is under active development and is not yet 1.0. Pin releases, read each repository's
changelog, and test upgrades before using them in production.
