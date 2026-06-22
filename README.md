<div align="center">

<!-- BANNER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=timeAuto&height=140&section=header&text=&animation=fadeIn" width="100%" />

</p>
<!-- TYPING HEADER -->
<a href="https://github.com/Akhil006-2">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=42&pause=1000&color=58A6FF&center=true&vCenter=true&width=700&height=70&lines=AKHIL+G" alt="Akhil G" />
</a>

<a href="https://github.com/Akhil006-2">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=400&size=18&pause=2000&color=8B949E&center=true&vCenter=true&width=700&height=40&lines=Software+Engineer;Backend+Systems;Distributed+Systems;System+Design;High+Performance+Computing;AI+Systems;Open+Source;Algorithms" alt="Role Rotation" />
</a>

<br/>

<!-- SOCIAL BADGES -->
<p>
  <a href="https://github.com/Akhil006-2">
    <img src="https://img.shields.io/github/followers/Akhil006-2?label=Followers&style=flat-square&color=58A6FF&labelColor=161b22&logo=github" />
  </a>
  &nbsp;
  <a href="https://linkedin.com/in/akhil-g-287249328">
    <img src="https://img.shields.io/badge/LinkedIn-Akhil%20G-0A66C2?style=flat-square&logo=linkedin&logoColor=white&labelColor=161b22" />
  </a>
  &nbsp;
  <img src="https://komarev.com/ghpvc/?username=Akhil006-2&style=flat-square&color=58A6FF&label=Profile+Views&labelColor=161b22" />
  &nbsp;
  <img src="https://img.shields.io/badge/Location-Coimbatore%2C+India-58A6FF?style=flat-square&logo=googlemaps&logoColor=white&labelColor=161b22" />
  &nbsp;
  <img src="https://img.shields.io/badge/Target-Google+SWE+2027-EA4335?style=flat-square&logo=google&logoColor=white&labelColor=161b22" />
</p>

</div>

---

## `$ whoami`

```
akhil@systems:~$ cat profile.txt

Backend engineer building fault-tolerant, observable, and high-throughput systems.

Current focus: distributed systems, system design, and backend infrastructure.
Engineering mindset: measure first, optimize second, design for failure always.

Open Source contributor in the backend and developer tooling space.
Targeting Google SWE Internship 2027.

Location   : Coimbatore, India
Status     : Building production-grade systems. Actively learning.
```

I build software that works reliably under real-world conditions — not demos.

My work centers on backend architecture, distributed systems primitives, and infrastructure that teams don't need to babysit. I care deeply about latency, fault isolation, observability, and systems that stay simple enough to reason about as they grow.

---

## Engineering Philosophy

```
01  Measure before optimizing.          Profiling beats intuition.
02  Reliability is a feature.           Uptime is engineering, not luck.
03  Design for failure.                 Every external call will fail. Eventually.
04  Simple systems scale better.        Complexity is a cost paid forever.
05  Readable code outlives clever code. Your future self is the next maintainer.
06  Observability is mandatory.         You can't fix what you can't see.
07  Latency has a tail.                 p99 matters more than p50.
08  Build once. Maintain forever.       Design with the full lifecycle in mind.
```

---

## Featured Projects

<details>
<summary><b>▸ Orchestrate — Distributed LLM Orchestration Engine</b></summary>

<br/>

```
Architecture: Modular provider-abstraction layer over multiple LLM backends
Scale:        Designed for concurrent workloads with structured retry semantics
Status:       Active development
```

**Problem**

Production LLM workflows are fragile: single-provider lock-in, silent prompt failures, zero visibility into latency or token costs, and no structured retry logic. Most "AI backends" are procedural scripts, not engineered systems.

**What Orchestrate Solves**

| Concern | Implementation |
|---|---|
| Provider abstraction | Unified interface over OpenAI, Anthropic, Gemini — swap without code changes |
| Fault tolerance | Exponential backoff retry engine with configurable jitter |
| Observability | Structured JSON logging + per-call latency tracking |
| Prompt integrity | Schema-validated JSON outputs with guardrail enforcement |
| Caching | Response memoization to reduce redundant API calls and latency |
| Evaluation | Built-in eval framework for prompt quality regression testing |
| Versioning | Prompt versioning with rollback support |

