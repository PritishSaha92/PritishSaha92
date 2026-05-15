<!-- Profile README refreshed from Resume___Personal/main.tex on 2026-05-15. -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B1020,45:134E5E,100:71B280&text=Pritish%20Saha&fontColor=F8FAFC&fontSize=56&fontAlignY=38&desc=AI%20Research%20%7C%20Efficient%20LLMs%20%7C%20Agent%20Learning%20%7C%20Systems&descAlignY=58&descSize=18" alt="Pritish Saha - AI Research, Efficient LLMs, Agent Learning, Systems" />
</p>

<p align="center">
  <a href="mailto:pritish171@gmail.com"><img src="https://img.shields.io/badge/Email-pritish171%40gmail.com-0B1020?style=for-the-badge&logo=gmail&logoColor=white&labelColor=134E5E" alt="Email" /></a>
  <a href="https://www.linkedin.com/in/pritish-saha-436a1922a/"><img src="https://img.shields.io/badge/LinkedIn-Pritish%20Saha-0B1020?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=0A66C2" alt="LinkedIn" /></a>
  <a href="https://scholar.google.com/citations?user=gmXhzpMAAAAJ&hl=en"><img src="https://img.shields.io/badge/Google%20Scholar-Profile-0B1020?style=for-the-badge&logo=googlescholar&logoColor=white&labelColor=4285F4" alt="Google Scholar" /></a>
  <a href="https://huggingface.co/Pritish92"><img src="https://img.shields.io/badge/Hugging%20Face-Pritish92-0B1020?style=for-the-badge&logo=huggingface&logoColor=white&labelColor=FFB000" alt="Hugging Face" /></a>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=20&duration=2800&pause=850&color=71B280&center=true&vCenter=true&width=900&lines=4th-year+Dual+Degree+student+at+IIT+Kharagpur;Building+geometry-aware%2C+memory-augmented+and+agentic+AI;Researching+RL%2C+representation+learning%2C+LLMs+and+multimodal+agents;I+like+systems+where+theory%2C+kernels+and+messy+reality+meet" alt="Typing summary" />
</p>

---

### Research Compass

I am a 4th-year Dual Degree student at **IIT Kharagpur** working toward a career in **AI research and innovation**. My north star is to build intelligent agents that can learn from limited data, infer hidden structure, remember without brittle retrieval, adapt efficiently, and make decisions under uncertainty.

I am especially interested in **interactive agent learning**, **reinforcement learning**, **representation learning**, **generative and graphical models**, **continual learning**, **causality**, and **multimodal/embodied intelligence**. I enjoy problems that sit between principle and production: deriving the learning signal, implementing the system, optimizing the kernels, and making the thing run at scale.

```text
Current question I keep circling back to:
How do we build agents that turn sparse feedback, multiple modalities,
latent world structure, and long-horizon memory into robust behavior?
```

---

### Education And Foundations

**Indian Institute of Technology, Kharagpur**  
Dual Degree in Manufacturing Science and Engineering, 2022-2027

**Academic base:** Safety Fundamentals of Generative AI, Operations Research, Probability and Statistics, Linear Algebra, Stanford CS229, Stanford CS230, LLM Agents MOOC, Algozenith, Summer Analytics.

**Beyond research:** Codeforces Pupil, KodeinKGP Senior AI Developer, interhall football and water polo, karate black belt, and NSS volunteering around nearby village development.

---

### Current Research Threads

| Thread | What I am building | Why it matters |
|---|---|---|
| **Geometry-aware LLM adaptation** | First-author work on **GRIT**, a PEFT method using rank-space K-FAC preconditioning, Fisher-guided reprojection, and dynamic LoRA rank adaptation. | Adapt foundation models with fewer trainable parameters while reducing drift and catastrophic forgetting. |
| **Learned memory in transformers** | Co-authored **Mixture of Chapters**, scaling learned latent memory banks with MoE-style chapter routing up to 262K memory tokens. | Move beyond pure parametric memory and text-only retrieval toward addressable, trainable memory substrates. |
| **RL for reasoning models** | Developing **LaViDA**, a reward-gated latent auxiliary objective augmenting GRPO for math LLM training. | Improve reasoning behavior by shaping latent dynamics, not just final-answer reward. |
| **Latent inference in transformers** | Research Fellow at **Cambridge AI Safety Hub**, probing whether causal transformers infer multi-timescale Bayesian hidden states. | Understand when model internals recover structured latent state, and how that structure separates across layers/subspaces. |
| **Medical LLM safety and antidistillation** | Evaluating unsafe behavior in medical LLMs and engineering token-level decoding defenses such as **FROST**. | Make specialized LLMs safer under domain shift, adversarial prompts, and deployment constraints. |

---

### Selected Publications

