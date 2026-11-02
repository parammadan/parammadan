<h1 align="center">Param Madan</h1>

<p align="center">
  <b>Software Engineer · Robotics · GPU / CUDA · AI</b> — robot perception on real hardware · GPU inference & LLM serving · reliable AI systems
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

I'm a software engineer who builds **AI systems that run on real machines**: robot perception on an NVIDIA Jetson, GPU inference with TensorRT and vLLM, and the reliability layer that keeps them honest when hardware, data or models misbehave. I like problems where the failure is quiet (a camera bumped half a degree, one bad row that crash-loops a GPU engine) and the fix has to be measured, not assumed.

```text
🔭  Building   →  robot perception + manipulation in sim and on edge hardware (ROS 2, Jetson, MuJoCo)
⚡  GPU work   →  TensorRT / ONNX inference, vLLM batch serving, CUDA-fault resilience, Slurm GPU training
🌱  Learning   →  CUDA kernels & profiling (Nsight), C++ performance, real-robot deployment
```

---

## 🚀 Projects

### 🦾 [AURA-3D](https://github.com/parammadan/aura3d) · [paper (DOI)](https://doi.org/10.5281/zenodo.23734027)
> **Uncertainty-aware perception and drift recovery for a simulated industrial pick cell**, on a UR10e and a **FANUC M-710iC/50** loaded from FANUC's official description. A 0.5° camera bump drops sorting success from 50/50 to 7/50; a fixture-residual **drift monitor** plus robust **SE(3) recalibration** (accepted only if it predicts a held-out reference sphere) recovers **42/50** (p = 6e-11) and cuts wrong picks **251 → 0**, with 0 false alarms in 1,000 frames. In touching-part clutter, a **fine-tuned Mask R-CNN** plus collision-aware grasp ordering sorts **88/100** trays (classical depth: 30). The same code runs on the FANUC arm with only a config change. A learned **pose-risk gate** with conformal bounds, a reproduced **Meta JEPA world model** (given no control authority, since it can't foresee grasp outcome), a **ROS 2** node graph and an ONNX/TensorRT latency study. Simulation only.
>
> `Python` · `MuJoCo` · `PyTorch` · `Mask R-CNN` · `SE(3) / hand-eye calibration` · `conformal prediction` · `ROS 2` · `ONNX Runtime / TensorRT` · `Slurm GPU training`

### 🎯 [BELIEF-3D](https://github.com/parammadan/belief-3d)
> **Multimodal 6D pose belief and calibration-aware active vision** (Franka Panda, MuJoCo). In the pre-registered final study (299 paired episodes), the full system lifts physical grasp success from **0.488 (Kalman baseline) to 0.773** (Holm p = 3e-14). Neural pose proposals with geometric refinement raise success on < 50 %-visible objects from 0.853 to **0.985**. A pre-registered **multimodal SE(3) belief** beats a Kalman tracker on rotation (64.8 % → 87.0 %, p = 0.007). Online **extrinsic self-calibration** from known objects lifts task success 0.640 → **0.767** (p = 0.003), and a calibration-aware view objective beats entropy/covariance view selection (0.667 vs 0.533, Holm p = 0.008). Includes a pre-registered *negative* result: task-risk view selection that ignores calibration lost to random views.
>
> `Python` · `MuJoCo` · `6D pose estimation` · `particle / SE(3) belief` · `multi-camera tracking` · `active vision`

### 📷 [Robot Edge Stack](https://github.com/parammadan/robot_edge_stack-main)
> **Real hardware:** multi-node **ROS 2** perception on an **NVIDIA Jetson Orin Nano** with dual USB cameras. **YOLOv8 + TensorRT** at 24 ms per frame; a bandwidth manager fuses network health (RTT, loss) and `tegrastats` thermal/GPU metrics to throttle perception 15 → 10 → 5 FPS without restarts. Custom C++ message packages, FastDDS discovery server, watchdog, Docker Compose deployment and network-chaos test scripts.
>
> `C++17` · `ROS 2 Humble` · `TensorRT` · `YOLOv8` · `Jetson` · `Docker`

