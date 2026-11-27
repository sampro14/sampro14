<h1 align="center">Sameer Atram</h1>

<p align="center">
  <b>Applied AI Engineer · I build LLM agents, and the evals that prove they work.</b>
</p>

<p align="center">
  MTech CSE, IIT Hyderabad · Agentic AI Developer at <b>Amgo Games</b> · Hyderabad, India (UTC+5:30, full UK and UAE working-day overlap)
</p>

<p align="center">
  <a href="https://sampro14.github.io/"><img src="https://img.shields.io/badge/Portfolio-sampro14.github.io-111827?style=for-the-badge" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/sameer-atram"><img src="https://img.shields.io/badge/LinkedIn-Sameer%20Atram-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:sam14atram@gmail.com"><img src="https://img.shields.io/badge/Email-sam14atram%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  <img src="https://img.shields.io/badge/Open%20to-Remote%20%2F%20Relocation-0F766E?style=for-the-badge" alt="Open to remote or relocation" />
</p>

---

At **Amgo Games** I architected and own a FastAPI + LangGraph platform where GDD, planning, asset, coding and vision agents turn a one-line idea into a playable Three.js game. Before that, at **Winfo Solutions**, I built a four-agent LangGraph suite for Oracle ERP UI testing.

In my own projects, an agent isn't done until something other than the model says it worked: an execution sandbox, a baseline, or a release gate. Each one also documents what didn't work.

## Pinned work

<table>
<tr>
<td width="50%" valign="top">

<a href="https://sampro14.github.io/enterprise_engineering_memory_agent/"><img src="https://raw.githubusercontent.com/sampro14/enterprise_engineering_memory_agent/main/docs/assets/demo.gif" alt="Memory agent ingesting documents, flagging a conflicting claim, and answering cleanly after human review" width="100%" /></a>

### [Memory Agent](https://github.com/sampro14/enterprise_engineering_memory_agent)

Memory for AI agents that knows what's true now, what was true before, and what to distrust.

**95%** accuracy vs **82%** for vector RAG, and **14%** stale or poisoned answers vs **43%**, on a held-out synthetic benchmark. [Honest caveats in the report](https://github.com/sampro14/enterprise_engineering_memory_agent/blob/main/docs/POC_REPORT.md).

[**▶ Live demo**](https://sampro14.github.io/enterprise_engineering_memory_agent/) · [Code](https://github.com/sampro14/enterprise_engineering_memory_agent)

<sub>LangGraph · FastAPI · Postgres + pgvector · async job queue</sub>

</td>
<td width="50%" valign="top">

<a href="https://github.com/sampro14/agentval_system"><img src="https://raw.githubusercontent.com/sampro14/agentval_system/main/docs/media/demo.gif" alt="AgentEval dashboard showing one run passing and another failing, being diagnosed, and repairing itself" width="100%" /></a>

### [AgentEval](https://github.com/sampro14/agentval_system)

Finds where an agent run went wrong, why, and whether it recovered. A locked-down Docker sandbox, not the model, decides whether the code works.

On held-out planted bugs it caught **15/15** runs with **0/9** false alarms, and blamed the right agent in **12/15**. [What that doesn't show](https://github.com/sampro14/agentval_system#results).

[**▶ Watch a run**](https://github.com/sampro14/agentval_system#agenteval) · [Code](https://github.com/sampro14/agentval_system)

<sub>LangGraph · FastAPI · Next.js · Postgres · Redis · Docker</sub>

</td>
</tr>
<tr>
<td width="50%" valign="top">

<a href="https://sampro14.github.io/procedure-agent/"><img src="https://raw.githubusercontent.com/sampro14/procedure-agent/main/docs/assets/demo.gif" alt="Procedure agent chat countering a $40 request at the $100 minimum, with highlighted disclosures and a decision trace beside each reply" width="100%" /></a>

### [Procedure Agent](https://github.com/sampro14/procedure-agent)

A chat agent for regulated conversations: legal wording is never paraphrased, limits can't be broken, and nothing ships until the replay evals pass.

**9 replayed calls**, **3 deterministic metrics**, and **8 planted regressions** the release gate must catch.

[**▶ Live demo**](https://sampro14.github.io/procedure-agent/) (runs in your browser) · [Code](https://github.com/sampro14/procedure-agent)

<sub>Python · DeepEval · pytest · Pyodide</sub>

</td>
<td width="50%" valign="top">

<a href="https://github.com/sampro14/invoiceiq"><img src="https://raw.githubusercontent.com/sampro14/invoiceiq/main/docs/assets/review.png" alt="InvoiceIQ pausing a wrong-total invoice for human review, with the graph path, the reason and the extracted fields" width="100%" /></a>

### [InvoiceIQ](https://github.com/sampro14/invoiceiq)

Invoice PDFs, scans and photos to validated, ERP-ready JSON, approved only when two model families and eight code-level checks agree.

Checks include **UAE TRN** and **India GSTIN** formats; doubtful documents pause for human review. Held-out results on 300 documents are in progress.

[**▶ Try it without an API key**](https://github.com/sampro14/invoiceiq#try-it-in-30-seconds-no-api-key) · [Code](https://github.com/sampro14/invoiceiq)

<sub>LangGraph · FastAPI · Gemini · Groq · Langfuse</sub>

</td>
</tr>
</table>

## Also built

- **[Agentic Game Builder](https://github.com/sampro14/agentic-game-builder):** describe a game in plain English, and agents clarify, plan, build, validate and repair it into a playable browser game. [2-minute video](https://drive.google.com/file/d/1CUDBPYp_mgWnRbgeW4WAUWuMQs6DjtGV/view?usp=drive_link).
- **[Text-to-image diffusion](https://github.com/sampro14/Text-to-Animated-video):** a latent diffusion pipeline built from parts: a VAE with an adversarial loss, a CLIP-style text encoder and a conditional UNet.

## Tools

**Agents and LLMs:** LangGraph, LangChain, OpenAI, Anthropic, Gemini, DeepSeek<br/>
**Retrieval and memory:** pgvector, Qdrant, Pinecone, FAISS, hybrid BM25 + dense retrieval with RRF<br/>
**Evaluation and LLMOps:** DeepEval, Langfuse, LangSmith, MLflow, OpenTelemetry, pytest, Playwright<br/>
**Backend and infrastructure:** Python, FastAPI, PostgreSQL, Redis, SQLite, SQLAlchemy, Alembic, Docker, GitHub Actions, Linux<br/>
**Machine learning:** PyTorch, TensorFlow, Keras, scikit-learn, Diffusers, Transformers, OpenCV<br/>
**Also:** C++, JavaScript, SQL, Next.js, Three.js, Streamlit

---

<p align="center">
  Open to <b>Applied AI</b>, <b>Forward Deployed</b> and <b>GenAI Engineer</b> roles: remote or relocation, full-time or contract.<br/>
  <a href="mailto:sam14atram@gmail.com">Email me</a> · <a href="https://www.linkedin.com/in/sameer-atram">LinkedIn</a> · <a href="https://sampro14.github.io/">Portfolio</a>
</p>
