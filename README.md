# wecode

Language / 语言: **English** | [中文速览](#chinese-summary)

<div align="center">
  <img src="./images/hero-banner.png" alt="WeCode hero banner" width="100%" />
  <br />
  <br />
  <a href="https://github.com/wmjwmj100/wecode/releases"><img src="https://img.shields.io/github/v/release/wmjwmj100/wecode?style=for-the-badge&logo=github&label=release" alt="Latest release" /></a>
  <a href="https://github.com/wmjwmj100/wecode"><img src="https://img.shields.io/github/stars/wmjwmj100/wecode?style=for-the-badge&logo=github&label=stars" alt="GitHub stars" /></a>
  <img src="https://img.shields.io/badge/swarm-multi--agent-0f766e?style=for-the-badge" alt="Swarm multi-agent" />
  <img src="https://img.shields.io/badge/platform-Windows%20x64-111827?style=for-the-badge" alt="Windows x64" />
  <img src="https://img.shields.io/badge/SWE--bench-79.20%25-1d4ed8?style=for-the-badge" alt="SWE-bench 79.20%" />
  <br />
  <br />
  <strong>Swarm-native coding on Codex.</strong>
  <br />
  WeCode runs multiple cooperating agents in parallel so exploration, review, and execution do not collapse into one brittle trace.
  <br />
  <br />
  <a href="https://github.com/wmjwmj100/wecode/releases">Download Binary</a>
  ·
  <a href="#why-swarm-not-one-agent">Why Swarm</a>
  ·
  <a href="#how-the-swarm-executes">Architecture</a>
  ·
  <a href="#benchmark-snapshot">Benchmark</a>
  ·
  <a href="#quick-start">Quick Start</a>
</div>

> README visuals are now sourced from the generated images in [`images/`](./images).

---

## Built For Hard Engineering Work

WeCode is a multi-agent coding system built on Codex for teams that care about execution speed, collaboration quality, and delivery stability. Instead of forcing one model to plan, inspect, code, test, and review in a single chain, WeCode lets a swarm of agents split the work, share memory, and cross-check each other before converging on an answer.

<table>
  <tr>
    <td width="33%" valign="top">
      <strong>Parallel reconnaissance</strong><br />
      Multiple agents inspect different parts of the codebase at the same time, which reduces blind spots and shortens time-to-context.
    </td>
    <td width="33%" valign="top">
      <strong>Shared working memory</strong><br />
      Findings are written into a common space so later agents can start from the current state of understanding instead of rebuilding it.
    </td>
    <td width="33%" valign="top">
      <strong>Cross-agent verification</strong><br />
      Agents challenge each other's assumptions before the final answer is produced, which makes long-horizon tasks more stable.
    </td>
  </tr>
</table>

## Why Swarm Not One Agent?

Most coding agents are still one model wearing many hats. That works for short, local edits, but performance degrades when the task becomes ambiguous, cross-cutting, or unfamiliar. WeCode is designed for the cases where a single uninterrupted reasoning trace is the failure mode.

| Problem Shape | Single-Agent Flow | WeCode Swarm |
|---|---|---|
| Small bug fix | Usually fast | Usually fast |
| Unknown codebase | Sequential exploration | Parallel repo reconnaissance |
| Multi-file refactor | Context becomes fragile | Agents divide scope and compare notes |
| Architecture change | One chain loses the thread | Shared memory preserves the big picture |
| Ambiguous requirement | First interpretation tends to stick | Disagreement surfaces early |

## How the Swarm Executes

<p align="center">
  <img src="./images/swarm-architecture.png" alt="Swarm architecture diagram" width="100%" />
</p>

1. **Split the search space.** Agents explore different files, hypotheses, and failure modes in parallel.
2. **Write to shared memory.** Useful findings are published so other agents can build on them immediately.
3. **Cross-check before converge.** Proposed fixes are challenged by peers instead of being accepted by default.
4. **Return one coherent result.** The user sees a single output backed by distributed investigation.

### Coordination Patterns We Care About

- **Spontaneous role division:** agents naturally specialize when duplicate work becomes wasteful.
- **Proactive unblocking:** one agent often provides missing context before another explicitly asks.
- **Self-correction through critique:** weak assumptions are more likely to be exposed before they reach the user.
- **Adaptive planning:** collaboration order emerges from the task instead of being hard-coded into a rigid pipeline.

## Observability

<p align="center">
  <img src="./images/observability.png" alt="Observability view" width="100%" />
</p>

WeCode is designed to make collaboration legible, not hidden. The current public presentation focuses on four things:

- **Per-agent timelines:** inspect what each agent was doing and when it switched focus.
- **Communication log:** see messages, blockers, and handoffs across the swarm.
- **Shared-memory snapshots:** understand what the colony collectively knew at each stage.
- **Replay-friendly traces:** reconstruct how the final answer emerged from parallel work.

<details>
  <summary><strong>Design note</strong></summary>

WeCode does not depend on a fixed planner-worker template. The coordination layer is closer to MARL-style adaptation: agents react to the changing task state, each other, and the shared workspace rather than obeying one pre-written script.

</details>

## Benchmark Snapshot

The table below keeps the public snapshot concise and clearly labels WeCode as a self-evaluated entry. The point is not only raw model quality. The point is that collaboration architecture materially changes how well the system handles broad, messy engineering tasks.

| System | % Resolved |
|---|---:|
| Sonnet 4.6 | 79.60 |
| WeCode (multi-agent on Codex) | 79.20 |
| live-SWE-agent + Claude 4.5 Opus medium (20251101) | 79.20 |
| Sonar Foundation Agent + Claude 4.5 Opus | 79.20 |
| TRAE + Doubao-Seed-Code | 78.80 |
| live-SWE-agent + Gemini 3 Pro Preview (2025-11-18) | 77.40 |
| Atlassian Rovo Dev (2025-09-02) | 76.80 |
| EPAM AI/Run Developer Agent v20250719 + Claude 4 Sonnet | 76.80 |
| mini-SWE-agent + Claude 4.5 Opus (high reasoning) | 76.80 |
| ACoder | 76.40 |
| mini-SWE-agent + Gemini 3 Flash (high reasoning) | 75.80 |

> `WeCode` is currently shown here as a public self-evaluated snapshot. Update this section once an official leaderboard submission is published.

## Quick Start

```powershell
# 1) Download the latest Windows binary from Releases
# 2) Launch WeCode
.\wecode-windows-x64.exe

# 3) Give the swarm a concrete engineering goal
#    Example: fix a failing test, inspect a regression, or plan a refactor
```

Current public distribution:

- Windows x64 binary via [GitHub Releases](https://github.com/wmjwmj100/wecode/releases)
- Binary publishing notes in [BINARY_UPLOAD.md](./BINARY_UPLOAD.md)

## Roadmap

- [x] Core swarm runtime
- [x] Shared blackboard communication
- [x] Readable cross-agent execution traces
- [ ] Web UI for live swarm observation
- [ ] Custom specialist profiles
- [ ] Strategy self-critique during long-horizon runs
- [ ] Domain packs for analysis-heavy workflows, including finance
- [ ] Multi-repo task execution

## Contributing

WeCode is still early. The most useful contributions right now are concrete failures, surprising coordination wins, and trace-backed bug reports.

- Open issues: [github.com/wmjwmj100/wecode/issues](https://github.com/wmjwmj100/wecode/issues)
- Follow releases: [github.com/wmjwmj100/wecode/releases](https://github.com/wmjwmj100/wecode/releases)

<a id="chinese-summary"></a>

## Chinese Summary

WeCode 是一个基于 Codex 的多智能体编程系统。它不是让一个模型串行完成“理解代码、制定方案、修改、验证、复盘”全部流程，而是让多个智能体并行探索、共享上下文、互相校验，再汇总成一个最终结果。

### 中文速览

- **并行探索：** 多个智能体同时查看不同文件、路径和假设，缩短进入上下文的时间。
- **共享记忆：** 发现会写入公共工作区，后来加入的智能体不需要从零开始。
- **交叉验证：** 方案在收敛前会经过同伴挑战，而不是默认接受第一版答案。
- **过程可见：** README 中的视觉区块预留了架构图、观测视图和后续截图位置，方便你继续补完整个 GitHub 首页。

### 中文快速开始

```powershell
# 1) 从 Releases 下载最新 Windows x64 二进制
# 2) 运行 WeCode
.\wecode-windows-x64.exe

# 3) 输入一个明确的工程目标开始使用
```

### 中文说明

- 当前 README 图片已切换到 `images/*.png`，后续可继续直接替换同路径文件。
- 当前基准部分沿用仓库里已有的公开快照写法，并明确标注了 `WeCode` 为自测条目。
- 公共仓库暂时只保留高层说明，不展开内部实现细节。
