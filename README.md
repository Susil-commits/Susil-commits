<div align="center">

# Susil Kumar Nayak

### Backend-Focused Full-Stack Developer · B.Tech CSE '26

Building production-grade REST APIs that hold up under load — race conditions resolved, indexes tuned, latency measured.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/susil-kumar-nayak-5180472b6)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:nayaksushil298@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/Susil-commits)

</div>

<br>

## Focus

Three independently built platforms, each pushed through load testing and fixed for the failure modes that actually show up in production — race conditions, N+1 queries, retry storms, duplicate writes. Currently building functional-programming fundamentals in **Haskell** to bring FP discipline (pure functions, no shared state) into backend design.

<br>

## Tech Stack

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Haskell](https://img.shields.io/badge/Haskell-5D4F85?style=flat-square&logo=haskell&logoColor=white)

**Backend & APIs**
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
![Socket.io](https://img.shields.io/badge/Socket.io-010101?style=flat-square&logo=socketdotio&logoColor=white)
![REST API](https://img.shields.io/badge/REST%20API-005571?style=flat-square&logo=fastapi&logoColor=white)

**Databases**
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)

**Reliability & Testing**
![Jest](https://img.shields.io/badge/Jest-C21325?style=flat-square&logo=jest&logoColor=white)
![Supertest](https://img.shields.io/badge/Supertest-25D366?style=flat-square&logo=checkmarx&logoColor=white)
![Artillery](https://img.shields.io/badge/Artillery-FF4F00?style=flat-square&logo=artillery&logoColor=white)

**Cloud & DevOps**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazonaws&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI%2FCD-2088FF?style=flat-square&logo=githubactions&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)

<br>

## Projects

### [FaRm — Farmer-to-Consumer Marketplace](https://github.com/Susil-commits/FarmDirect)
`React.js` `TypeScript` `Node.js` `Express.js` `MongoDB` `Tailwind CSS` `Artillery`

- Load-tested at 200 concurrent users — sub-150ms p95 latency, 0% error rate.
- Cut filter query latency from ~240ms to ~12ms (95%) via MongoDB compound indexing.
- Migrated the entire backend from JavaScript to TypeScript for full type safety.
- Idempotency-key duplicate-request protection on checkout: Mongo unique constraint + atomic transaction + cached response replay.
- Rolling-average / z-score anomaly detection on order transactions — flags abnormal orders for manual review without an ML model.
- Patched all high/critical dependency vulnerabilities via `npm audit`, including a Nodemailer SSRF flaw.

### [Left2Serve — Food Redistribution Platform](https://github.com/Susil-commits/Left2Serve)
`React.js` `TypeScript` `Node.js` `Express.js` `PostgreSQL` `Tailwind CSS` `Socket.io`

- Resolved race conditions with `SERIALIZABLE` transactions; compound B-tree SQL index cut query latency from 340ms to 12ms (96%).
- Validated `express-rate-limit` under 19K+ requests at 187 req/sec — 18K+ excess requests blocked.
- 100% Jest/Supertest coverage on auth and reservation flows, 85% overall.
- Real-time Socket.io chat, a smart donor–NGO–volunteer matching engine, and web push notifications.
- Self-healing notification delivery: exponential-backoff retry plus a hand-rolled circuit breaker (closed/open/half-open).

### [MyMate — Driver Booking Platform](https://github.com/Susil-commits/MyMate)
`React.js` `TypeScript` `Node.js` `Express.js` `MongoDB` `Tailwind CSS` `Tesseract.js`

- Fixed a production Socket.IO race condition by re-sequencing transactional writes to commit before event emission.
- Load-tested at 200 concurrent users (115 req/sec) while blocking 3,000+ excess requests via rate limiting.
- MongoDB compound indexing on search fields cut query time to ~1ms.
- Live WebSocket location tracking, AI-heuristic driver matching, and Tesseract.js OCR for license KYC verification.
- Driver-matching scoring rewritten as pure, side-effect-free functions, with a parallel Haskell proof-of-concept.

<br>

## Experience

**Backend Developer Intern**, Techgeering Solutions Pvt. Ltd. — Oct '25 to Feb '26
Built 5+ reusable UI/API components for a real-time video-handling platform on the MERN stack; resolved 20+ bugs across the SDLC in an Agile/Scrum team of 4.

<br>

## Certifications

- Oracle Certified Foundations Associate (Agentic AI) — 1Z0-1157-26, 88%
- NPTEL — Software Testing
- NPTEL — IoT 4.0
- NASSCOM FutureSkills Prime — Big Data Technology (Gold)

<br>

<div align="center">

**Cuttack, Odisha, India**

</div>
