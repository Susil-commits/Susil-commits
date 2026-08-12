<div align="center">

<p width="700" align="center">
A final-year Computer Science student who likes taking a real-world problem all the way to something that runs in production. I've built three consumer-facing platforms on the MERN stack, and I've since moved into backend/platform engineering — designing and building systems that manage <em>other</em> systems: deployment controllers, health-gated rollouts, and event-driven self-healing infrastructure. I care about what breaks a system in production (race conditions, drift, retry storms) as much as what ships a feature.
</p>

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/susil-kumar-nayak-5180472b6)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:nayaksushil298@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Susil-commits)

</div>

<br>

## Focus

Two tracks, one habit: don't just build the happy path — engineer for the failure modes that actually show up in production.

- **Platform Engineering (current):** `HyperDeploy` and `EdgeGuard` — a hybrid deployment controller and a self-healing edge-monitoring platform, both built around explicit failure-scenario matrices (crash loops, drift, unsigned artifacts, WAN outages) rather than just the demo path.
- **Full-Stack Applications:** Three MERN platforms — a farmer marketplace, a food-redistribution network, and a driver-booking system — each load-tested and hardened against race conditions, N+1 queries, and duplicate writes.

Currently building functional-programming fundamentals in **Haskell** to bring FP discipline (pure functions, no shared state) into backend and rule-engine design.

<br>

## 🛠️ Platform Engineering

<table>
<tr>
<td width="50%" valign="top">

### [HyperDeploy](https://github.com/Susil-commits/HyperDeploy) — Hybrid Deployment Controller

![Python](https://img.shields.io/badge/Python%203.13-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)
![Cosign](https://img.shields.io/badge/Cosign-Sigstore-FF69B4?style=flat-square)

A GitOps-aligned control plane that unifies **bare-metal/VM automation (Ansible)** and **container orchestration (Kubernetes)** behind one secure release pipeline — instead of managing them as two disconnected tools.

- Immutable-artifact enforcement: rejects mutable tags, verifies **Cosign** signatures before a release ever touches the DB.
- Health-gated rollouts: classifies pod state (`CrashLoopBackOff`, stalled rollout, failed readiness) and auto-triggers rollback to the last known-good release.
- GitOps drift reconciliation: auto-corrects drift in dev, alert-only in prod — no silent prod mutations.
- Enterprise RBAC (Viewer → Admin) with dual-control self-approval prevention and non-bypassable audit logging.
- Async-safe by design: idempotent job queue, stale-worker reaper, exponential-backoff DB retries.

<sub>Engineered against a **24-scenario failure matrix** (A1–G1) — mutable tags, unsigned images, race conditions on concurrent releases, SSH-unreachable hosts, worker crashes mid-job, secret leaks in logs, and more — each with a defined detection path and system response.</sub>

</td>
<td width="50%" valign="top">

### [EdgeGuard](https://github.com/Susil-commits/EdgeGuard) — Self-Healing Edge Monitoring

![Python](https://img.shields.io/badge/Python%203.12-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![EDA](https://img.shields.io/badge/Event--Driven%20Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Postgres](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

An edge fleet monitoring platform built around **Red Hat Event-Driven Ansible** and predictive alerting — detection and remediation are fully decoupled, so new response policies are a YAML rulebook change, not a redeploy.

- Predictive EWMA trend forecasting: extrapolates metric trajectories to catch threshold breaches **up to 6 hours** before they happen.
- Offline-first edge agent: buffers telemetry in a local SQLite WAL spool during WAN outages, replays with zero duplicates via `event_id` idempotency.
- Remediation is declarative: incidents match against YAML rulebooks (`ansible-rulebook`), which trigger allow-listed Ansible playbooks over SSH — no ad-hoc scripting on prod hosts.
- Security-first automation: server-side `ALLOWED_PLAYBOOKS` registry blocks unauthorized playbook execution; every action lands in an immutable audit ledger.
- Full observability loop: Prometheus `/metrics` + pre-built Grafana dashboards, multi-tenant RBAC, optional Keycloak OIDC SSO.

<sub>Every major component — EWMA forecaster, offline spooling, EDA rulebook integration, K8s manifests, Prometheus/Grafana wiring, Keycloak OIDC — is **built**, not just designed; see the repo's built-vs-designed audit table.</sub>

</td>
</tr>
</table>

<br>

## Tech Stack

<div align="center">

**Languages**
<br>
<img src="https://skillicons.dev/icons?i=py,js,ts,cpp,java,haskell" />

**Backend & APIs**
<br>
<img src="https://skillicons.dev/icons?i=fastapi,nodejs,express,socketio" />

**Data & Queues**
<br>
<img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,mysql,sqlite" />

**Infra & Automation**
<br>
<img src="https://skillicons.dev/icons?i=kubernetes,docker,ansible,git,github" />

**Observability & Reliability**
<br>
<img src="https://skillicons.dev/icons?i=prometheus,grafana,jest" />
![Artillery](https://img.shields.io/badge/Artillery-FF4F00?style=flat-square)
![Cosign](https://img.shields.io/badge/Cosign-FF69B4?style=flat-square)

**Frontend**
<br>
<img src="https://skillicons.dev/icons?i=react,tailwind,html" />

</div>

<br>

## Full-Stack Applications

<table>
<tr>
<td width="33%" valign="top">

**[FaRm](https://github.com/Susil-commits/FarmDirect)** — Farmer-to-Consumer Marketplace
`React` `TS` `Node` `MongoDB`

Load-tested at 200 concurrent users, sub-150ms p95. Compound indexing cut filter-query latency 95%. Idempotency-key checkout protection + z-score order anomaly detection.

</td>
<td width="33%" valign="top">

**[Left2Serve](https://github.com/Susil-commits/Left2Serve)** — Food Redistribution
`React` `TS` `Node` `PostgreSQL`

`SERIALIZABLE` transactions resolve donation race conditions. Rate-limiting blocked 18K+ excess requests under load. Real-time Socket.io matching + self-healing retry/circuit-breaker notifications.

</td>
<td width="33%" valign="top">

**[MyMate](https://github.com/Susil-commits/MyMate)** — Driver Booking Platform
`React` `TS` `Node` `MongoDB`

Fixed a production Socket.IO race by re-sequencing writes before event emission. Live WebSocket tracking, AI-heuristic driver matching, Tesseract.js OCR for KYC.

</td>
</tr>
</table>

<br>

## Experience & Certifications

<table>
<tr>
<td width="50%" valign="top">

**Backend Developer Intern**
Techgeering Solutions Pvt. Ltd. — Oct '25 to Feb '26

Built 5+ reusable UI/API components for a real-time video-handling platform on the MERN stack; resolved 20+ bugs across the SDLC in an Agile/Scrum team of 4.

</td>
<td width="50%" valign="top">

- Oracle Cloud Infrastructure 2025 Certified Generative AI Professional
- Oracle Cloud Infrastructure 2025 Certified Data Science Professional
- Oracle Certified Foundations Associate (Agentic AI) — 88%
- NASSCOM FutureSkills Prime — Big Data (Gold)

</td>
</tr>
</table>

<br>

## GitHub Stats

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=Susil-commits&theme=tokyo-night&hide_border=true"/>

</div>

<br>

<div align="center">
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1e3a5f,100:0f172a&height=120&section=footer"/>
</div>
