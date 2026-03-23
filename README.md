# wecode

<div align="center">

**EN**: A multi-agent coding assistant built on Codex for high-speed engineering collaboration.  
**中文**：基于 Codex 的多智能体编程助手，面向高效率工程协作。

</div>

---

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

## Typical Workflow | 典型工作流

1. Define the engineering goal and constraints.  
   明确目标与约束。  
2. Split work into parallelizable units.  
   拆分可并行任务。  
3. Let agents collaborate and synchronize on dependencies.  
   智能体并行执行并同步依赖。  
4. Merge outcomes into a single delivery result.  
   汇总结果并完成交付。  

## Benchmark Board (Snapshot + Unlisted Results) | 榜单快照（含未上榜自测）

The board below combines:
- Official leaderboard entries visible in shared snapshots.
- Additional self-evaluated entries that are **not yet listed** on the official board.

下表同时包含：
- 截图中可见的官方榜单条目。
- **尚未上官方榜单** 的自测结果。

| Model | % Resolved | Source | Official Board Status |
|---|---:|---|---|
| Sonnet 4.6 | 79.60 | Self-evaluated | Not listed on official board |
| wecode (multi-agent, based on Codex) | 79.20 | Self-evaluated | Not listed on official board |
| live-SWE-agent + Claude 4.5 Opus medium (20251101) | 79.20 | Official snapshot | Listed |
| Sonar Foundation Agent + Claude 4.5 Opus | 79.20 | Official snapshot | Listed |
| TRAE + Doubao-Seed-Code | 78.80 | Official snapshot | Listed |
| live-SWE-agent + Gemini 3 Pro Preview (2025-11-18) | 77.40 | Official snapshot | Listed |
| Atlassian Rovo Dev (2025-09-02) | 76.80 | Official snapshot | Listed |
| EPAM AI/Run Developer Agent v20250719 + Claude 4 Sonnet | 76.80 | Official snapshot | Listed |
| mini-SWE-agent + Claude 4.5 Opus (high reasoning) | 76.80 | Official snapshot | Listed |
| ACoder | 76.40 | Official snapshot | Listed |
| mini-SWE-agent + Gemini 3 Flash (high reasoning) | 75.80 | Official snapshot | Listed |

## Release | 二进制发布

- GitHub Releases: `https://github.com/wmjwmj100/wecode/releases`
- Latest Windows binary package is published as release assets.

---

> Note / 说明：This repository intentionally keeps internal architecture details high-level.
