# Pritish Saha

Final-year student at **IIT Kharagpur** working on reinforcement learning for reasoning, learned state representations, mechanistic supervision, efficient adaptation, and memory in neural systems.

[Email](mailto:pritish171@gmail.com) / [LinkedIn](https://www.linkedin.com/in/pritish-saha-436a1922a/) / [Google Scholar](https://scholar.google.com/citations?user=gmXhzpMAAAAJ&hl=en) / [Hugging Face](https://huggingface.co/Pritish92) / [CV](https://github.com/PritishSaha92/PritishSaha/blob/main/data/Pritish_CV.pdf)

## Research taste

I study how agents turn experience into reusable internal structure. The question I keep returning to is whether a model that reaches the right answer learned a robust internal strategy or a shortcut that happened to work. I like problems where behavior, representation, and causal interventions have to tell the same story.

Current themes:

- Reinforcement learning for reasoning, especially the limits of outcome-only rewards and opportunities for latent or process-level supervision.
- Bayesian belief states, coarse-graining, state abstractions, and mechanistic analysis of learned representations.
- Efficient LLM adaptation through PEFT, Fisher geometry, natural-gradient-style updates, and forgetting control.
- Learned memory and interactive agents that acquire transferable structure from limited feedback.

## Selected research

### LaViDA: latent supervision for mathematical reasoning

My BTP at the **Complex Networks Research Lab, IIT Kharagpur**, supervised by Prof. Pawan Goyal, asks whether outcome-only GRPO leaves useful reasoning structure on the table. LaViDA supplements verified rewards with representation-level alignment toward expert reasoning traces.

- Built a Qwen2.5-Math-7B GRPO pipeline with LoRA-r64, vLLM, FlashAttention, self-distilled traces, and a filtered Oracle-augmented pool from Qwen2.5-Math-72B-Instruct.
- Compared GRPO, chi-square LaViDA, nearest-expert alignment, self-only attribution, and SFT under leakage-aware evaluation.
- Nearest-expert alignment tied GRPO on greedy MATH-500 and improved `n=8` mean correctness by `+4.70pp` (`p=0.0069`); the harder L4-5 subset improved by `+5.77pp` (`p=0.0429`).
- The learned chi-square critic was null, motivating CR-LaViDA: a prompt-exclusive contrastive reformulation rather than density-ratio matching.

[BTP slides](https://github.com/PritishSaha92/PritishSaha/blob/main/data/BTP2_ppt.pdf)

### Belief-state geometry in transformer ε-transducers

Research Fellow in **[MARS 4.0](https://drive.google.com/file/d/1e1NrSwDkh5JacG8v2lmQSzG7bedZAJMd/view?usp=sharing)** at the **Cambridge AI Safety Hub**, supervised by Prof. Fernando Rosas. I study Bayesian belief-state geometry and coarse-graining in transformer ε-transducers.

- Devised hierarchical-HMM and ε-transducer pipelines with exact joint and coarse-grained Bayesian belief operators.
- Probed 4-layer causal transformers and linearly decoded input and transducer beliefs at `R² ≈ 0.99`, with next-token loss at the computed entropy-rate floor.
- Found that coarse-graining hides roughly `93%` of the fully observable input belief while preserving most transducer belief.
- Used shuffle, untrained, sequence-level cross-validation, and temporal controls to distinguish learned geometry from probe leakage.

### GRIT: geometry-aware PEFT

First author of **[GRIT](https://arxiv.org/abs/2601.00231)**, developed at **RAAPID INC** with Prof. Amitava Das. GRIT treats adapter updates as a geometric object using rank-space K-FAC, Fisher-guided reprojection, dynamic rank adaptation, and guarded high-rank-to-low-rank compression.

- Built the framework for LLM adaptation under parameter and forgetting constraints.
- Implemented fused Triton kernels for covariance fusion, GPU-side Cholesky inversion, and batched preconditioning.
- Built a dual-stream CUDA pipeline that overlaps stale-by-one curvature work with the next training step.
- Targets competitive generative and NLU performance while reducing trainable parameters by `25-80%`.

### Mixture of Chapters: learned memory in transformers

Co-author of **[Mixture of Chapters](https://arxiv.org/abs/2603.21096)**, accepted at the **ICLR 2026 New Frontiers in Associative Memory Workshop**. [OpenReview](https://openreview.net/forum?id=uwnwGYICWe) / [Code](https://github.com/Tasmay-Tibrewal/Memory)

- Added sparse learned memory banks queried by transformer layers through cross-attention.
- Used chapter routing to scale to `262K` learned memory tokens without dense memory access.
- Improved iso-FLOP pretraining loss and retention during instruction fine-tuning.

## Applied systems and competitions

### Fraud-graph systems at Axis Bank

As a Data Science Intern in the **Axis Bank Business Intelligence Unit** (May-July 2026), I built a leakage-free temporal graph pipeline for explainable loan-onboarding fraud review.

- Processed `224.8M` accounts and `1.31B` transfers with PySpark, Hadoop, and HDFS checkpointing.
- Cast fraud proximity as bidirectional, three-hop, time-respecting BFS and reduced the working graph by roughly `20x` while retaining about `80%` applicant coverage.
- Implemented camouflage-aware dense-subgraph signals and delivered a LOAO-validated review queue; the closest band reached roughly `81x` the portfolio fraud rate, while a separate scorecard indicated a feature rather than model ceiling.

[Final presentation](https://drive.google.com/file/d/1sOSdI06d-h-Mi6OKhAklsaRF8sPu17tN/view?usp=sharing)

- **General Championship Data Analytics, IIT Kharagpur — Runner-up:** led a GenAI analytics dashboard for Frammer AI with LangGraph, self-healing SQL, NLQ-driven KPI analysis, and synthetic star-schema evaluation. [Presentation](https://drive.google.com/file/d/1VRiHxlmjm4wJ9ezu4tE9BwB5iGUvbngH/view?usp=sharing)
- **[Amazon ML Challenge 2025](https://github.com/PritishSaha92/Amazon-ML-25):** stacked Qwen2.5-VL-3B SFT with LightGBM over CLIP and text features; used WebDataset, 4-bit QLoRA, Pseudo-Huber loss, and monotonic constraints; reached `40.8` SMAPE.
- **[American Express Campus Challenge](https://github.com/PritishSaha92/AmEX-Spacebar-Sketchers-2025) — National Finalist:** built a three-stage GBDT-Transformer ranking ensemble with `3k+` leakage-free temporal features and a listwise Transformer trained on GBDT residuals; final MAP `0.59`.

## Tools I use

`Python`, `C/C++`, `PyTorch`, `JAX`, `CUDA`, `Triton`, `Penzai`, `Transformers`, `PEFT/LoRA`, `TRL`, `vLLM`, `FlashAttention-2`, `bitsandbytes`, `PySpark`, `Spark SQL`, `Hadoop/HDFS`, `Impala`, `GraphFrames`, `FastAPI`, `Docker`, `Linux`, `WebDataset`, `LangGraph`, `ChromaDB`, `Git`.

## What I am looking for

I am most excited by research on RL for reasoning, mechanistic supervision, latent-state interpretability, efficient adaptation, learned memory, and agents that acquire useful abstractions through interaction.
