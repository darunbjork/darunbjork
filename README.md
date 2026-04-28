# 👋 Hi, I'm Darun Mustafa

Full-stack developer shipping production systems in React/TypeScript,
Node.js/Fastify, PostgreSQL, MongoDB, and Docker — with a consistent
focus on auth security, API contract design, and real-time data.

Six years coordinating complex operations under pressure built one rule:
**design for failure before you design for features** — I bring the same
precision regulators required in documentation to every codebase I touch.

> Specialising in production LLM integrations — structured prompt
> pipelines, output validation, and AI-powered full-stack backends.

🌍 Stockholm, Sweden
📧 darunbjork@gmail.com
🎓 Fullstack Developer — Chas Academy (2025–2027)
💼 Open to Full-Stack, Frontend, and Backend roles
🔗 Portfolio: https://myportfolio-ui.netlify.app

---

## 🚧 Currently Building

| Project                                                                                  | Stack                                     | Status        |
| ---------------------------------------------------------------------------------------- | ----------------------------------------- | ------------- |
| [Research Assistant Platform](https://github.com/darunbjork/research-assistant-platform) | React · Fastify · Gemini · RAG · Pinecone | 🟡 In progress |
| [Task Manager API](https://github.com/darunbjork/task-manager-api)                       | Bun · Fastify · PostgreSQL · Prisma       | 🟡 In progress |
| [Smart Home Frontend](https://github.com/darunbjork/smart-home-frontend)                 | React · TypeScript · Socket.io · Tailwind | 🟡 In progress |

> 🟢 Shipped · 🟡 In progress · 🔴 Planned

---

## 🚀 Featured Projects

### [Smart Home Automation API](https://github.com/darunbjork/smart-home-automation-api) · [Live Demo ↗](https://smart-home-api-c9r8.onrender.com/)
`Node.js` `TypeScript` `MongoDB` `MQTT` `Socket.io` `JWT/RBAC` `Docker` `GitHub Actions` `Swagger`

- **Full IoT real-time loop** — MQTT handles device commands; Socket.io fans state to all clients in <30 ms; closed-loop simulator validates the full device ↔ API ↔ client flow
- **Production-hardened deploy** — multi-stage Dockerfile, multi-platform image (linux/amd64 + linux/arm64), GitHub Actions CI, Swagger /api-docs, live on Render
- **Zero cross-tenant leakage** — RBAC + household-scoped middleware at the route layer; users physically cannot read or write another tenant's devices

---

### [DevQuiz — AI Quiz Platform](https://github.com/darunbjork/DevQuiz)
`React` `TypeScript` `Gemini API` `Bun` `Fastify` `PostgreSQL` `FastAPI` `Docker`

- **Structured prompt engineering** — micro-step prompt pipelines + output validation cut off-format Gemini responses by ~85% vs unstructured prompting
- **Resumable sessions** — PostgreSQL-persisted quiz state with JWT accounts; users resume mid-session with zero data loss on reconnect

---

### [Portfolio Management System](https://github.com/darunbjork/my-portfolio-os) · [Live Demo ↗](https://my-portfolio-gr2e.onrender.com/)
`React` `TypeScript` `Tailwind` `Zustand` `Axios` `Node.js` `MongoDB` `Cloudinary` `JWT`

- **Hardened file upload pipeline** — MIME type + size validation at middleware; invalid payloads blocked before reaching Cloudinary
- **Production-scale frontend patterns** — Zustand global auth state, Axios interceptor token refresh, abstracted API service layer

---

## 🗂 Also Built

| Project                                                                  | Description                                                            | Stack                                     |
| ------------------------------------------------------------------------ | ---------------------------------------------------------------------- | ----------------------------------------- |
| [DevQuiz API](https://github.com/darunbjork/devquiz-api)                 | Backend for AI quiz generation with Gemini, JWT auth, and Swagger docs | Bun · Fastify · MongoDB · Gemini          |
| [InsightAPI](https://github.com/darunbjork/InsightAPI)                   | Social platform backend — auth, posts, user relationships              | Node.js · Express · MongoDB               |
| [Developer Portfolio](https://github.com/darunbjork/developer-portfolio) | Responsive SPA with GSAP animations and Node.js contact backend        | HTML · CSS · JavaScript · Node.js         |

---

## 🛠 Skills

**Frontend**
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)

**Backend**
![Node.js](https://img.shields.io/badge/Node.js-43853D?style=flat&logo=node.js&logoColor=white)
![Fastify](https://img.shields.io/badge/Fastify-000000?style=flat&logo=fastify&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-404D59?style=flat)
![Bun](https://img.shields.io/badge/Bun-000000?style=flat&logo=bun&logoColor=white)

**AI & Prompt Engineering**
![Gemini](https://img.shields.io/badge/Gemini_LLM-4285F4?style=flat&logo=google&logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt_Engineering-FF6B6B?style=flat)
![LLM Integration](https://img.shields.io/badge/LLM_Integration-7C3AED?style=flat)

**Databases**
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat&logo=mongodb&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=flat&logo=firebase&logoColor=white)

**DevOps & Tooling**
![Docker](https://img.shields.io/badge/Docker-0DB7ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)
![Jest](https://img.shields.io/badge/Jest-323330?style=flat&logo=jest&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=swagger&logoColor=black)
![Netlify](https://img.shields.io/badge/Netlify-00C7B7?style=flat&logo=netlify&logoColor=white)
![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=white)

**APIs & Protocols**
![REST](https://img.shields.io/badge/REST_API-FF6C37?style=flat)
![WebSockets](https://img.shields.io/badge/WebSockets-010101?style=flat)
![MQTT](https://img.shields.io/badge/MQTT-660066?style=flat)
![JWT](https://img.shields.io/badge/JWT/RBAC-000000?style=flat&logo=jsonwebtokens&logoColor=white)

---

## 📚 Currently Learning

- 🔬 RAG architecture — retrieval pipelines, vector search, embedding strategies
- 🤖 AI agent design — tool-calling, multi-step reasoning, memory management
- ☁️ Cloud-native deployment — Kubernetes fundamentals, scaling strategies
- 🧪 Advanced backend testing — integration and contract testing patterns

---

## 📊 GitHub Stats

![Darun's GitHub Stats](https://github-readme-stats.vercel.app/api?username=darunbjork&show_icons=true&theme=dark&hide_border=true&count_private=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=darunbjork&layout=compact&theme=dark&hide_border=true)

---

## 🔥 Streak

> 1,622 contributions and counting — I build every day.

![GitHub Streak](https://streak-stats.demolab.com?user=darunbjork&theme=dark&hide_border=true)

---

## 🤝 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/darun-mustafa/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat&logo=netlify&logoColor=white)](https://myportfolio-ui.netlify.app)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:darunbjork@gmail.com)

---

## 📚 Education

**Fullstack Developer — Open Source Track** · Chas Academy, Stockholm
`Sep 2025 – Jun 2027` · Full-stack development, DevOps, cloud-native architecture

**Full-Stack Web Development Certificate** · CareerFoundry (Remote)
`Jun 2023 – Aug 2024` · Frontend, backend, databases, deployment

**Business Administration Diploma** · Choman Technical Institute, Iraq
`2011 – 2013` · Evaluated by UHR Sweden as equivalent to SeQF Level 5

---

*⚡ Design for failure before you design for features.*