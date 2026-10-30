<h1 align="center">Param Madan</h1>

<p align="center">
  <b>AI Software Engineer · Statistical Programming in R</b> — clinical trial tables · SAS → R migration · AI with independent validation
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ex--MIT-A31F34?style=for-the-badge&logoColor=white" alt="ex-MIT">
  <img src="https://img.shields.io/badge/OpenSearch%20Contributor-005EB8?style=for-the-badge&logo=opensearch&logoColor=white" alt="OpenSearch Contributor">
</p>

<p align="center">
  <a href="mailto:madan.pa@northeastern.edu"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</p>

---

## 👋 About me

I build **AI tools for statistical programming that never get the last word**. In a trial analysis the risky failure is quiet: a translated SAS program that rounds a half differently, or a table whose denominator came from the wrong dataset. My work puts AI on the routine drafting (SAP → table shells and R programs, SAS → R translation, answering "where does this number come from?") and puts **an independent check behind every output**: rebuilt numbers compared to the published CSR, side-by-side SAS vs R diffs, and sign-off by a programmer and a statistician. The copilot drafts and routes; **people approve**.

```text
🔭  Building   →  Forward 2028: an R workspace from SAP and amendments to validated tables and SAS → R migration
🧪  Measuring  →  table rebuilds vs the CSR, SAS → R equivalence, copilot answers vs an answer key
🌱  Learning   →  CDISC ADaM / SDTM depth, pharmaverse (admiral, rtables), regulatory-grade R validation
```

---

## 🚀 Projects

### 📊 Forward 2028 · *private repo, demo on request*
> **An end-to-end R workspace for clinical trial statistical programming**, built on public CDISC Pilot Study data. A request moves Requested → AI drafting → checks → programmer review → statistician review → approved, with an audit log. **SAP → tables:** the copilot drafts table shells and R programs from the SAP, and every printed number is checked against the CSR: **451 of 474 equal** across 5 tables, with each of the 23 differences explained (22 from recoded data, 1 where the CSR didn't follow its SAP). **SAS → R studio:** scan for risky constructs, translate, run, diff, sign off, over a 12-program benchmark that also surfaced bugs on the SAS side. **Trace a number** from a table cell back to ADaM, SDTM and the CRF; **amendment impact** finds 18 of 19 recorded SAP changes; ten rule-based **data checks** on SDTM AE vs DM; a director dashboard in **Shiny**. Runs deterministically by default (recorded, validated runs); live AI is server-side with a spend cap.
>
> `R` · `tidyverse` · `Shiny` · `plumber` · `testthat` · `Quarto` · `CDISC SDTM / ADaM` · `SAS → R` · `React + TypeScript` · `GitHub Actions`

### 🧪 Rigorous evaluation — [AURA-3D](https://github.com/parammadan/aura3d) ([paper](https://doi.org/10.5281/zenodo.23734027)) · [BELIEF-3D](https://github.com/parammadan/belief-3d)
> The same discipline in another domain: **pre-registered, paired experiments** on held-out seeds, **Holm-corrected** tests, **conformal** bounds and published negative results. Example: a fixture-based drift monitor recovers pick success from 7/50 to **42/50** (p = 6e-11) with 0 false alarms in 1,000 frames; a pre-registered study of 299 paired episodes lifts success 0.488 → **0.773** (Holm p = 3e-14).
>
> `Python` · `experimental design` · `paired tests / multiplicity` · `conformal prediction` · `PyTorch`

### 🛍️ Also — [PennyPilot](https://github.com/parammadan/pennypilot) · [cre-copilot](https://github.com/parammadan/cre-copilot)
> Also: a multi-turn RL shopping agent (SFT → RLOO with a verifiable reward and a structural safety gate, pre-registered data-recipe loop), and multi-agent incident response on Azure with a deterministic confidence + permission gate and human-in-the-loop remediation.
>
> `PyTorch` · `LoRA` · `RL (RLOO · GRPO · PPO)` · `Azure OpenAI` · `React + TypeScript`

### 🔧 Open source — [OpenSearch Dashboards · search-relevance](https://github.com/opensearch-project/dashboards-search-relevance)
> Contributing to a **production OpenSearch plugin** used by search-relevance engineers: a **performance fix** replacing O(n²) result matching with id lookup maps ([#910](https://github.com/opensearch-project/dashboards-search-relevance/pull/910)) and **surfacing real experiment errors** instead of a generic failure message ([#911](https://github.com/opensearch-project/dashboards-search-relevance/pull/911)).
>
> `TypeScript` · `React` · `OpenSearch` · `Jest`

---

## 🛠️ Toolbox

**Statistical programming**
![R](https://img.shields.io/badge/R-276DC3?style=for-the-badge&logo=r&logoColor=white)
![tidyverse](https://img.shields.io/badge/tidyverse-1A162D?style=for-the-badge&logo=tidyverse&logoColor=white)
![Shiny](https://img.shields.io/badge/Shiny-276DC3?style=for-the-badge&logo=rstudioide&logoColor=white)
![Quarto](https://img.shields.io/badge/Quarto-39729E?style=for-the-badge&logo=quarto&logoColor=white)
![testthat](https://img.shields.io/badge/testthat-276DC3?style=for-the-badge&logo=r&logoColor=white)
![SAS to R](https://img.shields.io/badge/SAS%20%E2%86%92%20R%20Migration-0766D1?style=for-the-badge&logoColor=white)
![CDISC](https://img.shields.io/badge/CDISC%20SDTM%20%2F%20ADaM-444444?style=for-the-badge&logoColor=white)

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)

**AI / ML**
![LLMs](https://img.shields.io/badge/LLMs%20%2F%20Agents-412991?style=for-the-badge&logo=openai&logoColor=white)
![LLM Eval](https://img.shields.io/badge/LLM%20Evaluation-150458?style=for-the-badge&logo=weightsandbiases&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20%2F%20Retrieval-FF6F00?style=for-the-badge&logo=databricks&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![vLLM](https://img.shields.io/badge/Open%20models%20on%20HPC%20(vLLM%2FSlurm)-30A14E?style=for-the-badge&logoColor=white)

**Engineering**
![Git](https://img.shields.io/badge/Git%20%2F%20GitHub-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)

---

## 📌 Focus right now

- **AI that drafts, people who approve**: copilots for SAPs, tables and code questions that cite their sources and hand off what they can't settle.
- **SAS → R you can trust**: translation plus side-by-side output diffs, so differences like rounding rules are found before sign-off.
- **Validation first**: every number traced to its source and checked against an independent reference or the published record.

---

<p align="center"><i>📫 Reach me at <a href="mailto:madan.pa@northeastern.edu">madan.pa@northeastern.edu</a></i></p>
