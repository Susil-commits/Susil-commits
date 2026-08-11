<div align="center">

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,50:1e3a5f,100:0f172a&height=220&section=header&text=Susil%20Kumar%20Nayak&fontSize=46&fontColor=ffffff&fontAlignY=38&desc=Backend-Focused%20Full-Stack%20Developer%20%C2%B7%20B.Tech%20CSE%20'26&descSize=18&descAlignY=58&animation=fadeIn"/>

<a href="https://github.com/Susil-commits">
  <img src="https://readme-typing-svg.demolab.com/?lines=Shipping+REST+APIs+that+hold+up+under+load;200%2B+concurrent+users+%C2%B7+sub-150ms+p95+latency;Race+conditions+%E2%86%92+resolved.+Indexes+%E2%86%92+tuned.;Currently+leveling+up+in+Haskell+%2F+FP;&font=Fira+Code&center=true&width=650&height=40&color=38BDF8&vCenter=true&size=20&pause=1800"/>
</a>

<br>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/susil-kumar-nayak-5180472b6)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:nayaksushil298@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Susil-commits)

</div>

<br>

## Focus

Three independently built platforms, each pushed through load testing and fixed for the failure modes that actually show up in production — race conditions, N+1 queries, retry storms, duplicate writes. Currently building functional-programming fundamentals in **Haskell** to bring FP discipline (pure functions, no shared state) into backend design.

<br>

## Tech Stack

<div align="center">

**Languages**
<br>
<img src="https://skillicons.dev/icons?i=py,js,ts,cpp,java,haskell" />

**Backend & APIs**
<br>
<img src="https://skillicons.dev/icons?i=nodejs,express,socketio" />

**Databases**
<br>
<img src="https://skillicons.dev/icons?i=mongodb,postgres,mysql" />

**Reliability & Testing**
<br>
<img src="https://skillicons.dev/icons?i=jest" />
![Supertest](https://img.shields.io/badge/Supertest-25D366?style=flat-square)
![Artillery](https://img.shields.io/badge/Artillery-FF4F00?style=flat-square)

**Cloud & DevOps**
<br>
<img src="https://skillicons.dev/icons?i=aws,docker,git,github" />

**Frontend**
<br>
<img src="https://skillicons.dev/icons?i=react,tailwind,html" />

</div>

<br>

## Projects

<table>
<tr>
<td width="50%" valign="top">

### [FaRm — Farmer-to-Consumer Marketplace](https://github.com/Susil-commits/FarmDirect)
`React.js` `TypeScript` `Node.js` `Express.js` `MongoDB` `Tailwind CSS` `Artillery`

- Load-tested at 200 concurrent users — sub-150ms p95 latency, 0% error rate.
- Cut filter query latency from ~240ms to ~12ms (95%) via MongoDB compound indexing.
- Migrated the entire backend from JavaScript to TypeScript for full type safety.
- Idempotency-key duplicate-request protection on checkout: Mongo unique constraint + atomic transaction + cached response replay.
- Rolling-average / z-score anomaly detection on order transactions — flags abnormal orders without an ML model.
- Patched all high/critical dependency vulnerabilities via `npm audit`, including a Nodemailer SSRF flaw.

</td>
<td width="50%" valign="top">

### [Left2Serve — Food Redistribution Platform](https://github.com/Susil-commits/Left2Serve)
`React.js` `TypeScript` `Node.js` `Express.js` `PostgreSQL` `Tailwind CSS` `Socket.io`

- Resolved race conditions with `SERIALIZABLE` transactions; compound B-tree SQL index cut query latency from 340ms to 12ms (96%).
- Validated `express-rate-limit` under 19K+ requests at 187 req/sec — 18K+ excess requests blocked.
- 100% Jest/Supertest coverage on auth and reservation flows, 85% overall.
- Real-time Socket.io chat, a smart donor–NGO–volunteer matching engine, and web push notifications.
- Self-healing notification delivery: exponential-backoff retry plus a hand-rolled circuit breaker (closed/open/half-open).

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [MyMate — Driver Booking Platform](https://github.com/Susil-commits/MyMate)
`React.js` `TypeScript` `Node.js` `Express.js` `MongoDB` `Tailwind CSS` `Tesseract.js`

- Fixed a production Socket.IO race condition by re-sequencing transactional writes to commit before event emission.
- Load-tested at 200 concurrent users (115 req/sec) while blocking 3,000+ excess requests via rate limiting.
- MongoDB compound indexing on search fields cut query time to ~1ms.
- Live WebSocket location tracking, AI-heuristic driver matching, and Tesseract.js OCR for license KYC verification.
- Driver-matching scoring rewritten as pure, side-effect-free functions, with a parallel Haskell proof-of-concept.

</td>
<td width="50%" valign="top">

### Experience

**Backend Developer Intern**
Techgeering Solutions Pvt. Ltd. — Oct '25 to Feb '26

Built 5+ reusable UI/API components for a real-time video-handling platform on the MERN stack; resolved 20+ bugs across the SDLC in an Agile/Scrum team of 4.

### Certifications
- Oracle Certified Foundations Associate (Agentic AI) — 88%
- NPTEL — Software Testing
- NPTEL — IoT 4.0
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
