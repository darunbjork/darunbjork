# 👋 Hi, I'm Darun Mustafa

Full-stack developer shipping production systems in React/TypeScript,
Node.js/Fastify/Express, Bun, PostgreSQL, MongoDB, and Docker — with a
consistent focus on auth security, API contract design, real-time data,
and production AI integration.

- 🌍 Stockholm, Sweden
- 📧 darunbjork@gmail.com
- 🎓 Fullstack Developer — Chas Academy (2025–2027)
- 💼 Open to Full-Stack, Backend, and AI Engineering roles
- 🔗 Portfolio: https://darun-dev.pages.dev

---

## 🚧 Currently Building

| Project | Stack | Status |
| --- | --- | --- |
| [CleanNation](https://github.com/darunbjork/cleannation) | Bun · Fastify 5 · Prisma 7 · PostgreSQL (database-per-service) · Redis · Kafka | 🟡 In progress |
| [Smart Home Frontend](https://github.com/darunbjork/smart-home-frontend) | React · TypeScript · Socket.io · Tailwind | 🟡 In progress |
| [voice-agent](https://github.com/darunbjork) | Fastify 5 · TypeScript — real-time streaming STT, structured LLM reasoning | 🟡 In progress |

> 🟢 Shipped · 🟡 In progress · 🔴 Planned

---

## 🚀 Featured Projects

### [darun.dev](https://github.com/darunbjork/darun.dev) · [Live ↗](https://darun-dev.pages.dev)

`Fastify 5` `Prisma 7` `PostgreSQL` `Redis` `Gemini API` `React` `Tailwind` `Turborepo`

- **Hybrid RAG chat over my own CV and project READMEs** — ask it what I've shipped recently and it answers grounded in the actual docs.
- **Self-maintaining embeddings** — a GitHub webhook pipeline (`@octokit/webhooks`) re-embeds content automatically when project READMEs change, no manual re-indexing.
- **Admin CMS** — manage project content, view analytics, without touching code.
- **Security** — Argon2id password hashing, CSRF protection, JWT auth via a shared Turborepo monorepo (`@darun/shared-types` across API and web).
- Frontend built with React, Tailwind, GSAP animations, Radix UI primitives, TanStack Query, and React Hook Form.

---

### [Research Assistant Platform](https://github.com/darunbjork/research-assistant-platform)

`Express` `TypeScript` `PostgreSQL/pgvector` `Redis` `Gemini API` `Docker` `OpenTelemetry`

- **Hybrid retrieval & grounded AI** — pgvector cosine similarity + BM25 keyword search merged via Reciprocal Rank Fusion (RRF) for cited, grounded answers.
- **Multi-node agent workflow** — classify → retrieve/tool-use → evaluate, with automated quality scoring and retry logic on low-confidence answers.
- **Observability** — OpenTelemetry tracing, Prometheus metrics, structured logging with daily rotation.
- **Load-tested** — Artillery suite covering baseline, ramp-up, cache-warming, spike, and sustained-load scenarios, plus dedicated WebSocket load tests.
- **640+ Jest tests, 82% line coverage in CI.**
- **Status:** built and validated locally, deployment in progress.

---

### [DevQuiz — AI Quiz Platform](https://github.com/darunbjork/DevQuiz) · [Live Demo ↗](https://dev-quiz-2stl.vercel.app/)

`React 19` `TypeScript` `Vite` `Vitest` `Testing Library` `Recharts` `Bun` `Fastify` `MongoDB` `Zod` `JWT` `Gemini API`

- **Analytics dashboard with Recharts** — performance-over-time line chart, accuracy donut chart, quick-stat cards.
- **Structured prompt engineering** — micro-step prompt pipelines + Zod output validation to keep Gemini responses on-format.
- **State: React Context**, not Redux — kept deliberately minimal for the app's size.
- **Real backend, not local-only** — JWT auth with refresh-token rotation, quiz generation and results persisted server-side in MongoDB.
- **Tested on both sides** — Vitest + Testing Library on the client, Vitest on the API.

---

### [Smart Home Automation API](https://github.com/darunbjork/smart-home-automation-api) · [Live Demo ↗](https://smart-home-api-c9r8.onrender.com/)

`Node.js` `TypeScript` `MongoDB` `MQTT` `Socket.io` `JWT/RBAC` `Docker` `GitHub Actions` `Swagger`

- **Full IoT real-time loop** — MQTT handles device commands; Socket.io fans state to all clients in <30ms.
- **Production-hardened deploy** — multi-stage Dockerfile, multi-platform image (linux/amd64 + linux/arm64), GitHub Actions CI, Swagger at `/api-docs`.
- **Tenant isolation** — RBAC + household-scoped middleware; cross-tenant data access is structurally blocked.

---

## 🗂 Also Built

| Project | Description | Stack |
| --- | --- | --- |
| [my-portfolio-os](https://github.com/darunbjork/my-portfolio-os) + [portfolio-ui](https://github.com/darunbjork/portfolio-ui) | My previous portfolio — superseded by darun.dev | Express · MongoDB · Redis · Cloudinary · React · Tailwind |
| [DevQuiz API](https://github.com/darunbjork/devquiz-api) | Standalone backend for DevQuiz — quiz generation, JWT auth, Swagger docs | Bun · Fastify · MongoDB · Gemini |
| [Chat App](https://github.com/darunbjork) | Real-time mobile messaging — Firestore listeners, push notifications | React Native · Expo · Firebase |
| [InsightAPI](https://github.com/darunbjork/InsightAPI) | Social platform backend — auth, posts, user relationships | Node.js · Express · MongoDB |
| [QuickServe](https://github.com/darunbjork/quickserve) | Distributed, event-driven fast-food ordering system (Chas Academy exam) | TypeScript · React · RabbitMQ · PostgreSQL · Docker |

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

**AI / LLM (production)**
`Gemini API` `RAG` `Agentic workflows` `Prompt Engineering` `Structured Output Validation`

**AI APIs explored** *(not yet confirmed as wired into shipped code)*
`DeepSeek` `Grok` `GroqCloud` `Deepgram`

**Databases & Messaging**
`PostgreSQL` `pgvector` `Prisma` `MongoDB` `Mongoose` `Redis` `Firebase` `MQTT` `WebSockets` `Kafka` `RabbitMQ`

**DevOps & Testing**
`Docker` `GitHub Actions` `Git` `Vitest` `Jest` `Testing Library` `Supertest` `Artillery` `Render` `Vercel` `Cloudflare Pages`

**Security**
`JWT/RBAC` `Argon2id` `bcrypt` `Helmet` `CSRF Protection` `Multi-tenant Isolation`

---

## 📚 Currently Exploring

- 🧠 Agentic systems at scale — multi-service orchestration, event-driven architecture (CleanNation)
- ☁️ Cloud-native deployment — Kubernetes fundamentals, horizontal scaling
- 🧪 Contract testing and integration patterns across service boundaries

---

## 📊 GitHub Stats

![Darun's GitHub Stats](https://github-stats-extended.vercel.app/api?username=darunbjork&show_icons=true&theme=dark&hide_border=true&count_private=true)
![Top Languages](https://github-stats-extended.vercel.app/api/top-langs/?username=darunbjork&layout=compact&theme=dark&hide_border=true)

---

## 🔥 Streak

> 1,622 contributions and counting — I build every day.

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