**Architecture**

```
┌─────────────────────────────────────────────────────┐
│                   Orchestrate Engine                │
│                                                     │
│  ┌──────────────┐    ┌──────────────────────────┐  │
│  │ Prompt Store │───▶│    Execution Planner      │  │
│  │  (versioned) │    │  (retry + fallback logic) │  │
│  └──────────────┘    └──────────┬───────────────┘  │
│                                 │                   │
│  ┌──────────────────────────────▼────────────────┐  │
│  │            Provider Abstraction Layer          │  │
│  │   OpenAI   │   Anthropic   │   Gemini  │ ...  │  │
│  └──────────────────────────────────────────────┘  │
│                                                     │
│  ┌──────────────┐    ┌──────────────┐               │
│  │  JSON Guard  │    │ Eval Runner  │               │
│  │  (schema val)│    │ (regression) │               │
│  └──────────────┘    └──────────────┘               │
│                                                     │
│  ┌────────────────────────────────────────────────┐ │
│  │    Structured Logger + Latency Tracker         │ │
│  └────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────┘
```

**Engineering Challenges**
- Designing a provider interface that doesn't leak implementation details across boundaries
- Building retry semantics that handle rate limits, timeouts, and partial failures distinctly
- Making prompt versioning queryable without a heavy database dependency

