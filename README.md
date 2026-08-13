<h1 align="center">Param Madan</h1>

<p align="center">
  <b>AI Software Engineer</b> — LLM post-training & eval · generative AI data platforms · agent orchestration
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ex--MIT-A31F34?style=for-the-badge&logoColor=white" alt="ex-MIT">
  <img src="https://img.shields.io/badge/OpenSearch%20Contributor-005EB8?style=for-the-badge&logo=opensearch&logoColor=white" alt="OpenSearch Contributor">
</p>

<p align="center">
  <a href="mailto:madan.pa@northeastern.edu"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.linkedin.com/in/parammadan/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

## 👋 About me

I build **foundational AI systems for shopping-style agents** — from RL post-training on a real LLM to the data platform that measures whether it's actually working. I care about the parts that make model changes trustworthy, not just demos: **verifiable rewards** instead of a hackable reward model, **pre-registered experiments with honest negative results**, **behavioral telemetry** (event streaming, funnels, friction metrics) that catches regressions offline evals miss, and **deterministic safety gates** on autonomous actions.

```text
🔭  Building   →  RL post-training + behavioral-data platform for a generative shopping agent
🧪  Measuring  →  GRPO/RLOO/PPO experiments, offline eval vs. live behavioral replay, honest negative results
🌱  Learning   →  ML platform engineering at scale — streaming ingestion, self-service extraction/training
🎯  Open to    →  Software Dev Engineer (AI) roles
```

---

## 🚀 Projects

### 🛍️ [PennyPilot + PennyData](https://github.com/parammadan/pennypilot)
> A **multi-turn, multilingual RL shopping agent** and the **behavioral-data platform** built to prove it actually improved. SFT (LoRA) → **RLOO post-training** with a **verifiable reward** against a ground-truth catalog (no reward model to hack) and a **structural safety gate** — cart actions without a prior permission grant are impossible to reward, 0 violations across every eval. Real bugs found by dogfooding the agent were fixed through a **pre-registered, guardrail-gated data-recipe loop** — including an actual rollback (v1 broke the model) and an actual "not shipped" call (v2 hit its target metric but breached a guardrail) — before the accepted recipe (v3) shipped a model that topped *both* the offline eval **and** live behavioral replay, resolving a case where the two had been ranking models **oppositely**.
>
> Behind the agent: **Kafka → S3/DuckDB** streaming + batch ingestion, a behavioral-intelligence layer (funnels, friction metrics, deterministic failure attribution with evidence citations), and a self-service ML layer (login, extraction requests, real Slurm training-job submission) with **PII scrubbing** and **admin-gated SQL** — the ML platform half of the JD, not just the model half.
>
> `Python` · `PyTorch` · `LoRA / PEFT` · `RL (RLOO · GRPO · PPO)` · `Kafka` · `S3 · DuckDB` · `React + TypeScript`

### 🛰️ [cre-copilot](https://github.com/parammadan/cre-copilot)
> **Multi-agent AI orchestration** for live-site incident response on Azure. Hosted Azure OpenAI agents triage real telemetry via **tool calling** over Azure Data Explorer — in a fixed pipeline or a fully **autonomous mode** where an orchestrator agent picks its own read-only tools. A **deterministic confidence + permission gate** decides act-vs-escalate behind an enterprise **AI-safety layer** (blast-radius guard, prompt-injection detection, approval integrity, audit trail); remediation is **human-in-the-loop** (Teams Adaptive Cards + approval) and confirmed by an independent Verifier agent. Plus a **conversational** "Ask CRE Copilot" mode, an eval harness for correlation quality, and structured tracing — deployed on **Azure Container Apps** with a React console.
>
> `Python` · `Azure OpenAI` · `Azure Data Explorer (KQL)` · `React + TypeScript` · `Azure Container Apps` · `Managed Identity` · `FastAPI` · `Teams`

### 🔧 Open source — [OpenSearch Dashboards · search-relevance](https://github.com/opensearch-project/dashboards-search-relevance)
> Contributing to a **production OpenSearch plugin** used by search-relevance engineers: a **performance fix** replacing O(n²) result matching with id lookup maps ([#910](https://github.com/opensearch-project/dashboards-search-relevance/pull/910)) and **surfacing real experiment errors** instead of a generic failure message ([#911](https://github.com/opensearch-project/dashboards-search-relevance/pull/911)).
>
> `TypeScript` · `React` · `OpenSearch` · `Jest`

---

## 🛠️ Toolbox

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![SQL](https://img.shields.io/badge/SQL%20%2F%20KQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

**AI / ML**
![LLMs](https://img.shields.io/badge/LLMs%20%2F%20Agents-412991?style=for-the-badge&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%20%2F%20Tool%20Calling-000000?style=for-the-badge&logo=anthropic&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20%2F%20Vector%20Search-FF6F00?style=for-the-badge&logo=databricks&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![RL](https://img.shields.io/badge/RL%20Post--training%20(GRPO%2FRLOO%2FPPO)-8B0000?style=for-the-badge&logo=pytorch&logoColor=white)
![LLM Eval](https://img.shields.io/badge/LLM%20Evaluation-150458?style=for-the-badge&logo=weightsandbiases&logoColor=white)

**Frontend**
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)

**Robotics / Perception**
![ROS2](https://img.shields.io/badge/ROS2-22314E?style=for-the-badge&logo=ros&logoColor=white)
![Perception](https://img.shields.io/badge/Perception%20%2F%20Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)

**Cloud / Infra**
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![ADX](https://img.shields.io/badge/Azure%20Data%20Explorer%20(Kusto)-0062AD?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Container Apps](https://img.shields.io/badge/Azure%20Container%20Apps-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**Microsoft 365 / Power Platform**
![Copilot Studio](https://img.shields.io/badge/Copilot%20Studio-8661C5?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Automate](https://img.shields.io/badge/Power%20Automate-0066FF?style=for-the-badge&logo=powerautomate&logoColor=white)
![Microsoft Graph](https://img.shields.io/badge/Microsoft%20Graph-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Teams](https://img.shields.io/badge/Teams%20%2F%20Adaptive%20Cards-6264A7?style=for-the-badge&logo=microsoftteams&logoColor=white)
![Entra ID](https://img.shields.io/badge/Azure%20Entra%20ID-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Dataverse](https://img.shields.io/badge/Dataverse-742774?style=for-the-badge&logo=microsoft&logoColor=white)

---

## 📌 Focus right now

- **RL post-training for LLMs** — GRPO/RLOO/PPO behind one interface, verifiable rewards, pre-registered experiments with honest negative results, forgetting-mitigation via rehearsal.
- **ML data platforms** — streaming + batch ingestion (Kafka/S3/DuckDB), behavioral telemetry that catches what offline eval misses, self-service extraction/training with governance (PII scrubbing, admin-gated SQL).
- **Agent orchestration & safety** — deterministic gates on autonomous actions, human-in-the-loop approval, structured tracing, measured performance work (O(n²) → O(n) fixes in production OSS).

---

<p align="center"><i>📫 Reach me at <a href="mailto:madan.pa@northeastern.edu">madan.pa@northeastern.edu</a></i></p>
