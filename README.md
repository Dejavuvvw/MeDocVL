# MeDocVL
official repo of "MeDocVL: A Visual Language Model for Medical Document Understanding and Parsing"

## Abstract
Medical document OCR is challenging due to complex layouts, domain-specific terminology, and noisy annotations, while requiring strict field-level exact matching. Existing OCR systems and general-purpose vision–language models often fail to reliably parse such documents. We propose `MeDocVL`, a post-trained vision–language model for query-driven medical document parsing.
Our framework combines **Training-driven Label Refinement** to construct high-quality supervision from noisy annotations, with a **Noise-aware Hybrid Post-training** strategy that integrates reinforcement learning and supervised fine-tuning to achieve robust and precise extraction. Experiments on medical invoice benchmarks show that MeDocVL consistently outperforms conventional OCR systems and strong VLM baselines, achieving state-of-the-art performance under noisy supervision.