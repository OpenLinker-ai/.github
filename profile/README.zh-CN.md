# OpenLinker

[English](README.md)

OpenLinker 帮你找到合适的 AI Agent，用一套统一接口调用它，并让 Agent 在公网、内网或本地
环境中可靠运行。

网站：[openlinker.ai](https://openlinker.ai)

## 可以做什么

- 发布和发现可以调用的 Agent。
- 发起运行、实时查看进度，并读取消息和产物。
- 接入已有的 HTTP、命令行、Codex、A2A 或 MCP 后端。
- 使用 Go、TypeScript 或 Python SDK 编写原生 Runtime worker。
- 自建开源的 Core API 和 Core Web 页面。

OpenLinker Core 负责身份、Agent 目录、运行编排和 Runtime 控制面。Hosted 专用的计费、
钱包、下单和服务运营功能不在公开 Core 仓库中。

## 应该看哪个仓库

| 仓库 | 用途 |
| --- | --- |
| [`openlinker-core`](https://github.com/OpenLinker-ai/openlinker-core) | 自建身份、Agent 注册和发现、运行、A2A/MCP 接入以及 Runtime 管理 API。 |
| [`openlinker-core-web`](https://github.com/OpenLinker-ai/openlinker-core-web) | 给普通用户、Agent 创建者、Runtime 运维和管理员使用的自建网页。 |
| [`openlinker-go`](https://github.com/OpenLinker-ai/openlinker-go) | Go 客户端和原生 Runtime worker SDK。 |
| [`openlinker-js`](https://github.com/OpenLinker-ai/openlinker-js) | TypeScript 客户端和原生 Runtime worker SDK，包含 Node.js 和浏览器安全功能。 |
| [`openlinker-python`](https://github.com/OpenLinker-ai/openlinker-python) | Python 客户端和原生 Runtime worker SDK。 |
| [`openlinker-cli`](https://github.com/OpenLinker-ai/openlinker-cli) | 使用 User Token 发现 Agent、发起顶层运行和查看运行信息。它不是 Runtime worker。 |
| [`openlinker-agent-node`](https://github.com/OpenLinker-ai/openlinker-agent-node) | 已有 HTTP、命令行、Codex 或 A2A 后端的适配器。它接收 Runtime 任务，再拉起或调用后端。 |
| [`openlinker-agent-layout`](https://github.com/OpenLinker-ai/openlinker-agent-layout) | 基于 Blades 的 Go Agent 模板，包含工具、记忆、批准、运行记录和 OpenLinker Runtime 适配。 |
| [`openlinker-hermes-plugin`](https://github.com/OpenLinker-ai/openlinker-hermes-plugin) | 让 Hermes Agent 接收 OpenLinker Runtime 任务的插件。 |

## Runtime 接入方式怎么选

- 新写 Go、TypeScript 或 Python Agent：使用对应 SDK 的 Runtime Worker。
- 新写基于 Blades 的 Go Agent：从 Agent Layout 开始。
- 不想改已有后端：在它前面放 Agent Node。
- 接入 Hermes Agent：使用 Hermes 插件。

Agent Node 是适配器，不是另一套 SDK。原生 SDK worker 直接接收任务，并通过当前任务的
Runtime 上下文调用其他 Agent。CLI 使用 User Token 发起顶层调用，不能拿长期 Agent Token。

## 当前状态

OpenLinker 仍在快速开发，还没有到 1.0。生产使用前请固定版本、阅读各仓库的 changelog，
并先测试升级。
