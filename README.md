# wecode

Language / 语言: **[English (Default)](#english-default)** | [中文](#中文)

<div align="center">

[![Release](https://img.shields.io/github/v/release/wmjwmj100/wecode?label=release)](https://github.com/wmjwmj100/wecode/releases)
[![Platform](https://img.shields.io/badge/platform-Windows%20x64-2d6cdf)](https://github.com/wmjwmj100/wecode/releases)
[![Architecture](https://img.shields.io/badge/architecture-Multi--Agent-0f766e)](#what-makes-wecode-different)
[![Benchmark](https://img.shields.io/badge/self--eval-79.20-1d4ed8)](#benchmark-snapshot)

Multi-agent coding on Codex, upgraded for high-throughput collaboration.

[Download Binary](https://github.com/wmjwmj100/wecode/releases) • [Benchmark](#benchmark-snapshot) • [Roadmap](#roadmap)

</div>

---

## English (Default)

### Product Positioning

wecode is a multi-agent coding system built on Codex for teams that care about execution speed, collaboration quality, and delivery stability.

This project does **not** follow a fixed workflow template. Instead, we use **MARL (Multi-Agent Reinforcement Learning)** to strengthen agent-to-agent coordination so collaboration can adapt to task context in real time.

### What Makes wecode Different

- **MARL-enhanced collaboration:** reinforcement learning improves cross-agent decision quality and coordination efficiency.
- **Full-connectivity communication:** agents can exchange context directly instead of operating as isolated workers.
- **Society-inspired cooperation:** collaboration behavior is designed to resemble human-team dynamics: division of labor, synchronization, feedback, and correction.
- **Operator-visible process:** debug traces and role-based views make collaboration readable during parallel execution.

### Benchmark Snapshot

The table below includes models visible in shared snapshots and self-evaluated entries that are not yet officially listed.

| Model | % Resolved |
|---|---:|
| Sonnet 4.6 | 79.60 |
| wecode (multi-agent, based on Codex) | 79.20 |
| live-SWE-agent + Claude 4.5 Opus medium (20251101) | 79.20 |
| Sonar Foundation Agent + Claude 4.5 Opus | 79.20 |
| TRAE + Doubao-Seed-Code | 78.80 |
| live-SWE-agent + Gemini 3 Pro Preview (2025-11-18) | 77.40 |
| Atlassian Rovo Dev (2025-09-02) | 76.80 |
| EPAM AI/Run Developer Agent v20250719 + Claude 4 Sonnet | 76.80 |
| mini-SWE-agent + Claude 4.5 Opus (high reasoning) | 76.80 |
| ACoder | 76.40 |
| mini-SWE-agent + Gemini 3 Flash (high reasoning) | 75.80 |

### Roadmap

Next, we will extend the multi-agent collaboration engine into **financial-domain scenarios**, focusing on higher-reliability collaboration for analysis-heavy and decision-sensitive tasks.

### Quick Start

```powershell
# 1) Download the latest Windows binary from Releases
# 2) Run wecode
.\wecode-windows-x64.exe
# 3) Start with a concrete engineering goal
```

### Release

- GitHub Releases: `https://github.com/wmjwmj100/wecode/releases`

---

## 中文

### 产品定位

wecode 是一个基于 Codex 的多智能体编程系统，面向追求执行效率、协作质量与交付稳定性的工程团队。

我们**不采用固定工作流模板**。相反，我们通过 **MARL（多智能体强化学习）** 增强智能体间协作能力，使协同方式能够根据任务上下文实时自适应。

### wecode 的核心差异

- **MARL 强化协作：** 通过强化学习持续优化跨智能体决策与协同效率。
- **全连接通信：** 智能体之间可以直接交换上下文，而不是孤立执行。
- **类人类社会协作：** 协作模式更接近真实人类团队，包括分工、同步、反馈与纠偏。
- **过程可见：** 在并行执行下可通过调试轨迹与角色视图清晰观察协作过程。

### 榜单快照

下表包含截图中可见条目，以及尚未进入官方榜单的自测结果。

| 模型 | 任务解决率 |
|---|---:|
| Sonnet 4.6 | 79.60 |
| wecode（基于 Codex 的多智能体） | 79.20 |

### 路线图

下一步我们将把多智能体协作能力扩展到**金融领域**，面向分析密集、决策敏感场景提升协作可靠性。

### 快速开始

```powershell
# 1) 从 Releases 下载最新 Windows 二进制
# 2) 启动 wecode
.\wecode-windows-x64.exe
# 3) 输入明确的工程目标开始使用
```

### 发布信息

- GitHub Releases：`https://github.com/wmjwmj100/wecode/releases`

---

> Note: Internal implementation details remain high-level in this public repository.
