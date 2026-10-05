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

## 🚧 Currently Building

| Project | Stack | Status |
| --- | --- | --- |
| [CleanNation](https://github.com/darunbjork/cleannation) | Bun · Fastify · Prisma · PostgreSQL (per-service) · Redis · Kafka | 🟡 In progress |
| [voice-agent](https://github.com/darunbjork/voice-agent) · [Live ↗](https://voice-agent-nine-self.vercel.app) | Fastify 5 · TypeScript · Deepgram · Gemini · ElevenLabs | 🟢 Shipped |
| [Smart Home Frontend](https://github.com/darunbjork/smart-home-frontend) | React · TypeScript · Socket.io · Tailwind | 🟡 In progress |

> 🟢 Shipped · 🟡 In progress · 🔴 Planned

---

## 🚀 Featured Projects

### [darun.dev](https://github.com/darunbjork/darun.dev) · [Live ↗](https://darun-dev.pages.dev)

`Fastify 5` `Prisma 7` `PostgreSQL` `Redis` `Gemini API` `React` `Tailwind` `Turborepo`

- **Hybrid RAG chat over my own CV and project READMEs** — ask what I've shipped recently and it answers grounded in the actual docs.
- **Self-maintaining embeddings** — a GitHub webhook pipeline (`@octokit/webhooks`) re-embeds content automatically when project READMEs change.
- **Admin CMS**, Argon2id password hashing, CSRF protection, JWT auth, shared TypeScript types across a Turborepo monorepo.
- **Structured Gemini chat** with Zod-validated output.
- **ATS source aggregation** (Greenhouse, Lever, Ashby, Adzuna) with Redis caching and AI-scored matching against my CV, generating tailored pitches.
- Frontend built with React, Tailwind, GSAP, Radix UI, TanStack Query, React Hook Form.

---

### [voice-agent](https://github.com/darunbjork/voice-agent) · [Live ↗](https://voice-agent-nine-self.vercel.app)

`Fastify 5` `TypeScript` `PostgreSQL` `Redis` `WebSocket` `Deepgram` `Gemini` `ElevenLabs`

- **Real-time three-provider voice pipeline** — Deepgram handles streaming speech-to-text, Gemini handles reasoning, ElevenLabs handles text-to-speech, coordinated over a persistent WebSocket connection.
- **Per-provider circuit breakers with graceful degradation** — if the speech-to-text circuit opens, the session falls back to text input instead of dropping.
- **Production observability** — Sentry error tracking, a scripted accessibility baseline (axe-core), and dedicated latency instrumentation.
- **Daily token ceiling** with pre-flight budget checks per Gemini/ElevenLabs call — returns 429 once exceeded, alerts at 80%.
- **Status:** shipped.

---

### [Research Assistant Platform](https://github.com/darunbjork/research-assistant-platform)

`Express` `TypeScript` `PostgreSQL/pgvector` `Redis` `Gemini API` `Docker` `OpenTelemetry`

- **Hybrid retrieval & grounded AI** — pgvector cosine similarity + BM25 keyword search merged via Reciprocal Rank Fusion (RRF) for cited, grounded answers.
- **Multi-node agent workflow** — classify → retrieve/tool-use → evaluate, with automated quality scoring and retry logic on low-confidence answers.
- **Load-tested** — Artillery suite covering baseline, ramp-up, cache-warming, spike, sustained-load, and WebSocket scenarios.
- **640+ Jest tests, 82% line coverage in CI.**
- **Status:** built and validated locally, deployment in progress.

---

### [CleanNation](https://github.com/darunbjork/cleannation)

`Bun` `Fastify` `Prisma` `PostgreSQL (database-per-service)` `Redis` `Kafka`

- **Event-driven microservices** — seven independent services (auth, event, location, media, gamification, notification, payment), each with its own database.
- **Argon2id password hashing**, JWT auth, Redis-backed rate limiting.
- **Status:** in progress.

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
| [my-portfolio-os](https://github.com/darunbjork/my-portfolio-os) + [portfolio-ui](https://github.com/darunbjork/portfolio-ui) | My previous portfolio — superseded by darun.dev | Express · MongoDB · Redis · Cloudinary · React · Tailwind |
| [DevQuiz](https://github.com/darunbjork/DevQuiz) + [API](https://github.com/darunbjork/devquiz-api) | AI quiz platform with an analytics dashboard | React · Vite · Recharts · Bun · Fastify · MongoDB · Gemini |
| [Smart Home Frontend](https://github.com/darunbjork/smart-home-frontend) | Dashboard for the Smart Home API | React · TypeScript · Socket.io · Recharts |
| [Chat App](https://github.com/darunbjork/chat-app) | Mobile messaging with maps and image sharing | React Native · Expo · Firebase |
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

**AI / LLM — production**
`Gemini API` (5 projects) · `Deepgram` (voice-agent) · `ElevenLabs` (voice-agent) · `RAG` · `Agentic workflows` · `Prompt Engineering`

**AI APIs explored** *(not in shipped code)*
`DeepSeek` `Grok` `GroqCloud`

**Databases & Messaging**
`PostgreSQL` `pgvector` `Prisma` `MongoDB` `Mongoose` `Redis` `Firebase` `MQTT` `WebSockets` `Kafka` `RabbitMQ`

**DevOps & Testing**
`Docker` `GitHub Actions` `Git` `Vitest` `Jest` `Testing Library` `Supertest` `Artillery` `Render` `Vercel` `Cloudflare Pages`

**Security**
`JWT/RBAC` `Argon2id` `bcrypt` `Helmet` `CSRF Protection` `Multi-tenant Isolation`

---

## 📚 Currently Exploring

- 🧠 Agentic systems at scale — multi-service orchestration, event-driven architecture (CleanNation)
- 🎙️ Multi-provider real-time pipelines — circuit breaking and graceful degradation across services (voice-agent)
- ☁️ Cloud-native deployment — Kubernetes fundamentals, horizontal scaling
- 🧪 Contract testing and integration patterns across service boundaries

---

## 📊 GitHub Stats

![Darun's GitHub Stats](https://github-stats-extended.vercel.app/api?username=darunbjork&show_icons=true&theme=dark&hide_border=true&count_private=true)
![Top Languages](https://github-stats-extended.vercel.app/api/top-langs/?username=darunbjork&layout=compact&theme=dark&hide_border=true)

---

## 🔥 Streak

> I build every day — see the graph below.

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
