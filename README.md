# wecode

<div align="center">

[![Release](https://img.shields.io/github/v/release/wmjwmj100/wecode?label=release)](https://github.com/wmjwmj100/wecode/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%20x64-2d6cdf)](https://github.com/wmjwmj100/wecode/releases)
[![Architecture](https://img.shields.io/badge/architecture-Multi--Agent-0f766e)](#collaboration-advantages--多智能体协作优势)
[![Benchmark](https://img.shields.io/badge/self--eval-79.20-1d4ed8)](#benchmark-board-snapshot--unlisted-results--榜单快照含未上榜自测)

**EN**: A multi-agent coding assistant built on Codex for high-speed engineering collaboration.  
**中文**：基于 Codex 的多智能体编程助手，面向高效率工程协作。

<br/>

[Download Binary](https://github.com/wmjwmj100/wecode/releases) •
[Benchmark Board](#benchmark-board-snapshot--unlisted-results--榜单快照含未上榜自测) •
[Collaboration Advantages](#collaboration-advantages--多智能体协作优势)

</div>

---

## Product Highlights | 产品亮点

**EN**
- Built for production-style engineering collaboration instead of single-thread assistant workflows.
- Emphasizes agent-to-agent communication quality, coordinated execution, and delivery throughput.
- Provides a clear operator-facing view of collaboration progress and task state.

**中文**
- 面向工程化协作场景，而不是单线程助手式工作流。
- 强调智能体之间的交流质量、协同执行效率与整体交付吞吐。
- 提供面向操作者的协作过程可见性与任务状态清晰度。

## Quick Start | 快速开始

```powershell
# 1) Download the latest Windows binary from Releases
#    从 Releases 下载最新 Windows 二进制

# 2) Run wecode
#    运行 wecode
.\wecode-windows-x64.exe

# 3) Start with a concrete engineering task
#    直接给出明确工程任务开始使用
```

## Overview | 项目概述

**EN**  
wecode is a multi-agent coding system designed for engineering teams that need speed, coordination, and execution quality at the same time. Instead of a single-threaded assistant workflow, wecode enables multiple agents to collaborate in parallel under one shared objective.

**中文**  
wecode 是一个多智能体编程协作系统，面向追求效率、协同与交付质量的工程团队。它不再依赖单智能体串行执行，而是让多个智能体围绕同一目标并行协作。

## Why wecode | 为什么是 wecode

| Capability | Value |
|---|---|
| Full-connectivity collaboration | Agents can communicate and coordinate across tasks rather than staying isolated. |
| Self-organization | Collaboration patterns can adjust dynamically based on task state and progress. |
| Parallel execution | Complex work can be decomposed and executed concurrently to reduce end-to-end latency. |
| Human-visible coordination | Collaboration progress and agent activity can be surfaced for operational clarity. |

| 能力 | 价值 |
|---|---|
| 全连接协作 | 智能体之间可跨任务协同，不是信息孤岛。 |
| 自组织协作 | 协作模式会根据任务状态动态调整。 |
| 并行执行 | 复杂任务可拆解并并发推进，缩短整体交付时间。 |
| 可观测协同 | 协作过程可被清晰展示，便于管理与回溯。 |

## Collaboration Advantages | 多智能体协作优势

1. **Task-level parallelism / 任务级并行**  
   Multiple task streams can run simultaneously, while preserving shared context and goal alignment.
2. **Coordination over isolation / 协同优先于孤立执行**  
   Agents are designed to coordinate decisions, dependencies, and handoffs in real time.
3. **Adaptive routing / 动态协作路由**  
   Work can be redistributed as context changes, improving resilience under uncertainty.
4. **Execution transparency / 过程透明可见**  
   Teams can inspect collaboration progress instead of treating agent behavior as a black box.

## Benchmark Board (Snapshot + Unlisted Results) | 榜单快照（含未上榜自测）

The board below combines:
- Official leaderboard entries visible in shared snapshots.
- Additional self-evaluated entries that are **not yet listed** on the official board.

下表同时包含：
- 截图中可见的官方榜单条目。
- **尚未上官方榜单** 的自测结果。

| Model | % Resolved |
|---|---:|
| Sonnet 4.6 | 79.60 |
| wecode (multi-agent, based on GPT 5.2) | 79.20 |
| live-SWE-agent + Claude 4.5 Opus medium (20251101) | 79.20 |
| Sonar Foundation Agent + Claude 4.5 Opus | 79.20 |
| TRAE + Doubao-Seed-Code | 78.80 |
| live-SWE-agent + Gemini 3 Pro Preview (2025-11-18) | 77.40 |
| Atlassian Rovo Dev (2025-09-02) | 76.80 |
| EPAM AI/Run Developer Agent v20250719 + Claude 4 Sonnet | 76.80 |
| mini-SWE-agent + Claude 4.5 Opus (high reasoning) | 76.80 |
| ACoder | 76.40 |
| mini-SWE-agent + Gemini 3 Flash (high reasoning) | 75.80 |

## Release | 二进制发布

- GitHub Releases: `https://github.com/wmjwmj100/wecode/releases`
- Latest Windows binary package is published as release assets.

---

> Note / 说明：This repository intentionally keeps internal architecture details high-level.
