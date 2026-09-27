# Hi, I'm Sameer Atram 👋

**Applied AI Engineer** · Agentic AI · Multi-Agent Systems · Enterprise RAG
MTech CSE, IIT Hyderabad · Based in Hyderabad, India · Open to remote / relocation

I build production-oriented LLM systems: multi-agent workflows with LangGraph, hybrid retrieval pipelines, structured outputs, guardrails, and evaluation. Currently building an agentic platform at **Amgo Games** that turns natural-language game ideas into playable Three.js applications.

---

### 🔧 What I work on

- **Agentic AI:** multi-agent orchestration, plan → execute → validate → repair loops, tool/function calling
- **Agent reliability & evaluation:** sandboxed execution, failure attribution, evidence-first validation
- **RAG & memory:** hybrid BM25 + dense retrieval, Reciprocal Rank Fusion, temporal and authority-aware agent memory
- **Reliable LLM systems:** JSON-Schema structured outputs, guardrails, CI/CD-integrated validation agents
- **LLM Ops:** OpenTelemetry tracing, latency / token / cost tracking, LangSmith, MLflow

---

### 🚀 Featured Projects

#### 🧪 [AgentEval](https://github.com/sampro14/agentval_system): Multi-agent reliability & evaluation platform

Most agent benchmarks report one success rate. AgentEval shows **where** a run went wrong, **why**, and whether it recovered.

- Planner, researcher, coder, executor, validator, failure-analyzer and repairer agents wired with LangGraph, including a bounded repair loop
- Generated code runs in a **locked-down Docker sandbox** (CPU, memory, time limits, no network), so pass/fail comes from execution, not the agent's own claim
- **Failure attribution:** rule-based classifier with an LLM fallback tags every failure with a category, the responsible agent, and a recommended action
- Every step stored as a structured event (output, latency, tokens); live Next.js dashboard to inspect each agent's prompt and reply
- Pluggable LLM providers (Anthropic, OpenAI, Gemini, DeepSeek, offline fake provider for tests), fault injection, CI

`LangGraph` `FastAPI` `Docker` `Next.js` `Playwright` `Python 3.12`

---

#### 🧠 [Enterprise Engineering Memory Agent](https://github.com/sampro14/enterprise_engineering_memory_agent): Memory that knows what's true *now*

A persistent memory layer for AI agents that tracks **what is true now, what was true before, and what to distrust**, and learns lessons from repeated failures.

- **Bitemporal storage:** answers "what is true now", "what was true on date X", and "when did it change"
- **Authority-aware conflict handling:** a production config outranks an agent's guess; low-authority or poisoned claims never overwrite accepted facts and go to a human review queue
- LLM extraction → entity resolution → validation → consolidation write path; hybrid retrieval; LangGraph query and task flows
- **Evaluation** on a synthetic benchmark (held-out seeds, programmatic grading, no LLM judge): **95% overall vs 82% for vector RAG** (+12.9 pts, 95% CI [+8.2, +18.4]), with full results and limitations documented in the PoC report

`LangGraph` `Gemini` `Hybrid retrieval` `SQLite` `NumPy` `pytest`

---

#### 🎮 [Agentic Game Builder](https://github.com/sampro14/agentic-game-builder): From an idea to a playable game

Type a game idea in plain English and get a playable browser game (HTML + CSS + JS).

- **Clarify → Plan → Build → Validate → Repair** pipeline as a LangGraph state graph with conditional routing
- Clarifier asks up to 3 targeted questions; planner produces a structured JSON game plan
- Validator runs a 10-point static check plus an optional LLM semantic check; repair agent fixes only the broken parts (max 2 iterations)
- FastAPI backend streams each phase live to a web UI over Server-Sent Events; CLI mode and Docker supported
- [▶ Watch the demo](https://drive.google.com/file/d/1CUDBPYp_mgWnRbgeW4WAUWuMQs6DjtGV/view?usp=drive_link)

`LangGraph` `LangChain` `OpenAI` `FastAPI` `SSE` `Docker`

---

### 🛠️ Tech Stack

**GenAI & Agents:** LangGraph · LangChain · RAG · Prompt Engineering · Structured Outputs · LLM Evaluation
**Retrieval & Data:** Qdrant · Pinecone · Weaviate · FAISS · BM25 · PostgreSQL · SQLite
**ML / DL:** Python · PyTorch · Scikit-learn · XGBoost · SHAP
**Backend & Frontend:** FastAPI · Docker · Linux · Git · CI/CD · Next.js · Three.js
**Observability:** OpenTelemetry · LangSmith · MLflow

---

### 📫 Reach me

[LinkedIn](https://www.linkedin.com/in/sameer-atram-5a04322b2) · [Email](mailto:sam14atram@gmail.com)
