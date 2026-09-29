<div align="center">
<img src="https://readme-typing-svg.demolab.com?font=Inconsolata&weight=500&size=44&duration=4000&pause=300&color=0969DA&center=true&vCenter=true&multiline=true&repeat=false&width=1100&height=120&lines=Hey+there;I'm+Mustafa+%E2%80%94+AI+agent+%26+backend+engineer+%E2%9A%A1" width="90%" />
<br>
<img src="./assets/gojo.gif" width="55%" alt="Gojo — Hollow Purple" />
<br><br>
<pre>
    💼 AI Agent Engineer • Backend Systems & Production AI
    🤖 Claude API • LangGraph • RAG • guardrails • evals • prompt-injection testing
    🦀 Rust • Python • Go • TypeScript
    🗄️ PostgreSQL (RLS) • Redis • pgvector • SQL
    ☁️ AWS • Oracle Cloud • Docker • Kubernetes • Terraform • Argo CD
    📍 Lahore, PK 🇵🇰 • Remote (GMT+5)
</pre>
<br>

[![](https://img.shields.io/badge/linkedin-0a66c2)](https://www.linkedin.com/in/musishere/)
[![](https://img.shields.io/badge/email-24292f)](mailto:mustafabukhari333@gmail.com)
[![](https://img.shields.io/badge/github-181717)](https://github.com/musishere)
[![](https://img.shields.io/badge/portfolio-6E56CF)](https://mustafa-ahmad-olive.vercel.app)

</div>

## 🎮 Khel — turf-booking marketplace

Co-founder, backend & systems. Go (`chi` / `fiber`).

- Reservation engine handling booking conflicts, payment deadlines and partial payments, directly shaping booking-to-revenue conversion
- Peer-to-peer split-payment system built in-house, replacing the third-party gateway: lower transaction cost, one less external dependency
- AI-assisted ELO rating system tracking player performance across matches to power skill-based matchmaking
- Gamification (badges, streaks) to drive retention

## 🚪 LLM Gateway — one front door between apps and Claude

Python · FastAPI · Redis · Terraform · Argo CD. Built one layer at a time.

**🔐 Auth and metering**
- FastAPI proxy in front of the Claude API; the official Anthropic SDK works through it without code changes
- Per-tenant API keys, stored only as hashes
- Every call writes a usage row: tokens, cost, latency and outcome

**🌊 Streaming, metered honestly**
- Relays SSE chunks to the client while reading token counts from the stream events
- Mid-stream disconnects used to leave usage empty, so hanging up early meant free output tokens. The gateway now estimates output tokens and labels the row `client_disconnected`

**⏱️ Rate limits and quotas in Redis**
- Per-tenant token bucket plus a monthly token quota, both as atomic Lua scripts
- Fixed a check-then-write race (20 concurrent requests all saw the old count and got through) with reserve-then-settle accounting, like a card hold at a hotel
- Result: 20 concurrent requests with 100 tokens left → 4 admitted, 0 overshoot

**☁️ Infrastructure**
- Terraform on Oracle Cloud: remote state in a versioned bucket, budget alerts, VCN with public and private subnets, OKE cluster
- Free ARM nodes were out of capacity, so the containerized gateway ships via Argo CD GitOps to a local cluster; moving to the cloud is just a new cluster target

**Next:** CI/CD with canary releases → SLOs and burn-rate alerts → self-hosted model on vLLM with cost-aware routing

## 🛡️ Compliance Copilot — GitHub & AWS APIs

- Agent that checks GitHub and AWS settings against SOC 2, GDPR and HIPAA controls and cites the exact evidence behind every finding
- Drafts remediation fixes that wait for human approval before any change is applied

## 🧰 Stack

<div align="center">

**Languages**

![Rust](https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Go](https://img.shields.io/badge/Go-00ADD8?logo=go&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

**AI / Agent Engineering**

![Claude API](https://img.shields.io/badge/Claude%20API-D97757?logo=anthropic&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?logo=langgraph&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-6E56CF)
![pgvector](https://img.shields.io/badge/pgvector-336791)
![PaddleOCR](https://img.shields.io/badge/PaddleOCR-0062B0)
![Structured Outputs](https://img.shields.io/badge/Structured%20Outputs-555555)
![Agent Evals](https://img.shields.io/badge/Agent%20Evals-555555)
![Prompt Injection Testing](https://img.shields.io/badge/Prompt%20Injection%20Testing-555555)
![Human in the Loop](https://img.shields.io/badge/Human--in--the--Loop-555555)

**Backend & Data**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?logo=nodedotjs&logoColor=white)
![NestJS](https://img.shields.io/badge/NestJS-E0234E?logo=nestjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?logo=express&logoColor=white)
![chi](https://img.shields.io/badge/chi-00ADD8?logo=go&logoColor=white)
![fiber](https://img.shields.io/badge/fiber-00ADD8?logo=go&logoColor=white)
![sqlx](https://img.shields.io/badge/sqlx-000000?logo=rust&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20(RLS)-4169E1?logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?logo=redis&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite&logoColor=white)

**Cloud & Infra**

![AWS](https://img.shields.io/badge/AWS-232F3E?logo=amazonwebservices&logoColor=white)
![Oracle Cloud](https://img.shields.io/badge/Oracle%20Cloud-F80000?logo=oracle&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-844FBA?logo=terraform&logoColor=white)
![Argo CD](https://img.shields.io/badge/Argo%20CD-EF7B4D?logo=argo&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)

**Frontend**

![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React%20Native-61DAFB?logo=react&logoColor=black)

</div>

## 📈 Activity

<div align="center">

<img height="160" alt="Stats" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=musishere&theme=default" />
<img height="160" alt="Languages" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=musishere&theme=default" />

<img width="100%" alt="Contribution activity" src="https://github-readme-activity-graph.vercel.app/graph?username=musishere&custom_title=Contribution%20Activity&bg_color=ffffff&color=1f2328&title_color=0969da&line=0969da&point=1f2328&area=true&area_color=0969da&hide_border=false&border_color=d0d7de&radius=8" />

</div>

---

<div align="center">

**BSc Computer Science · University of Lahore**

Reach me by [email](mailto:mustafabukhari333@gmail.com) or on [LinkedIn](https://www.linkedin.com/in/musishere/).

</div>
