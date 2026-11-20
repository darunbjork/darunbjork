# 👋 Hi, I'm Darun Mustafa

Full-stack developer shipping production systems in React/TypeScript,
Node.js/Fastify/Express, Bun, PostgreSQL, MongoDB, and Docker — with a
consistent focus on auth security, API contract design, real-time data,
and production AI integration across five projects.

- 🌍 Stockholm, Sweden
- 📧 darunbjork@gmail.com
- 🎓 Fullstack Developer — Chas Academy (2025–2027)
- 💼 Open to Full-Stack, Backend, and AI Engineering roles
- 🔗 Portfolio: https://darun-dev.pages.dev

---

## 🟢 Live in Production

| Project | What it is | Stack | Live |
| --- | --- | --- | --- |
| [ResearchBot](https://github.com/darunbjork/research-assistant-platform) | Agentic RAG — ask questions about your own documents, get cited answers | Express · TypeScript · pgvector · Redis · Gemini · k3s | [Live ↗](https://research.voxcript.app) |
| [Voxcript](https://github.com/darunbjork/voxcript) | Upload a short video, get subtitles — transcribed locally with Whisper | Fastify · TypeScript · PostgreSQL · whisper.cpp · ffmpeg · k3s | [Live ↗](https://cdn.voxcript.app) |
| [voice-agent](https://github.com/darunbjork/voice-agent) | Real-time voice assistant: speech-to-text → reasoning → speech | Fastify 5 · TypeScript · Deepgram · Gemini · ElevenLabs | [Live ↗](https://voice-agent-nine-self.vercel.app) |
| [darun.dev](https://github.com/darunbjork/darun.dev) | My portfolio, with a RAG chat grounded in my own CV and projects | Fastify 5 · Prisma · PostgreSQL · Redis · Gemini · React | [Live ↗](https://darun-dev.pages.dev) |
| [Smart Home Automation API](https://github.com/darunbjork/smart-home-automation-api) | IoT backend with MQTT, real-time state and AI device commands | Node.js · TypeScript · MongoDB · MQTT · Socket.io · Gemini | [Live Demo ↗](https://smart-home-api-c9r8.onrender.com/) *(wakes in ~30s)* |
| [DevQuiz](https://github.com/darunbjork/DevQuiz) + [API](https://github.com/darunbjork/devquiz-api) | AI quiz platform with an analytics dashboard | React · Vite · Recharts · Bun · Fastify · MongoDB · Gemini | [Live ↗](https://dev-quiz-2stl.vercel.app/) *(wakes in ~30s)* |

ResearchBot and Voxcript run side by side on the same self-managed k3s cluster.

---

## 🚀 Featured Projects

### [ResearchBot — Research Assistant Platform](https://github.com/darunbjork/research-assistant-platform) · [Live ↗](https://research.voxcript.app)

`Express` `TypeScript` `PostgreSQL + pgvector` `Prisma` `Redis` `Bull` `Gemini API` `WebSocket` `OpenTelemetry` `Docker` `k3s`

- **Hybrid retrieval & grounded AI** — pgvector cosine similarity + BM25 keyword search merged with Reciprocal Rank Fusion (RRF), so every answer cites its evidence.
- **ReAct agent engine** — one shared reasoning loop behind both HTTP and WebSocket transports, with tool use, cancellation and live step streaming.
- **Voice layer** — Deepgram streaming speech-to-text and ElevenLabs spoken answers with barge-in (works locally; off in the public demo to avoid paid-API costs).
- **Production deployment** — k3s, Traefik + cert-manager TLS, NetworkPolicies, least-privilege deploy user; CI → images pinned by digest → migrations → smoke test → automatic rollback.
- **Observability & testing** — Prometheus metrics and Grafana dashboards, Artillery load tests, ~970 automated tests, ~81% backend coverage in CI.

---

### [Voxcript — AI subtitle generation](https://github.com/darunbjork/voxcript) · [Live ↗](https://cdn.voxcript.app)

`Fastify 5` `TypeScript` `Prisma` `PostgreSQL 16` `React` `Vite` `whisper.cpp` `ffmpeg` `k3s` `Traefik` `cert-manager`

- **Local AI inference** — whisper.cpp runs inside the worker image; no external transcription API, so no per-minute cost and no audio leaves the server.
- **Async job pipeline** — the API answers immediately; a worker claims jobs from a Postgres-backed queue with `FOR UPDATE SKIP LOCKED`. Concurrency tests prove exactly one winner when five workers race for one job.
- **Safe uploads** — ffprobe validates format, duration, resolution and audio track; each job's SRT is downloadable only with a per-job access token.
- **Zero-downtime deploys** — CI → images pushed by immutable digest → rolling update (`maxUnavailable: 0`); 900 requests, 0 failures during a live rollout. API autoscales 2→4 pods.
- **Operated like production** — kube-prometheus-stack monitoring, daily `pg_dump` backups to Cloudflare R2; unit (Vitest), integration (real Postgres) and E2E (Playwright with real whisper.cpp) tests.

---

### [voice-agent](https://github.com/darunbjork/voice-agent) · [Live ↗](https://voice-agent-nine-self.vercel.app)

`Fastify 5` `TypeScript` `PostgreSQL` `Redis` `WebSocket` `Deepgram` `Gemini` `ElevenLabs`

- **Real-time three-provider voice pipeline** — Deepgram handles streaming speech-to-text, Gemini handles reasoning, ElevenLabs handles text-to-speech, coordinated over a persistent WebSocket connection.
- **Per-provider circuit breakers with graceful degradation** — if the speech-to-text circuit opens, the session falls back to text input instead of dropping.
- **Production observability** — Sentry error tracking, a scripted accessibility baseline (axe-core), and dedicated latency instrumentation.
- **Daily token ceiling** with pre-flight budget checks per Gemini/ElevenLabs call — returns 429 once exceeded, alerts at 80%.

---

### [darun.dev](https://github.com/darunbjork/darun.dev) · [Live ↗](https://darun-dev.pages.dev)

`Fastify 5` `Prisma 7` `PostgreSQL` `Redis` `Gemini API` `React` `Tailwind` `Turborepo`

- **Hybrid RAG chat over my own CV and project READMEs** — ask what I've shipped recently and it answers grounded in the actual docs.
- **Self-maintaining embeddings** — a GitHub webhook pipeline (`@octokit/webhooks`) re-embeds content automatically when project READMEs change.
- **Admin CMS**, Argon2id password hashing, CSRF protection, JWT auth, shared TypeScript types across a Turborepo monorepo.
- **Structured Gemini chat** with Zod-validated output.
- **ATS source aggregation** (Greenhouse, Lever, Ashby, Adzuna) with Redis caching and AI-scored matching against my CV, generating tailored pitches.
- Frontend built with React, Tailwind, GSAP, Radix UI, TanStack Query, React Hook Form.

---

### [Smart Home Automation API](https://github.com/darunbjork/smart-home-automation-api) · [Live Demo ↗](https://smart-home-api-c9r8.onrender.com/)

`Node.js` `TypeScript` `MongoDB` `MQTT` `Socket.io` `Gemini API` `JWT/RBAC` `Docker` `Swagger`

- **Full IoT real-time loop** — a self-hosted MQTT broker (`aedes`) handles device commands; Socket.io fans state to all clients in <30ms.
- **Server-side Gemini integration** for natural-language device commands.
- **Tenant isolation** — RBAC + household-scoped middleware; cross-tenant data access is structurally blocked.
- Structured logging (`pino`), rate limiting, input validation.

---

## 🗂 Also Built

| Project | Description | Stack |
| --- | --- | --- |
| [my-portfolio-os](https://github.com/darunbjork/my-portfolio-os) + [portfolio-ui](https://github.com/darunbjork/portfolio-ui) · [Live ↗](https://myportfolio-ui.netlify.app/) *(wakes in ~60s)* | My previous portfolio (shipped) — superseded by darun.dev | Express · MongoDB · Redis · Cloudinary · React · Tailwind |
| [Chat App](https://github.com/darunbjork/chat-app) | Mobile messaging with maps and image sharing | React Native · Expo · Firebase |
| [InsightAPI](https://github.com/darunbjork/InsightAPI) | Social platform backend — auth, posts, user relationships | Node.js · Express · MongoDB |
| [QuickServe](https://github.com/darunbjork/quickserve) | Distributed, event-driven fast-food ordering system (Chas Academy exam) | TypeScript · React · RabbitMQ · PostgreSQL · Docker |

---

## 🚧 Work in Progress

Not shipped yet. These are the projects I'm still building.

| Project | What I'm building | Stack |
| --- | --- | --- |
| [CleanNation](https://github.com/darunbjork/cleannation) | Event-driven microservices — seven services (auth, event, location, media, gamification, notification, payment), each with its own database; Argon2id, JWT, Redis rate limiting | Bun · Fastify · Prisma · PostgreSQL (per-service) · Redis · Kafka |
| [Smart Home Frontend](https://github.com/darunbjork/smart-home-frontend) | Real-time dashboard for the Smart Home Automation API | React · TypeScript · Socket.io · Tailwind |

---

## 🤖 AI-Assisted Development

I use AI tools — **Grok, Claude, and Codex** — as part of my daily workflow:
scaffolding, refactoring, and reviewing. I verify what they produce by
reading the diff, running the tests, and checking edge cases before
anything ships. Generated code still has to pass CI, and I own what I merge.

---

## 🛠 Skills

**Frontend**
`React` `TypeScript` `JavaScript` `Tailwind CSS` `Zustand` `React Native` `Vite` `GSAP` `Radix UI` `TanStack Query` `React Hook Form`

**Data Visualization**
`Recharts`

**Backend**
`Node.js` `Fastify` `Express` `Bun` `REST` `Swagger/OpenAPI` `Zod`

**AI / LLM — production**
`Gemini API` (darun.dev, voice-agent, ResearchBot, Smart Home API, DevQuiz) · `whisper.cpp` (Voxcript, local inference) · `Deepgram` (voice-agent) · `ElevenLabs` (voice-agent) · `RAG` · `Agentic workflows` · `Prompt Engineering`

**AI APIs explored** *(not in shipped code)*
`DeepSeek` `Grok` `GroqCloud`

**Databases & Messaging**
`PostgreSQL` `pgvector` `Prisma` `MongoDB` `Mongoose` `Redis` `Firebase` `MQTT` `WebSockets` `Kafka` `RabbitMQ`

**DevOps & Infrastructure**
`Docker` `Kubernetes (k3s)` `Traefik` `cert-manager` `Prometheus` `Grafana` `GitHub Actions` `Git` `Cloudflare (DNS, R2, Pages)` `Hetzner` `Render` `Vercel`

**Testing**
`Vitest` `Jest` `Testing Library` `Supertest` `Playwright` `Artillery` `k6`

**Security**
`JWT/RBAC` `Argon2id` `bcrypt` `Helmet` `CSRF Protection` `Multi-tenant Isolation` `NetworkPolicies` `Least-privilege deploy credentials`

---

## 📚 Currently Exploring

- 🧠 Agentic systems at scale — multi-service orchestration, event-driven architecture (CleanNation)
- 🎙️ Multi-provider real-time pipelines — circuit breaking and graceful degradation across services (voice-agent)
- ☁️ Kubernetes beyond one node — high availability, object storage instead of host volumes, GitOps
- 🧪 Contract testing and integration patterns across service boundaries

---

## 📊 Top Languages

![Top Languages](https://github-stats-extended.vercel.app/api/top-langs/?username=darunbjork&layout=compact&theme=dark&hide_border=true)

---

## 🔥 Streak

> I build consistently — see the graph below.

![GitHub Streak](https://streak-stats.demolab.com?user=darunbjork&theme=dark&hide_border=true)

---

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/darun-mustafa/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat&logo=cloudflare&logoColor=white)](https://darun-dev.pages.dev)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:darunbjork@gmail.com)

---

## 📚 Education

**Fullstack Developer — Open Source Track** · Chas Academy, Stockholm
`Sep 2025 – Jun 2027`

**Full-Stack Web Development Certificate** · CareerFoundry (Remote)
`Jun 2023 – Aug 2024`

**Business Administration Diploma** · Choman Technical Institute, Iraq
`2011 – 2013` · Evaluated by UHR Sweden as equivalent to SeQF Level 5

---

*⚡ Design for failure before you design for features.*