**Tech Stack**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)
![JSON Schema](https://img.shields.io/badge/JSON_Schema-000000?style=flat-square&logo=json&logoColor=white)

[![View Repository](https://img.shields.io/badge/GitHub-Orchestrate-58A6FF?style=flat-square&logo=github)](https://github.com/Akhil006-2)

</details>

---

<details>
<summary><b>▸ AnaMetrix — Engineering Telemetry & DORA Metrics Platform</b></summary>

<br/>

```
Architecture: FastAPI backend + MongoDB time-series store + Prometheus metrics export
Scale:        Multi-team CI/CD pipeline aggregation with real-time dashboards
Status:       Active development
```

**Problem**

Engineering teams fly blind without DORA metrics. Deployment frequency, lead time, MTTR, and change failure rate live across disconnected systems. No single platform gives teams a real-time engineering health signal.

**What AnaMetrix Solves**

| Metric | Implementation |
|---|---|
| Deployment Frequency | Webhook ingestion from CI/CD pipelines |
| Lead Time for Changes | Git commit → production timestamp tracking |
| MTTR | Incident lifecycle state machine |
| Change Failure Rate | Rollback event correlation |
| Forecasting | Time-series trend projection over 30/60/90 day windows |

**Architecture**

```
┌──────────────────────────────────────────────────────┐
│                    AnaMetrix Platform                │
│                                                      │
│  CI/CD Webhooks ──▶ Ingestion API (FastAPI)          │
│  GitHub Events  ──▶       │                          │
│  Incident Hooks ──▶       ▼                          │
│                    Event Normalizer                  │
│                           │                          │
│              ┌────────────▼────────────┐             │
│              │     MongoDB Store        │             │
│              │  (time-series + indexes) │             │
│              └────────────┬────────────┘             │
│                           │                          │
│       ┌───────────────────▼──────────────────┐       │
│       │         Metrics Computation Layer     │       │
│       │   DORA Aggregator │ Trend Forecaster  │       │
│       └───────────────────┬──────────────────┘       │
│                           │                          │
│   Prometheus Exporter ◀───┘   Dashboard API          │
│   (scrape endpoint)           (REST + WebSocket)     │
└──────────────────────────────────────────────────────┘
```

**Engineering Challenges**
- Normalizing event schemas across heterogeneous CI/CD providers (GitHub Actions, Jenkins, GitLab CI)
- Designing MongoDB indexes for time-range aggregation queries without full collection scans
- Keeping Prometheus metric cardinality bounded to avoid memory blowup

**Tech Stack**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

[![View Repository](https://img.shields.io/badge/GitHub-AnaMetrix-58A6FF?style=flat-square&logo=github)](https://github.com/Akhil006-2)

</details>

---

<details>
<summary><b>▸ Emotion Recognition — Real-Time Computer Vision Inference Pipeline</b></summary>

<br/>

```
Architecture: Multithreaded OpenCV capture → TensorFlow inference → live dashboard
Scale:        Real-time inference with optimized frame pipeline
Status:       Completed
```

**Problem**

Naive emotion recognition pipelines are latency-bound: blocking I/O on video capture stalls the inference thread, making real-time feel like slideshow. Most implementations don't separate capture, inference, and rendering into independent stages.

**What the Pipeline Solves**

| Concern | Implementation |
|---|---|
| Frame pipeline | Producer-consumer threading model — capture and inference run independently |
| Inference latency | TensorFlow model quantization + frame-skip under load |
| Real-time display | Non-blocking OpenCV rendering thread |
| Dashboard | Live confidence score visualization per emotion class |

**Architecture**

```
┌─────────────────────────────────────────────┐
│       Emotion Recognition Pipeline          │
│                                             │
│  Capture Thread ──▶ Frame Queue             │
│  (OpenCV)               │                   │
│                         ▼                   │
│              Inference Thread               │
│              (TensorFlow model)             │
│                         │                   │
│                         ▼                   │
│              Render Thread ──▶ Dashboard    │
│              (OpenCV window)  (live scores) │
└─────────────────────────────────────────────┘
```

**Engineering Challenges**
- Preventing frame queue backpressure from blocking the capture thread under load
- Tuning inference frequency vs. display refresh rate for perceived smoothness

**Tech Stack**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)

[![View Repository](https://img.shields.io/badge/GitHub-Emotion--Recognition-58A6FF?style=flat-square&logo=github)](https://github.com/Akhil006-2)

</details>

---

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=c%2B%2B&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)

**Backend & APIs**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![REST](https://img.shields.io/badge/REST_API-FF6C37?style=flat-square&logo=postman&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square&logo=socket.io&logoColor=white)

**Databases**

![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)

**Observability & Infrastructure**

![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

**AI / ML**

![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white)

**Learning (2025)**

![Go](https://img.shields.io/badge/Go-learning-00ADD8?style=flat-square&logo=go&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-learning-000000?style=flat-square&logo=rust&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-learning-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-learning-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-learning-244C5A?style=flat-square&logo=grpc&logoColor=white)
![Raft](https://img.shields.io/badge/Raft_Consensus-learning-58A6FF?style=flat-square)

---

## Engineering Focus Areas

```
Distributed Systems      ████████████░░░░  Actively learning — reading Designing Data-Intensive Applications
System Design            ████████████░░░░  Practicing HLD + LLD; studying real architectures
Backend Infrastructure   █████████████░░░  Applied in project work (Orchestrate, AnaMetrix)
Observability            ████████████░░░░  Prometheus, structured logging, latency tracking
Algorithms & DSA         ██████████████░░  Competitive programming, preparing for SWE interviews
Concurrency              ████████░░░░░░░░  Multithreading in Python; learning Go concurrency model
Networking               ██████░░░░░░░░░░  TCP/IP fundamentals, HTTP internals, DNS
```

---

## What I'm Currently Studying

<details>
<summary><b>▸ Distributed Systems</b></summary>

<br/>

```
Reading:   Designing Data-Intensive Applications — Martin Kleppmann
           Distributed Systems (van Steen & Tanenbaum)
Studying:  Raft consensus algorithm
           CAP theorem implications in real systems
           Clock synchronization (Lamport, vector clocks)
           Consistent hashing and its ring implementation
           Leader election patterns
Building:  Small Raft implementation to understand log replication
```

</details>

<details>
<summary><b>▸ System Design</b></summary>

<br/>

```
Practicing:  URL shortener, rate limiter, notification system, distributed cache
Focus:       Capacity estimation, bottleneck identification, trade-off articulation
Studying:    How Twitter, Discord, Uber, and Stripe actually built their backends
             Read-heavy vs write-heavy system design distinctions
             Sharding strategies and their rebalancing costs
```

</details>

<details>
<summary><b>▸ Algorithms & Competitive Programming</b></summary>

<br/>

```
Platform:    LeetCode, Codeforces
Focus:       Graphs (DFS/BFS, Dijkstra, Bellman-Ford, union-find)
             Dynamic programming (knapsack, LCS, interval DP)
             Trees (segment trees, tries, binary lifting)
             String algorithms (KMP, Z-function, Aho-Corasick)
Target:      Google interview readiness by mid-2026
```

</details>

<details>
<summary><b>▸ Go & Systems Programming</b></summary>

<br/>

```
Learning:    Go concurrency model — goroutines, channels, select
             Memory model and escape analysis basics
             Writing small CLI tools and HTTP servers in Go
Goal:        Rebuild a component of Orchestrate in Go to compare throughput
```

</details>

---

## Interests in Backend Engineering

These are the problems I find worth thinking about:

```
Rate Limiting           — Token bucket vs leaky bucket vs sliding window; distributed rate limiting with Redis
Load Balancing          — L4 vs L7, consistent hashing, least-connections, session stickiness
Caching                 — Cache invalidation strategies, cache-aside vs write-through, CDN edge caching
Distributed Queues      — Kafka log architecture, consumer group rebalancing, at-least-once delivery
Service Meshes          — Sidecar proxies, mTLS, observability at the network layer
Fault Isolation         — Circuit breakers, bulkheads, timeouts, retries with backoff
Database Internals      — B-tree vs LSM-tree, WAL, MVCC, index design
Consensus Protocols     — Raft log replication, leader election, split-brain prevention
Observability           — The three pillars: metrics, logs, traces. Why you need all three.
```
---

## 2027 Engineering Roadmap

```
2025 Q1─Q2  ──▶  Deepen Orchestrate: add gRPC transport, persistent prompt store, multi-node eval
            ──▶  AnaMetrix: add Grafana integration, alert rule engine, team-level DORA breakdown
            ──▶  Study Raft. Implement log replication from scratch.
            ──▶  Go: rewrite one Orchestrate component. Benchmark against Python.

2025 Q3─Q4  ──▶  Kafka: build a small event pipeline project (producer → consumer → sink)
            ──▶  Redis internals: persistence modes, cluster topology, eviction policies
            ──▶  System Design: complete 40 system design case studies with written breakdowns
            ──▶  Kubernetes: deploy Orchestrate to a local k8s cluster; understand pod scheduling

2026        ──▶  Open Source: meaningful contribution to a backend/infra OSS project
            ──▶  Rust: systems programming fundamentals; memory model, ownership, lifetimes
            ──▶  Interview prep: LeetCode 300+ (focus: graphs, DP, trees)
            ──▶  Apply: Google SWE Internship 2027

2027        ──▶  Google SWE Internship
```

---

## Repository Standards

Every project I ship includes:

```
README.md           Architecture overview, installation, API reference
ARCHITECTURE.md     System design decisions and trade-offs documented
/docs               API docs, sequence diagrams, deployment guide
Dockerfile          Reproducible build
docker-compose.yml  Local development environment
.github/workflows   CI pipeline — lint, test, build on every PR
BENCHMARKS.md       Baseline performance numbers
CHANGELOG.md        What changed and why
```

---

## Open Source

Interested in contributing to projects in:

```
Backend infrastructure    (API frameworks, task queues, job schedulers)
Developer tooling         (CLI tools, observability libraries, testing frameworks)
Distributed systems       (consensus implementations, consistent hash libraries)
Observability             (metrics exporters, log aggregators, trace samplers)
```

If you maintain a project in these areas and want a contributor — reach out.

---

<div align="center">

```
akhil@systems:~$ uptime
seeking: google swe internship 2027
building: distributed systems, backend infrastructure
status: online

```

<br/>

**[GitHub](https://github.com/Akhil006-2)** &nbsp;·&nbsp; **[LinkedIn](https://linkedin.com/in/akhil-g-287249328)**

<br/>

<!-- FOOTER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=timeAuto&height=100&section=footer" width="100%" />
</div>
