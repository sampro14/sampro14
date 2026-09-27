<h1 align="center">Hi, I'm Sameer Atram 👋</h1>

<p align="center">
  <a href="https://github.com/sampro14">
    <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=22&pause=1200&color=2DD4BF&center=true&vCenter=true&width=640&lines=Applied+AI+Engineer;Agentic+AI+%C2%B7+Multi-Agent+Systems;Agent+Reliability+%26+Evaluation;RAG+%C2%B7+Agent+Memory+%C2%B7+LangGraph" alt="Typing SVG" />
  </a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/sameer-atram-5a04322b2"><img src="https://img.shields.io/badge/LinkedIn-Sameer%20Atram-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:sam14atram@gmail.com"><img src="https://img.shields.io/badge/Email-Contact%20me-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Open%20to-Remote%20%2F%20Relocation-2DD4BF?style=for-the-badge" alt="Open to remote or relocation" />
</p>

<p align="center">
  <b>MTech CSE, IIT Hyderabad</b> · Hyderabad, India · Agentic AI Developer @ <b>Amgo Games</b>
</p>

---

## 👨‍💻 About me

I build **production-oriented LLM systems**: multi-agent workflows with LangGraph, hybrid retrieval pipelines, structured outputs, guardrails, and evaluation.
Currently building an agentic platform that turns natural-language game ideas into playable Three.js applications.

- 🤖 **Agentic AI:** multi-agent orchestration, plan → execute → validate → repair loops, tool/function calling
- 🧪 **Agent reliability:** sandboxed execution, failure attribution, evidence-first validation
- 🔎 **RAG & memory:** hybrid BM25 + dense retrieval, RRF, temporal and authority-aware agent memory
- 🛡️ **Reliable LLM systems:** JSON-Schema structured outputs, guardrails, CI/CD-integrated validation agents
- 📈 **LLM Ops:** OpenTelemetry tracing, latency / token / cost tracking, LangSmith, MLflow

---

## 🚀 Featured Projects

### 🧪 AgentEval: Multi-Agent Reliability & Evaluation Platform

<p>
  <a href="https://github.com/sampro14/agentval_system"><img src="https://img.shields.io/badge/View%20Repo-181717?style=flat-square&logo=github&logoColor=white" alt="Repo" /></a>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white" alt="Playwright" />
</p>

> Most agent benchmarks report one success rate. AgentEval shows **where** a run went wrong, **why**, and whether it recovered.

```mermaid
flowchart LR
  P[Plan] --> R[Research] --> D[Draft] --> E[Execute in sandbox] --> V{Validate}
  V -- pass --> EV[Evaluate]
  V -- fail --> DG[Diagnose] --> RP[Repair] --> E
```

- **Seven specialized agents** (planner, researcher, coder, executor, validator, failure analyzer, repairer) with a bounded repair loop
- **Ground truth from execution:** code runs in a locked-down Docker sandbox with CPU, memory and time limits and no network
- **Failure attribution:** rule-based classifier with LLM fallback tags every failure with a category, the responsible agent, and a fix
- **Full observability:** every step stored with output, latency and tokens, inspectable in a live Next.js dashboard
- **Multi-provider:** Anthropic, OpenAI, Gemini, DeepSeek, plus an offline fake provider for tests; fault injection and CI

---

### 🧠 Enterprise Engineering Memory Agent: Memory That Knows What's True *Now*

<p>
  <a href="https://github.com/sampro14/enterprise_engineering_memory_agent"><img src="https://img.shields.io/badge/View%20Repo-181717?style=flat-square&logo=github&logoColor=white" alt="Repo" /></a>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini" />
  <img src="https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white" alt="SQLite" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white" alt="pytest" />
</p>

> A persistent memory layer for AI agents that tracks **what is true now, what was true before, and what to distrust**, and learns lessons from repeated failures.

```mermaid
flowchart LR
  I[Ingest text] --> X[LLM extraction] --> ER[Entity resolution] --> VA[Validation & conflict rules] --> C[Consolidation] --> S[(Bitemporal store)]
  Q[Question] --> HR[Hybrid retrieval] --> S
  S --> A[Answer with evidence]
```

| Benchmark (synthetic, held-out seeds) | Vector RAG | **Full memory** |
|---|---|---|
| Overall accuracy | 82% | **95%** |
| Current-fact questions | 58% | **100%** |
| Stale / poisoned answer rate (lower is better) | 43% | **14%** |

- **Bitemporal queries:** "what is true now", "what was true on date X", "when did it change"
- **Authority-aware:** production config outranks an agent's guess; poisoned claims never overwrite accepted facts and go to human review
- **Rigorous eval:** programmatic grading, no LLM judge, bootstrap confidence intervals, and limitations documented in the PoC report

---

### 🎮 Agentic Game Builder: From an Idea to a Playable Game

<p>
  <a href="https://github.com/sampro14/agentic-game-builder"><img src="https://img.shields.io/badge/View%20Repo-181717?style=flat-square&logo=github&logoColor=white" alt="Repo" /></a>
  <a href="https://drive.google.com/file/d/1CUDBPYp_mgWnRbgeW4WAUWuMQs6DjtGV/view?usp=drive_link"><img src="https://img.shields.io/badge/%E2%96%B6%20Watch%20Demo-FF0000?style=flat-square" alt="Demo" /></a>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
</p>

> Type a game idea in plain English and get a playable browser game (HTML + CSS + JS).

```mermaid
flowchart LR
  U[Game idea] --> CL[Clarify] --> PL[Plan] --> B[Build] --> V{Validate}
  V -- pass --> G[Playable game]
  V -- fail, max 2 --> RP[Repair] --> V
```

- **LangGraph state graph** with conditional routing for the clarification and repair loops
- **Clarifier** asks up to 3 targeted questions; **planner** outputs a structured JSON game plan
- **Validator** runs a 10-point static check plus an optional LLM semantic check; **repair agent** fixes only the broken parts
- **Live streaming UI:** FastAPI streams each phase over Server-Sent Events; CLI and Docker modes included

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=py,pytorch,sklearn,fastapi,docker,linux,git,githubactions,postgres,sqlite,nextjs,threejs&perline=12" alt="Tech stack icons" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangGraph" />
  <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white" alt="LangChain" />
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI" />
  <img src="https://img.shields.io/badge/Anthropic-191919?style=for-the-badge&logo=anthropic&logoColor=white" alt="Anthropic" />
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini" />
  <img src="https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge" alt="Qdrant" />
  <img src="https://img.shields.io/badge/Pinecone-000000?style=for-the-badge" alt="Pinecone" />
  <img src="https://img.shields.io/badge/FAISS-0467DF?style=for-the-badge" alt="FAISS" />
  <img src="https://img.shields.io/badge/OpenTelemetry-000000?style=for-the-badge&logo=opentelemetry&logoColor=white" alt="OpenTelemetry" />
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow" />
</p>

---

<p align="center">
  <i>Open to Applied AI / GenAI Engineer roles, remote or relocation. Let's build agents that actually work. 🤝</i>
</p>
