# wecode

`wecode` is a multi-agent coding assistant built on top of Codex.

## What It Is

wecode focuses on collaborative software delivery with multiple agents working in parallel under one coordination model.

## Why Multi-Agent

- Full-connectivity collaboration: agents can coordinate across tasks instead of working in isolation.
- Self-organization: the system can dynamically adjust collaboration patterns based on task state.
- Parallel execution: complex work can be split and processed concurrently to improve throughput.
- Human-visible coordination: collaboration status can be surfaced for better operational clarity.

## Positioning

wecode is designed for engineering teams that need higher execution speed and clearer coordination in complex coding workflows.

## Benchmark Board (Snapshot + Unlisted Results)

The board below combines:
- Official leaderboard entries visible in the shared snapshot.
- Additional self-evaluated entries that are **not yet listed** on the official board.

| Model | % Resolved | Source | Official Board Status |
|---|---:|---|---|
| Sonnet 4.6 | 79.60 | Self-evaluated | Not listed on official board |
| wecode (multi-agent, based on Codex) | 79.20 | Self-evaluated | Not listed on official board |
| live-SWE-agent + Claude 4.5 Opus medium (20251101) | 79.20 | Official snapshot | Listed |
| Sonar Foundation Agent + Claude 4.5 Opus | 79.20 | Official snapshot | Listed |
| TRAE + Doubao-Seed-Code | 78.80 | Official snapshot | Listed |
| live-SWE-agent + Gemini 3 Pro Preview (2025-11-18) | 77.40 | Official snapshot | Listed |

> Note: This repository intentionally keeps architecture details high-level.
