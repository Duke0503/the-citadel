<div align="center">

# 🏰 The Citadel

### *An architect's 25-week journey through the Realm of Uptime*

**Read the theory · Watch it run · Build it for real · Break it on purpose · Defeat the Foe**

`Apprentice` → `Journeyman` → `Builder` → `Architect` → `Master Architect`

[🗺️ Open the adventure map](https://claude.ai/artifact/UzgAazFqS1erGSaASdrFkj) · [📜 The Guide](.claude/skills/teach-me-system-design/) · [📖 Field logs](_bmad-output/system-design-quest/)

</div>

---

> *Midnight. An empty plot of land at the edge of the Realm of Uptime.*
>
> *I arrive with a toolbox, a notebook, and one question: how do the great cities stay standing when millions of travelers arrive at once, and what happens on the night they fall?*
>
> *Nobody is going to hand me the answer. I'll build my own city, one building a week, and every week something will come to tear it down.*
>
> *This repository is that city.*

---

## ⚔️ The rules of the road

| | Oath | Why |
|---|---|---|
| 🔮 | **Predict before you press** | The gap between my guess and reality *is* the lesson |
| ⏳ | **First 30 minutes alone** | No AI, no search. My brain goes first |
| 🛡️ | **AI is my opponent, not my author** | It attacks my designs, it never writes them |
| 🧭 | **Design first, read the answer after** | That's how I learn to *think* like an architect, not memorize one |

---

## 🗺️ The map

```
   PROLOGUE        ACT I           ACT II              ACT III          ACT IV            ACT V
  ┌────────┐    ┌─────────┐    ┌─────────────┐    ┌────────────┐   ┌───────────┐   ┌────────────┐
  │Workshop│───▶│The Roads│───▶│ The Citadel │───▶│Grand Design│──▶│ Uncharted │──▶│ The Forge  │
  └────────┘    └─────────┘    └─────────────┘    └────────────┘   └───────────┘   └────────────┘
    wk 0          wk 1–3           wk 4–12           wk 13–15         wk 16–19        wk 20–24
   Docker       TCP · DNS      LB · Cache · DB     URL shortener     APIs · CDN      Queueing math
   WSL2         Protocols      Kafka · Raft        Chat · Feed       Security        My own
                               Resilience · O11y                     Multi-region    simulator
```

---

## 🐉 The Bestiary: a Foe for every week

Every Foe is a real failure that has taken down real systems.

| Wk | Chapter | Foe | What it really is | ✓ |
|---:|---|---|---|:-:|
| 0 | Forge the Workshop | **The Rust** | "Works on my machine" | ⬜ |
| 1 | The Messenger's Handshake | **The Long Silence** | Latency, TCP handshakes | ⬜ |
| 2 | The Map of Names | **The Lost Courier** | DNS, reverse proxies | ⬜ |
| 3 | Tongues of the Realm | **The Babel Wind** | TLS, HTTP/2, WebSockets, gRPC | ⬜ |
| 4 | The Gatekeepers | **The Slow Gate** | Load balancing + estimation | ⬜ |
| 5 | The Memory Vaults | **The Stampede** | Cache stampede | ⬜ |
| 6 | The Great Archive | **The Endless Scroll** | Indexes, B-trees | ⬜ |
| 7 | The Mirrored Archives | **The Laggard Twin** | Replication lag, sharding | ⬜ |
| 8 | The Couriers' Guild | **The Tangled Post** | Queues, Kafka partitions | ⬜ |
| 9 | Secrets of the Guild | **The Backlog Beast** | Consumer lag, rebalancing | ⬜ |
| 10 | The Council of Nodes | **The Split Crown** | Raft, quorum, split-brain | ⬜ |
| 11 | The Shield Wall | **The Echo Storm** | Retry storms, circuit breakers | ⬜ |
| 12 | The Watchtower | **The Fog** | Observability | ⬜ |
| 13 | The Short Road | **The Billion Doors** | Design: URL shortener | ⬜ |
| 14 | The Endless Conversation | **The Sleeping Friend** | Design: chat system | ⬜ |
| 15 | The Town Crier | **The Celebrity's Voice** | Design: news feed fan-out | ⬜ |
| 16 | The Treaty Halls | **The Broken Treaty** | API design, idempotency | ⬜ |
| 17 | The Far Warehouses | **The Far Mountain** | Object storage, CDN, search | ⬜ |
| 18 | The Locksmiths | **The Thief in Gray** | Auth, OWASP | ⬜ |
| 19 | Across the Seas | **The Wide Ocean** | Sagas, multi-region | ⬜ |
| 20 | Study the Masters | **The Mirror** | Product teardown | ⬜ |
| 21 | The Mathematics of Waiting | **The Crowd at the Gate** | Queueing theory | ⬜ |
| 22 | The Clockwork Engine | **The Clockwork Ghost** | Discrete-event simulation | ⬜ |
| 23 | Reading the Old Maps | **The Labyrinth** | Architecture + ADRs | ⬜ |
| 24 | The First Stone | **The Blank Page** | My first playable lesson | ⬜ |

*When a Foe falls, its ⬜ becomes ✅.*

---

## 🏗️ The Citadel grows

The city starts empty. By week 12 it looks like this, and every box is something I built, broke and repaired myself:

```
                 Travelers ──▶ [ nginx · the Gatekeeper ]
                                   │        │        │
                               [ app ]  [ app ]  [ app ]  ◀── Shield Wall: timeouts · retries · breaker
                                   │        │
                    ┌──────────────┼────────┴──────────────┐
                    ▼              ▼                       ▼
            [ Redis · Vault ] [ Postgres · Archive ]  [ Kafka · Couriers' Guild ]
                               │  └─▶ [ replica ]          │
                               │                           ▼
                        [ etcd · Council of 3 ]       [ workers ]

            [ Prometheus + Grafana · the Watchtower ] sees everything
```

---

## 📅 A week on the road

| When | What | Where |
|---|---|---|
| **Mon – Tue** | 📖 Read the theory | Papers, books, engineering blogs |
| **Wed** | 👀 Watch it run | Visualizers: samwho.dev, Raft, B-trees, Kafka |
| **Thu – Fri** | 🔨 Build it, then break it | My Docker lab: `citadel/` |
| **Weekend** | 🐉 Boss battle + field log | systemdesigner.io + the Guide |

---

## 🧙 The Guide

An old architect with a satchel of incident reports from a hundred fallen cities. The Guide never lectures and never gives away the answer. It sets the scene, asks for my prediction, sends me on missions, and then **attacks my design** in the boss battle.

```bash
/teach-me-system-design start week 0     # begin (or resume) a chapter
/teach-me-system-design review my boss   # face this week's Foe
/teach-me-system-design quiz me          # recall battles from past weeks
/teach-me-system-design where am I       # show the map and my rank
```

When I'm stuck, the Guide climbs a **hint ladder**: question → lens → analogy → partial → reveal. I want to need fewer rungs every week.

---

## 📂 What's in the satchel

| Path | Contents |
|---|---|
| [`_bmad-output/party-mode/architects-road.html`](_bmad-output/party-mode/architects-road.html) | The full 25-week map with every link, mission and boss |
| [`.claude/skills/teach-me-system-design/`](.claude/skills/teach-me-system-design/) | The Guide: curriculum, story world, lesson flow, boss review |
| `_bmad-output/system-design-quest/` | My progress, field logs and the running chronicle *(created on the road)* |
| `citadel/` | The Docker lab *(rises in week 0)* |
| `_bmad/`, `.claude/skills/bmad-*` | BMAD planning tools |

---

## 🌅 The destination

After 25 weeks I want to be able to look at any system (a chat app, a payment flow, a game server) and *see* it: where the state lives, what breaks at 10x, what it gives up and why.

Then I'll build something original: **a simulator where other people learn system design by watching cities rise and fall.**

<div align="center">

*The road starts at week 0. The Rust is already creeping into the workshop.* 🔨

**[⚔️ Begin the journey](https://claude.ai/artifact/UzgAazFqS1erGSaASdrFkj)**

</div>