| Work | Venue / Status | My role | Highlights |
|---|---|---|---|
| **[Mixture of Chapters: Scaling Learnt Memory in Transformers](https://arxiv.org/abs/2603.21096)** | ICLR 2026 NFAM Workshop | Co-author | Sparse learned memory banks, cross-attention retrieval, chapter routing, 262K latent tokens, stronger knowledge retention under IFT. [OpenReview](https://openreview.net/forum?id=uwnwGYICWe) / [Code](https://github.com/Tasmay-Tibrewal/Memory) |
| **[GRIT: Geometry-Aware PEFT with K-FAC Preconditioning, Fisher-Guided Reprojection, and Dynamic Rank Adaptation](https://arxiv.org/abs/2601.00231)** | arXiv preprint | First author | Curvature-aware LoRA adaptation; rank-space natural-gradient proxy; Fisher-spectrum rank allocation; ~46% average trainable-parameter reduction vs LoRA baselines. |

---

### Research And Engineering Experience

| Role | Lab / Organization | Focus |
|---|---|---|
| **Research Fellow, MARS 4.0** | Cambridge AI Safety Hub | Bayesian mixed-state geometry and multi-timescale latent inference in transformers under Prof. Fernando Rosas. Decoded a 6D Bayesian posterior from residual streams with high linear recoverability and ran temporal/shuffle/untrained controls. |
| **Research Intern** | Complex Networks Research Lab, IIT Kharagpur | LaViDA for math LLM training under Prof. Pawan Goyal. Built VRAM-optimized GRPO loops using LoRA-r64, vLLM, FlashAttention, and single-H100 rollout scaling. |
| **Research Intern** | RAAPID INC | Built GRIT from scratch under Prof. Amitava Das. Authored Triton/CUDA kernels for covariance accumulation and Cholesky-heavy natural-gradient updates, plus medical LLM safety evaluation and antidistillation work. |
| **Senior AI Developer** | KodeinKGP, IIT Kharagpur | Led AI selections, workshops, technical writing, and hackathon support for the campus developer community. |

---

### Systems, Competitions, And Projects

| Project | Result | Technical shape |
|---|---|---|
| **GenAI Analytics Dashboard** | Runner-up, General Championship Data Analytics, IIT Kharagpur | Full-stack NLQ analytics for Frammer AI using LangGraph, self-healing SQL, KPI labs, and synthetic star-schema evaluation. |
| **[Amazon ML Challenge 2025](https://github.com/PritishSaha92/Amazon-ML-25)** | 40.8 SMAPE | Stacked Qwen2.5-VL-3B SFT with LightGBM over CLIP/text features; offline tensorization, WebDataset, 4-bit QLoRA, Pseudo-Huber loss, monotonic constraints. |
| **American Express Campus Challenge** | National Finalist, Decision Science Track | 3-stage GBDT-Transformer ranking ensemble; 3k+ leakage-free temporal features; Transformer trained on GBDT residuals with listwise ranking loss. |
| **Hugging Face artifacts** | [13 models and 4 datasets](https://huggingface.co/Pritish92) | LLM fine-tunes, GRIT/LoRA checkpoints, ARC-style reasoning datasets, and instruction-tuning datasets. |

---

### Toolkit

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,cpp,c,linux,docker,git,pytorch,fastapi,latex" alt="Core tools" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/CUDA-0B1020?style=flat-square&logo=nvidia&logoColor=white" alt="CUDA" />
  <img src="https://img.shields.io/badge/Triton-0B1020?style=flat-square" alt="Triton" />
  <img src="https://img.shields.io/badge/JAX-0B1020?style=flat-square&logo=jax&logoColor=white" alt="JAX" />
  <img src="https://img.shields.io/badge/Transformers-0B1020?style=flat-square&logo=huggingface&logoColor=white" alt="Transformers" />
  <img src="https://img.shields.io/badge/vLLM-0B1020?style=flat-square" alt="vLLM" />
  <img src="https://img.shields.io/badge/FlashAttention--2-0B1020?style=flat-square" alt="FlashAttention-2" />
  <img src="https://img.shields.io/badge/PEFT%20%2F%20LoRA-0B1020?style=flat-square" alt="PEFT and LoRA" />
  <img src="https://img.shields.io/badge/TRL-0B1020?style=flat-square" alt="TRL" />
  <img src="https://img.shields.io/badge/bitsandbytes-0B1020?style=flat-square" alt="bitsandbytes" />
  <img src="https://img.shields.io/badge/LangGraph-0B1020?style=flat-square" alt="LangGraph" />
  <img src="https://img.shields.io/badge/WebDataset-0B1020?style=flat-square" alt="WebDataset" />
  <img src="https://img.shields.io/badge/ChromaDB-0B1020?style=flat-square" alt="ChromaDB" />
</p>

**Comfort zones:** LLM fine-tuning, PEFT, RLHF/RLAIF-style training, GRPO, CUDA/Triton kernels, representation probing, multimodal pipelines, ranking systems, RAG/agentic workflows, and production-oriented ML infrastructure.

---

### What I Like Working On

- Agents that learn from interaction, sparse reward, demonstrations, and world feedback.
- RL viewed through state-visitation distributions, occupancy matching, and useful abstraction learning.
- Multimodal systems that transfer structure across language, vision, action, and latent memory.
- Efficient LLM adaptation where optimization geometry, systems constraints, and safety all matter.
- Research code that survives contact with GPUs, ablations, reproducibility, and deadlines.

---

### GitHub Snapshot

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=PritishSaha92&show_icons=true&hide_border=true&theme=transparent&title_color=71B280&text_color=C9D1D9&icon_color=71B280&bg_color=0B1020" alt="Pritish's GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=PritishSaha92&layout=compact&hide_border=true&theme=transparent&title_color=71B280&text_color=C9D1D9&bg_color=0B1020" alt="Pritish's top languages" />
</p>

---

### Open To

Research collaborations, rigorous engineering projects, and conversations around **RL**, **efficient LLM adaptation**, **agent learning**, **multimodal representation learning**, **mechanistic interpretability**, and **AI safety**.

<p align="center">
  <a href="mailto:pritish171@gmail.com"><b>Email</b></a> |
  <a href="https://www.linkedin.com/in/pritish-saha-436a1922a/"><b>LinkedIn</b></a> |
  <a href="https://scholar.google.com/citations?user=gmXhzpMAAAAJ&hl=en"><b>Scholar</b></a> |
  <a href="https://github.com/PritishSaha92"><b>GitHub</b></a> |
  <a href="https://huggingface.co/Pritish92"><b>Hugging Face</b></a>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&height=120&section=footer&color=0:71B280,55:134E5E,100:0B1020" alt="Footer wave" />
</p>




