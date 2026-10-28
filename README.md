<h1 align="center">Param Madan</h1>

<p align="center">
  <b>AI Software Engineer · Robotics Perception</b> — 3D pose estimation · camera calibration & drift · uncertainty-aware manipulation
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

I build **robot perception that knows when not to trust itself**. A pick cell rarely fails loudly: the camera gets bumped half a degree, the pose estimator stays confident, and every grasp lands a few millimetres off. My work is the layer around perception that catches that: **calibration-drift monitoring**, **validated recalibration**, **calibrated pose uncertainty and risk gates against measured grasp tolerances**, and a safe fallback (defer to an operator) when a correction can't be verified. Every experiment is **pre-registered, paired and run on held-out seeds**, negative results included.

```text
🔭  Building   →  reliability layer for vision-guided industrial picking (UR10e + FANUC M-710iC/50, MuJoCo)
🧪  Measuring  →  drift detection, recalibration, pose-risk gating, Mask R-CNN in clutter, world models
🌱  Learning   →  real-image validation (BOP), MoveIt integration, edge deployment
```

---

## 🚀 Projects

### 🦾 [AURA-3D](https://github.com/parammadan/aura3d) · [paper](https://github.com/parammadan/aura3d/blob/main/paper/AURA3D_paper.pdf)
> **Uncertainty-aware perception and drift recovery for a simulated industrial pick cell**, on a UR10e and a **FANUC M-710iC/50** loaded from FANUC's official description. A 0.5° camera bump drops sorting success from 50/50 to 7/50; a fixture-residual **drift monitor** plus robust **SE(3) recalibration** (accepted only if it predicts a held-out reference sphere) recovers **42/50** (p = 6e-11) and cuts wrong picks **251 → 0**, with 0 false alarms in 1,000 frames. In touching-part clutter, a **fine-tuned Mask R-CNN** plus collision-aware grasp ordering sorts **88/100** trays (classical depth: 30). The same code runs on the FANUC arm with only a config change. A learned **pose-risk gate** with conformal bounds, a reproduced **Meta JEPA world model** (given no control authority, since it can't foresee grasp outcome), a **ROS 2** node graph and an ONNX/TensorRT latency study. Simulation only.
>
> `Python` · `MuJoCo` · `PyTorch` · `Mask R-CNN` · `SE(3) / hand-eye calibration` · `conformal prediction` · `ROS 2` · `ONNX Runtime / TensorRT` · `Slurm GPU training`

### 🎯 [BELIEF-3D](https://github.com/parammadan/belief-3d)
> **Multimodal 6D pose belief and calibration-aware active vision** (Franka Panda, MuJoCo). Neural pose proposals with geometric refinement raise success on < 50 %-visible objects from 0.853 to **0.985**. A pre-registered **multimodal SE(3) belief** beats a Kalman tracker on rotation (64.8 % → 87.0 %, p = 0.007). Online **extrinsic self-calibration** from known objects lifts task success 0.640 → **0.767** (p = 0.003), and a calibration-aware view objective beats entropy/covariance view selection (0.667 vs 0.533, Holm p = 0.008). Includes a pre-registered *negative* result: task-risk view selection that ignores calibration lost to random views.
>
> `Python` · `MuJoCo` · `6D pose estimation` · `particle / SE(3) belief` · `multi-camera tracking` · `active vision`

### 📷 [Robot Edge Stack](https://github.com/parammadan/robot_edge_stack-main)
> **Real hardware:** multi-node **ROS 2** perception on an **NVIDIA Jetson Orin Nano** with dual USB cameras. **YOLOv8 + TensorRT** at 24 ms per frame; a bandwidth manager fuses network health (RTT, loss) and `tegrastats` thermal/GPU metrics to throttle perception 15 → 10 → 5 FPS without restarts. Custom C++ message packages, FastDDS discovery server, watchdog, Docker Compose deployment and network-chaos test scripts.
>
> `C++17` · `ROS 2 Humble` · `TensorRT` · `YOLOv8` · `Jetson` · `Docker`

### 🛍️ [PennyPilot](https://github.com/parammadan/pennypilot) · [cre-copilot](https://github.com/parammadan/cre-copilot)
> Also: a multi-turn RL shopping agent (SFT → RLOO with a verifiable reward and a structural safety gate, pre-registered data-recipe loop), and multi-agent incident response on Azure with a deterministic confidence + permission gate and human-in-the-loop remediation.
>
> `PyTorch` · `LoRA` · `RL (RLOO · GRPO · PPO)` · `Azure OpenAI` · `React + TypeScript`

### 🔧 Open source — [OpenSearch Dashboards · search-relevance](https://github.com/opensearch-project/dashboards-search-relevance)
> Contributing to a **production OpenSearch plugin** used by search-relevance engineers: a **performance fix** replacing O(n²) result matching with id lookup maps ([#910](https://github.com/opensearch-project/dashboards-search-relevance/pull/910)) and **surfacing real experiment errors** instead of a generic failure message ([#911](https://github.com/opensearch-project/dashboards-search-relevance/pull/911)).
>
> `TypeScript` · `React` · `OpenSearch` · `Jest`

---

## 🛠️ Toolbox

**Robotics / Perception**
![ROS2](https://img.shields.io/badge/ROS%202-22314E?style=for-the-badge&logo=ros&logoColor=white)
![MuJoCo](https://img.shields.io/badge/MuJoCo-1F6FEB?style=for-the-badge&logoColor=white)
![Perception](https://img.shields.io/badge/3D%20Perception%20%2F%206D%20Pose-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Calibration](https://img.shields.io/badge/Camera%20%26%20Hand--Eye%20Calibration-444444?style=for-the-badge&logoColor=white)
![TensorRT](https://img.shields.io/badge/TensorRT%20%2F%20ONNX-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Jetson](https://img.shields.io/badge/NVIDIA%20Jetson-76B900?style=for-the-badge&logo=nvidia&logoColor=white)

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)

**AI / ML**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![RL](https://img.shields.io/badge/RL%20Post--training%20(GRPO%2FRLOO%2FPPO)-8B0000?style=for-the-badge&logo=pytorch&logoColor=white)
![LoRA](https://img.shields.io/badge/LoRA%20%2F%20PEFT-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![LLM Eval](https://img.shields.io/badge/LLM%20Evaluation-150458?style=for-the-badge&logo=weightsandbiases&logoColor=white)
![LLMs](https://img.shields.io/badge/LLMs%20%2F%20Agents-412991?style=for-the-badge&logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG%20%2F%20Vector%20Search-FF6F00?style=for-the-badge&logo=databricks&logoColor=white)
![MCP](https://img.shields.io/badge/MCP%20%2F%20Tool%20Calling-000000?style=for-the-badge&logo=anthropic&logoColor=white)

**Cloud / Infra**
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Azure OpenAI](https://img.shields.io/badge/Azure%20OpenAI-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Playwright](https://img.shields.io/badge/Playwright-2EAD33?style=for-the-badge&logo=playwright&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

---

## 📌 Focus right now

- **Perception you can trust in a workcell**: drift detection, validated recalibration, pose uncertainty calibrated against what the gripper can actually tolerate.
- **Learned perception under clutter and shift**: fine-tuning detectors and segmenters on synthetic data, and measuring where they still fail.
- **Honest evaluation**: pre-registered, paired experiments on held-out seeds, with the negative results published next to the positive ones.

---

<p align="center"><i>📫 Reach me at <a href="mailto:madan.pa@northeastern.edu">madan.pa@northeastern.edu</a></i></p>
