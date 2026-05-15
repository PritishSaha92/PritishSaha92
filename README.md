# Pritish Saha

4th-year Dual Degree student in Manufacturing Science and Engineering at **IIT Kharagpur**. I work on LLMs, reinforcement learning, and representation-level supervision: how models infer hidden state, adapt without drifting, use memory, and remain monitorable under optimization pressure.

[Email](mailto:pritish171@gmail.com) / [LinkedIn](https://www.linkedin.com/in/pritish-saha-436a1922a/) / [Google Scholar](https://scholar.google.com/citations?user=gmXhzpMAAAAJ&hl=en) / [Hugging Face](https://huggingface.co/Pritish92)

## Research taste

I am interested in the gap between surface behavior and internal computation. A model can pass an evaluation while using the wrong trajectory, exploiting a brittle shortcut, or hiding the state we actually care about. Most of my work tries to make that internal structure measurable or trainable: belief-state probing, latent trajectory alignment, curvature-aware adaptation, and learned memory.

Current themes:

- Reinforcement learning for reasoning models, especially outcome-only RL failures and latent/process-level supervision.
- Representation learning for hidden state, belief geometry, state abstractions, and useful downstream features.
- Efficient LLM adaptation with PEFT, natural-gradient style updates, Fisher structure, and forgetting control.
- Memory-augmented transformers and multimodal/agentic systems that use limited feedback well.

## Selected work

### LaViDA: latent supervision for math RL

My BTP / undergraduate thesis work studies whether outcome-only GRPO leaves useful reasoning structure on the table. LaViDA adds a reward-gated latent alignment signal: correct rollouts are projected through a frozen encoder and pulled toward verified expert reasoning traces.

What I found so far:

- Built a controlled Qwen2.5-Math-7B pipeline with LoRA-r64 GRPO, self-distilled expert traces, and an Oracle-augmented pool from filtered Qwen2.5-Math-72B-Instruct completions embedded on the 7B manifold.
- Compared GRPO-only, chi-square LaViDA, nearest-expert latent alignment, self-only attribution, and SFT on filtered Oracle traces.
- Seed-0 result: nearest-expert latent alignment tied GRPO on greedy MATH-500 but improved `n=8` mean correctness by `+4.70pp` over GRPO (`p=0.0069`).
- The learned chi-square critic was statistically null (`-0.60pp`, `p=0.7051`) with weak training-time alignment (`r~+0.04`), so I am reformulating the auxiliary as CR-LaViDA: a log-space, prompt-exclusive InfoNCE objective rather than density-ratio matching.

### GRIT: geometry-aware PEFT

First author of **[GRIT](https://arxiv.org/abs/2601.00231)**, a curvature-aware LoRA/PEFT method using rank-space K-FAC preconditioning, Fisher-guided reprojection, and dynamic rank adaptation.

- Built the framework from scratch for LLM adaptation under parameter and forgetting constraints.
- Implemented fused Triton kernels for covariance accumulation and GPU-side Cholesky-heavy natural-gradient updates.
- GRIT matches or improves LoRA/QLoRA-style baselines while reducing trainable parameters by `25-80%` across tasks.

### Mixture of Chapters: learned memory in transformers

Co-author of **[Mixture of Chapters](https://arxiv.org/abs/2603.21096)**, accepted at the **ICLR 2026 New Frontiers in Associative Memory Workshop**. [OpenReview](https://openreview.net/forum?id=uwnwGYICWe) / [Code](https://github.com/Tasmay-Tibrewal/Memory)

- Added sparse learned memory banks queried by transformer layers through cross-attention.
- Used MoE-style chapter routing to scale to `262K` learned memory tokens without dense memory attention.
- Improved iso-FLOP pretraining loss and reduced forgetting during instruction fine-tuning.

### Bayesian latent-state probing in transformers

Research Fellow at **Cambridge AI Safety Hub**, working on Bayesian mixed-state geometry and multi-timescale latent inference in transformers.

- Built hierarchical HMM/transducer pipelines with slow hidden drivers, fast dynamics, and exact 6-state Bayesian filters.
- Probed 4-layer causal transformers and linearly decoded the full 6D Bayesian posterior from the residual stream (`R^2=0.982`, `MSE=0.0043`).
- Ran shuffle, untrained, temporal, and layerwise controls to test whether the model is actually tracking hidden state rather than surface statistics.

### Medical LLM safety and antidistillation

At **RAAPID INC**, I also work on medical LLM safety and decoding-time defenses.

- Benchmarked MedGemma on CARES-18K and observed `86%` attack success under unsafe prompt settings.
- Built token-level decoding machinery for FROST-style antidistillation experiments.
- The broader question is whether safety supervision changes internal computation or only trains a shallow output wrapper.

## Projects and competitions

- **General Championship Data Analytics, IIT Kharagpur - Runner-up:** led a GenAI analytics dashboard for Frammer AI with LangGraph, self-healing SQL, NLQ-driven KPI analysis, and Gaussian-anchored synthetic star-schema evaluation.
- **[Amazon ML Challenge 2025](https://github.com/PritishSaha92/Amazon-ML-25):** stacked Qwen2.5-VL-3B SFT with LightGBM over CLIP/text features; used offline tensorization, WebDataset, 4-bit QLoRA, Pseudo-Huber loss, and monotonic constraints; reached `40.8` SMAPE.
- **American Express Campus Challenge - National Finalist:** built a 3-stage GBDT-Transformer ranking ensemble with `3k+` leakage-free temporal features and a Transformer trained on GBDT residuals; final MAP `0.59`.

## Tools I use

`Python`, `C/C++`, `CUDA`, `Triton`, `PyTorch`, `JAX`, `Transformers`, `PEFT/LoRA`, `TRL`, `vLLM`, `FlashAttention-2`, `bitsandbytes`, `Penzai`, `FastAPI`, `Docker`, `Linux`, `WebDataset`, `LangGraph`, `ChromaDB`, `Git`.

## What I am looking for

I am most excited by work where behavior, representation, and causality all have to line up. In practice that means RL for reasoning, mechanistic supervision, latent-state interpretability, efficient adaptation, and agents that learn useful abstractions from limited interaction.