### ⚡ [ChaosBatch](https://github.com/parammadan/chaosbatch) · [results](https://parammadan.github.io/chaosbatch/)
> **One bad row can hang a Ray batch-LLM job forever.** When a vLLM engine dies on a CUDA fault, Ray 2.59 restarts the actor and retries the same batch, so a row that kills the engine every time loops with no exit. Reproduced across the configurations Ray users are told to try (**hung in 6/6 runs**), confirmed on an **A100**, and fixed with a guard built from Ray primitives: **6/6 complete**, exactly 1 error row, and a bad GPU is fenced after 2 deaths instead of crash-looping 7–9×.
>
> `Python` · `Ray Data` · `vLLM` · `CUDA fault handling` · `A100` · `distributed systems`

### 🛍️ [PennyPilot](https://github.com/parammadan/pennypilot) · [cre-copilot](https://github.com/parammadan/cre-copilot)
> Also: a multi-turn RL shopping agent (SFT → RLOO with a verifiable reward and a structural safety gate, pre-registered data-recipe loop), and multi-agent incident response on Azure with a deterministic confidence + permission gate and human-in-the-loop remediation.
>
> `PyTorch` · `LoRA` · `RL (RLOO · GRPO · PPO)` · `Azure OpenAI` · `React + TypeScript`

### 🔧 Open source — [OpenSearch](https://github.com/opensearch-project/dashboards-search-relevance) · [NVIDIA Triton client](https://github.com/triton-inference-server/client)
> **OpenSearch search-relevance:** a merged **performance fix** replacing O(n²) result matching with id lookup maps ([#910](https://github.com/opensearch-project/dashboards-search-relevance/pull/910)) and surfacing real experiment errors instead of a generic failure ([#911](https://github.com/opensearch-project/dashboards-search-relevance/pull/911)). **Triton Inference Server client:** reuse a prebuilt gRPC inference request across retries ([#936](https://github.com/triton-inference-server/client/pull/936), open).
>
> `TypeScript` · `React` · `C++` · `gRPC` · `Triton Inference Server`

---

## 🛠️ Toolbox

**Robotics**
![ROS2](https://img.shields.io/badge/ROS%202-22314E?style=for-the-badge&logo=ros&logoColor=white)
![MuJoCo](https://img.shields.io/badge/MuJoCo-1F6FEB?style=for-the-badge&logoColor=white)
![Perception](https://img.shields.io/badge/3D%20Perception%20%2F%206D%20Pose-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Calibration](https://img.shields.io/badge/Camera%20%26%20Hand--Eye%20Calibration-444444?style=for-the-badge&logoColor=white)

**GPU / CUDA**
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![TensorRT](https://img.shields.io/badge/TensorRT%20%2F%20ONNX-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Jetson](https://img.shields.io/badge/NVIDIA%20Jetson-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![vLLM](https://img.shields.io/badge/vLLM-30A2FF?style=for-the-badge&logoColor=white)
![Triton](https://img.shields.io/badge/Triton%20Inference%20Server-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Ray](https://img.shields.io/badge/Ray-028CF0?style=for-the-badge&logo=ray&logoColor=white)

**Languages**
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
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

- **Robotics that holds up off the happy path**: perception that detects its own drift, recalibrates, and defers when it can't verify a correction.
- **GPU systems**: fast, observable inference on edge and datacenter GPUs (TensorRT, vLLM, Triton), and jobs that survive CUDA faults instead of crash-looping.
- **Honest engineering**: every claim measured, paired experiments on held-out seeds, negative results published next to the positive ones.

---

<p align="center"><i>📫 Reach me at <a href="mailto:madan.pa@northeastern.edu">madan.pa@northeastern.edu</a></i></p>
