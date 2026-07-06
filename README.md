<h1 align="center">Param Madan</h1>

<p align="center">
  <b>AI Software Engineer</b> — agentic systems · LLM inference tooling · Perception
</p>

<p align="center">
  <img src="https://img.shields.io/badge/ex--MIT-A31F34?style=for-the-badge&logoColor=white" alt="ex-MIT">
</p>

<p align="center">
  <a href="mailto:madan.pa@northeastern.edu"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://www.linkedin.com/in/parammadan/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

## 👋 About me

I build **AI systems that reason and act** — multi-agent pipelines, LLM inference profiling, and chain-of-thought reasoning agents. I care about making agentic systems that are **reliable and inspectable**, not just demos: deterministic gates, human-in-the-loop checkpoints, and measurable inference performance.

```text
🔭  Building   →  a multi-agent incident-response copilot on Azure
🌱  Learning   →  on-device / Windows AI inference, LLM eval & reliability
🧩  Interests  →  agent orchestration, structured reasoning, inference perf
🎯  Open to    →  Software Engineer (AI) roles
```

---

## 💼 Experience

### 🎓 Massachusetts Institute of Technology — MIT Spinout & Lincoln Laboratory
**AI Software Engineer (Co-op)** · Boston, MA · Jul 2024 – Dec 2024
> Real-time **3D spatial perception & low-latency telemetry transport** for an autonomous **surgical-robotics** platform — safety-critical, deterministic, sub-millimeter tracking.
> - **C++ / ROS middleware** — zero-copy **lock-free shared-memory ring buffer** + **Eigen** optical→kinematic coordinate transforms; cut sensor-fusion latency **~80 ms → negligible**.
> - **Edge AI** — optimized a **PyTorch U-Net** semantic-segmentation model (organs / vessels vs. tools) for a **60 FPS** control loop with **OpenCV** preprocessing → **+15%** real-time tracking reliability.
> - **GPU profiling** — diagnosed frame drops with **NVIDIA Nsight Systems**; **pinned memory + async CUDA streams** overlapped Host↔Device transfer with compute, eliminating the PCIe bottleneck for deterministic multi-GPU throughput.
> - **Engineering rigor** — CMake · GoogleTest · Docker · SonarQube · Git, with hardware-in-the-loop testing each sprint; edge-case rosbags → AWS (S3 / Batch / EC2) for distributed retraining.
>
> `C++17` · `ROS` · `CUDA` · `Eigen` · `PyTorch` · `OpenCV` · `Nsight Systems` · `Docker` · `CMake` · `AWS`

---

## 🚀 Projects

### 🛰️ [cre-copilot](https://github.com/parammadan/cre-copilot)
> **Multi-agent incident-response copilot** on Azure. Hosted Azure OpenAI agents triage live telemetry **read-only** over Azure Data Explorer; a **deterministic confidence + permission gate** decides act vs. escalate, with an enterprise **AI-safety layer** (blast-radius guard, prompt-injection detection, approval integrity, audit trail) and **human-in-the-loop** remediation confirmed by an independent Verifier.
>
> `Python` · `Azure OpenAI` · `Azure Data Explorer (KQL)` · `Azure Container Apps` · `Managed Identity` · `FastAPI` · `Playwright`

### 🤖 [robot_edge_stack](https://github.com/parammadan/robot_edge_stack-main)
> **Adaptive bandwidth management for edge perception.** Multi-node **ROS 2** system on **NVIDIA Jetson Orin Nano**: real-time **YOLOv8 + TensorRT** object detection with closed-loop, network-aware **FPS throttling** (NORMAL → DEGRADED → CRITICAL) that cuts bandwidth up to **67%** as the link degrades — with chaos-engineering tests for latency/loss/jitter.
>
> `ROS 2 Humble` · `C++17` · `Python 3.10` · `TensorRT` · `YOLOv8` · `FastDDS` · `Docker`

### ⚡ [winai-inference-profiler](https://github.com/parammadan/winai-inference-profiler)
> Profiles **LLM inference performance** for Windows AI workloads — latency, throughput, and resource characteristics for on-device model serving.
>
> `Python`

### 🧠 [Chain-of-Thought-Reasoning-Agent](https://github.com/parammadan/Chain-of-Thought-Reasoning-Agent)
> A step-by-step **reasoning agent** exploring structured chain-of-thought prompting for more transparent, verifiable model outputs.
>
> `Python`

---

## 🛠️ Toolbox

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![SQL](https://img.shields.io/badge/SQL%20%2F%20KQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

**AI / ML**
![LLMs](https://img.shields.io/badge/LLMs%20%2F%20Agents-412991?style=for-the-badge&logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%20%2F%20Function%20Calling-000000?style=for-the-badge&logo=anthropic&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20%2F%20Vector%20Search-FF6F00?style=for-the-badge&logo=databricks&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![LLM Eval](https://img.shields.io/badge/LLM%20Evaluation-150458?style=for-the-badge&logo=weightsandbiases&logoColor=white)

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
![Entra ID](https://img.shields.io/badge/Azure%20Entra%20ID-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Dataverse](https://img.shields.io/badge/Dataverse-742774?style=for-the-badge&logo=microsoft&logoColor=white)

---

## 📌 Focus right now

- **Reliable agents** — deterministic confidence + permission gates, blast-radius guards, and human-in-the-loop control so agentic systems fail safely.
- **AI safety & security** — prompt-injection defense, least-privilege identity, approval integrity, and auditable, inspectable agent behavior.
- **Windows / edge AI inference** — profiling and optimizing LLM serving for on-device workloads.

---

<p align="center"><i>📫 Reach me at <a href="mailto:madan.pa@northeastern.edu">madan.pa@northeastern.edu</a></i></p>
