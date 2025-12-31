☯️ AcuModel & AcuAgent: Intelligent Acupuncture Diagnosis System

AcuModel and AcuAgent represent a cutting-edge solution for intelligent acupuncture diagnosis and treatment. By combining domain-specific Large Language Models (LLMs) with a robust multi-agent architecture, this project addresses the challenges of complex meridian theory understanding and clinical reasoning in Traditional Chinese Medicine (TCM).

🚀 Key Innovations

Our system introduces several groundbreaking features tailored for the acupuncture domain:

🧠 1. AcuModel: Domain-Specific LLM with DPO
We present AcuModel, built upon the Qwen2.5-7B-Instruct base. Unlike general medical models, AcuModel undergoes a rigorous training process:
Two-Stage SFT: We utilize a "General Medical Logic -> Acupuncture Domain Knowledge" learning path to ensure both medical common sense and deep professional expertise.
Direct Preference Optimization (DPO): We employ expert-aligned preference data to significantly enhance the model's clinical reasoning reliability and reduce hallucinations.

🤖 2. AcuAgent: Multi-Agent Collaboration
To simulate real-world doctor-patient interactions, we designed AcuAgent, a system centered on AcuModel that coordinates specialized sub-agents.
AcuRouter (Semantic Task Routing):** A lightweight, millisecond-level routing mechanism based on multi-feature fusion (keywords, semantic similarity, and syntactic patterns). It dynamically distributes user intents to the most appropriate processing module (Clinical Diagnosis vs. Knowledge Query).
Graph-Driven Reverse Reasoning: Addressing sparse patient descriptions, AcuAgent utilizes the Acupuncture Knowledge Graph (AcuKG). It leverages co-occurrence laws (e.g., "Same Acupoint Treating Multiple Symptoms") to proactively generate follow-up questions, guiding the user to a complete symptom profile.

📚 3. Multi-Source Knowledge Fusion
Our architecture integrates structured and unstructured knowledge to ensure precision:
AcuKG: Contains ~39,000 semantic triplets (Meridian-Acupoint-Symptom-Treatment).
RAG Module: Retrieval-Augmented Generation based on 500+ ancient and modern acupuncture classics.
Clinical Databases:** Standardized acupoint positioning and symptom-acupoint mapping.

🏆 4. Specialized Evaluation Benchmarks
We constructed two dedicated datasets to standardize evaluation in the field:
SCQ-AcuBench: 1,030 objective questions testing theoretical mastery (Meridians, Acupoints).
QA-AcuEval: 600 clinical cases assessing reasoning and treatment plan generation.



📊 Performance

Experimental results demonstrate that AcuModel achieves scores of 0.7911 and 0.7072 on SCQ-AcuBench and QA-AcuEval, respectively. With the AcuAgent architecture, performance on clinical case evaluation is further elevated to 0.8507, significantly outperforming baseline models like AcuGPT, HuatuoGPT, and LLaMA-3.1.

🛠️ System Architecture

The AcuAgent workflow follows a "Route-Interact-Retrieve-Generate" closed-loop:

1.  User Query ➡️ AcuRouter (Intent Recognition)
2.  Clinical Diagnosis ➡️ Interactive Agent (Reverse Reasoning via AcuKG)
3.  Knowledge Query ➡️ RAG / Database Agent (Retrieval & Reranking)
4.  Final Response ➡️ AcuModel (Polished, Evidence-Based Output)

We are committed to the principles of Responsible AI in medicine. Given the clinical nature of the AcuModel and the potential risks associated with deploying generative models in real-world healthcare scenarios without supervision, we have decided to manage the distribution of the full model weights and training datasets.

While the source literature (such as ancient TCM classics) is public, the high-quality instruction tuning datasets and expert-aligned preference data constructed in this study represent significant proprietary curation and annotation efforts.

We enthusiastically support academic research. If you are a researcher or practitioner intending to use AcuAgent for non-commercial, academic purposes, we are more than happy to provide access.

To request access, please contact us:

Email: 2024920301@stu.haut.edu.cn

Subject: [Academic Request] Access to AcuModel & Data

Content: Please include a brief introduction of your research team and the intended use of the model.

We verify requests to prevent misuse and foster a safe research community. We look forward to your email!

