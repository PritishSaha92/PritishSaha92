# Pritish Saha

Final-year student at **IIT Kharagpur** working across reinforcement learning and reasoning, predictive-state representations and agent memory, model internals, optimization for efficient adaptation, and reliable evaluation under policy change.

[Website](https://pritishsaha92.github.io/) / [IIT KGP email](mailto:pritish.saha@kgpian.iitkgp.ac.in) / [Gmail](mailto:pritish171@gmail.com) / [LinkedIn](https://www.linkedin.com/in/pritish-saha-436a1922a/) / [Google Scholar](https://scholar.google.com/citations?user=gmXhzpMAAAAJ&hl=en) / [Hugging Face](https://huggingface.co/Pritish92) / [CV](https://pritishsaha92.github.io/data/Pritish_CV.pdf)

## Research interests

Most of my work asks what a model has actually learned when it succeeds, what its data can really tell us, and how both hold up when the objective or policy changes.

Current themes:

- Reinforcement learning for reasoning, especially how latent signals can provide useful credit beyond outcome rewards and why predictivity alone may not be enough to change a policy.
- Predictive-state representations and agent memory, especially what must be retained for control and transfer under partial observability.
- Reliable evaluation under adaptive data collection and changing policies.
- Model internals, deep-learning optimization, and efficient adaptation through representation analysis, Fisher geometry, PEFT, and GPU systems.

## Selected research

### LaViDA: representation-level credit for mathematical reasoning

My BTP at the **Complex Networks Research Group (CNeRG), IIT Kharagpur**, supervised by Prof. Pawan Goyal, studies whether latent representations can provide useful credit beyond exact-match rewards in GRPO. The broader question is how a predictive signal becomes a training signal that changes the model's policy.

- Built a Qwen2.5-Math-7B GRPO pipeline with LoRA-r64, vLLM, and FlashAttention on a single H100, using 8,963 self traces and 3,354 filtered Oracle traces.
- In a seed-0 comparison, the Oracle-augmented nearest-MSE arm improved `n=8` mean correctness by `+4.70pp` over GRPO. Because its reference data and training route also differed, I treat this as an arm-level comparison rather than evidence for the objective alone.
- An oracle-conditioned audit distinguished successful from unsuccessful rollouts, but the latent signal barely changed normalized credit and provided no learning signal when every sampled answer was wrong.

[BTP slides](https://pritishsaha92.github.io/data/BTP2_ppt.pdf)

### Predictive-state geometry in transformers and RL agents

**MARS 4.0 Fellow** at the **Cambridge AI Safety Hub**, supervised by Prof. Fernando Rosas. Using analytically tractable transducer worlds, I study how models represent Bayesian predictive state and what changes when those representations are adapted for decision-making through reinforcement learning.

- Built hierarchical-HMM and ε-transducer environments with exact Bayesian filters and predictive geometry.
- Decoded fully observed Bayesian beliefs at `R²=0.985–0.997` in four-layer transformer pilots trained for 100k updates, well above shuffled and untrained controls.
- Added exact KL-regularized POMDP solvers and reward-switch assays to connect predictive representations with control under changing objectives.

[Week-one MARS presentation](https://drive.google.com/file/d/1e1NrSwDkh5JacG8v2lmQSzG7bedZAJMd/view?usp=sharing)

### GRIT: geometry-aware PEFT

First author of the **[GRIT arXiv preprint](https://arxiv.org/abs/2601.00231)**, developed at **RAAPID INC** with Prof. Amitava Das. GRIT treats adapter updates as a geometric object using rank-space K-FAC, Fisher-guided reprojection, dynamic rank adaptation, and guarded high-rank-to-low-rank compression.

- Built the framework for LLM adaptation under parameter and forgetting constraints.
- Implemented fused Triton kernels for covariance fusion, GPU-side Cholesky inversion, and batched preconditioning.
- Built asynchronous CUDA streams that overlap K-FAC inversions and eigensolves with training across 60+ LoRA modules.
- On GSM8K with Llama-3.1-8B, GRIT reached `66.19%` versus `63.38%` for LoRA with a `27.8%` smaller effective active update footprint.
- Exported a `32%` smaller adapter with less than `0.04` percentage points of accuracy loss.

The wider internship also included rebuilding clinical NER evaluation and deterministic QC, reaching `0.640` exact micro-F1 with zero subword fragments across 5,035 rows.

### Mixture of Chapters: learned memory in transformers

Co-author of **[Mixture of Chapters](https://arxiv.org/abs/2603.21096)**, accepted at the **ICLR 2026 New Frontiers in Associative Memory Workshop**. [OpenReview](https://openreview.net/forum?id=uwnwGYICWe) / [Code](https://github.com/Tasmay-Tibrewal/Memory)

- Added sparse learned memory banks queried by transformer layers through cross-attention.
- Used chapter routing to scale to `262K` learned memory tokens without dense memory access.
- Improved iso-FLOP pretraining loss and retention during instruction fine-tuning.

## Applied systems and competitions

### Fraud-graph systems at Axis Bank

As a Data Science Intern in the **Axis Bank Business Intelligence Unit** (May–July 2026), I built a leakage-free temporal graph pipeline for explainable loan-onboarding fraud review.

- Processed `224.8M` accounts and `1.31B` transfers with PySpark, Hadoop, and HDFS checkpointing.
- Cast fraud proximity as bidirectional, three-hop, time-respecting BFS and reduced the working graph by roughly `20×` while retaining about `80%` applicant coverage.
- Implemented camouflage-aware dense-subgraph signals and delivered a LOAO-validated review queue whose top `1%` achieved `5.49×` mean lift across three monthly cohorts. A separate scorecard indicated a feature rather than model ceiling.

[Final presentation](https://drive.google.com/file/d/1sOSdI06d-h-Mi6OKhAklsaRF8sPu17tN/view?usp=sharing)

- **General Championship Data Analytics, IIT Kharagpur — 3rd Place:** led a GenAI analytics dashboard for Frammer AI with LangGraph, self-healing SQL, NLQ-driven KPI analysis, and synthetic star-schema evaluation. [Presentation](https://drive.google.com/file/d/1VRiHxlmjm4wJ9ezu4tE9BwB5iGUvbngH/view?usp=sharing)
- **[Amazon ML Challenge 2025](https://github.com/PritishSaha92/Amazon-ML-25):** stacked Qwen2.5-VL-3B SFT with LightGBM over CLIP and text features; used WebDataset, 4-bit QLoRA, Pseudo-Huber loss, and monotonic constraints; reached `40.8` SMAPE.
- **[American Express Campus Challenge](https://github.com/PritishSaha92/AmEX-Spacebar-Sketchers-2025) — National Finalist:** built a three-stage GBDT-Transformer ranking ensemble with `3k+` leakage-free temporal features and a listwise Transformer trained on GBDT residuals; final MAP `0.59`.

## Tools I use

`Python`, `C/C++`, `SQL`, `PyTorch`, `JAX`, `FSDP/DTensor`, `CUDA`, `Triton`, `Transformers`, `PEFT/LoRA`, `TRL`, `vLLM`, `FlashAttention-2`, `bitsandbytes`, `PySpark`, `Spark SQL`, `Hadoop/HDFS`, `GraphFrames`, `SLURM`, `Docker`, `Linux`, `Git`, `WebDataset`, `LangGraph`.

## Get in touch

I’m always happy to talk about research and am open to collaborations or research-focused roles beginning in 2027. If our interests overlap, please feel free to reach out.
