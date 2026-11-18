# the-citadel

My 25-week system design adventure, **The Architect's Road**. Each week I read the theory, watch it work in a visualizer, build it for real in my own Docker lab (the Citadel), break it on purpose, and face that week's Foe.

## What's here

| Path | What it is |
|---|---|
| `system design learning.pdf` | My original research: fivenines.dev, free alternatives, first draft plan |
| `_bmad-output/party-mode/architects-road.html` | The 25-week plan as an adventure map ([live page](https://claude.ai/artifact/UzgAazFqS1erGSaASdrFkj)) |
| `.claude/skills/teach-me-system-design/` | My Guide: a Claude Code skill that teaches each week as a chapter of the story |
| `_bmad-output/system-design-quest/` | Progress and weekly field logs (created as I go) |
| `citadel/` | The Docker lab, growing one service a week (from week 0) |
| `_bmad/`, `.claude/skills/bmad-*` | BMAD tooling used for planning |

## The road

| Act | Weeks | Theme |
|---|---|---|
| Prologue | 0 | The Workshop: Docker + WSL2 |
| I · The Roads | 1–3 | TCP, DNS, proxies, protocols |
| II · The Citadel | 4–12 | Load balancing, caching, databases, replication, Kafka, Raft, resilience, observability |
| III · Grand Designs | 13–15 | URL shortener, chat, news feed (design first, then compare) |
| IV · Uncharted Lands | 16–19 | APIs, storage/CDN/search, security, event-driven + multi-region |
| V · The Forge | 20–24 | Queueing theory, discrete-event simulation, my own simulator |

## The four oaths

1. Predict before you press.
2. First 30 minutes alone: no AI, no search.
3. AI is my opponent, not my author.
4. Design first, read the answer after.

## Start a lesson

In Claude Code, from this folder:

```
/teach-me-system-design start week 0
```
