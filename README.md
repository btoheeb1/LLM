# Evaluating Fine-Tuned LLMs vs Retrieval-Augmented Generation (RAG) Systems

Overview
--------
This project systematically evaluates and compares fine-tuned Large Language Models (LLMs) with Retrieval-Augmented Generation (RAG) systems in terms of performance, efficiency, and resource utilization.
We explore the trade-offs between these two approaches, focusing on when each method is most effective in real-world applications where data evolves and computational resources are limited.

Background
----------
Fine-Tuning (LoRA & QLoRA): Adapt pre-trained LLMs by training only small parameter matrices (adapters), reducing computation and memory requirements.

RAG: Augments LLMs with external knowledge retrieval during inference, enabling dynamic adaptation without retraining.

Methodology
-----------
Model Selection: Used LLaMa variants (e.g., 7B, 13B) as base models.

Fine-Tuning: Applied LoRA and QLoRA for parameter-efficient adaptation.

RAG Pipeline: Indexed the Dive into Deep Learning (d2l.ai) textbook and connected it to LLMs via a retriever.

Evaluation: Compared model outputs to source textbook content using prompts, analyzing:
Loss, Perplexity, and Computational cost.

Data Source: Unified corpus from Dive into Deep Learning ensured identical conditions for both methods.

Key Findings
-------------
LoRA fine-tuning improved relevance and specificity for task-specific queries.
RAG excelled when rich, domain-specific external content was available.

References
-----------
Zhang, A., et al. (2021). Dive into Deep Learning. https://d2l.ai
Hu, E. J., et al. (2021). LoRA: Low-Rank Adaptation of Large Language Models. arXiv:2106.09685
Dettmers, T., et al. (2023). QLoRA: Efficient Finetuning of Quantized LLMs. arXiv:2305.14314
Touvron, H., et al. (2023). LLaMA 2: Open Foundation and Fine-Tuned Chat Models. arXiv:2307.09288
