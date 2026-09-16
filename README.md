# AcuModel & AcuAgent: Intelligent Acupuncture Diagnosis System

**AcuModel** is a domain-specific LLM (fine-tuned from Qwen2.5-7B-Instruct) for acupuncture, and **AcuAgent** is a multi-agent system built on top of it that simulates real doctor–patient interactions.

## Highlights

- **AcuModel** — Two-stage SFT (general medical logic → acupuncture knowledge) + DPO with expert-aligned preference data for reliable clinical reasoning.
- **AcuRouter** — Millisecond-level intent routing across Clinical Diagnosis and Knowledge Query via multi-feature fusion (keywords, semantics, syntax).
- **Graph-driven reverse reasoning** — Uses AcuKG (~39K Meridian–Acupoint–Symptom–Treatment triplets) to ask follow-up questions and complete sparse symptom profiles.
- **Multi-source knowledge** — AcuKG + RAG over 500+ acupuncture classics + standardized acupoint/symptom databases.
- **Two benchmarks** — SCQ-AcuBench (1,030 theory questions) and QA-AcuEval (600 clinical cases).

## Results

| Benchmark | AcuModel | AcuModel-AcuAgent | Best Baseline |
|---|---|---|---|
| SCQ-AcuBench (acc) | 0.7911 | — | 0.7629 (AcuGPT) |
| QA-AcuEval (LLM-judge) | 0.6888 | **0.9184** | — |
| Hallucination error rate | 0.3750 | **0.0733** | — |
| Expert blind eval (/100) | 63 | **78** | 59 (AcuGPT) |

Baselines: AcuGPT, HuatuoGPT-o1, MedChatZH, LLaMA-3.1.


## Model & Data Access

To prevent misuse, full weights and tuning datasets are shared for **non-commercial academic use only**. Please email 2024920301@stu.haut.edu.cn with subject `[Academic Request] Access to AcuModel & Data`, including your team intro and intended use.
