# MeDocVL

![MeDocVL Comparison Bar](assets/MeDocVL-Comparison%20Bar.png)
*Comparison of query-driven document parsing performance.*
*Public model is trained exclusively on publicly available datasets, while Extended model is trained with additional non-public data to study the effect of increased training data scale.*

official repo of "MeDocVL: A Visual Language Model for Medical Document Understanding and Parsing"

## Abstract
Medical document OCR is challenging due to complex layouts, domain-specific terminology, and noisy annotations, while requiring strict field-level exact matching. Existing OCR systems and general-purpose vision–language models often fail to reliably parse such documents. We propose `MeDocVL`, a post-trained vision–language model for query-driven medical document parsing.
Our framework combines **Training-driven Label Refinement** to construct high-quality supervision from noisy annotations, with a **Noise-aware Hybrid Post-training** strategy that integrates reinforcement learning and supervised fine-tuning to achieve robust and precise extraction. Experiments on medical invoice benchmarks show that MeDocVL consistently outperforms conventional OCR systems and strong VLM baselines, achieving state-of-the-art performance under noisy supervision.