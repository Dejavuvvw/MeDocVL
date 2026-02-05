# MeDocVL

![MeDocVL Comparison Bar](assets/MeDocVL-Comparison%20Bar.png)
*Comparison of query-driven document parsing performance on medical document.*
*Public model is trained exclusively on publicly available datasets, while Extended model is trained with additional non-public data to study the effect of increased training data scale.*

## Abstract
Medical document OCR is challenging due to complex layouts, domain-specific terminology, and noisy annotations, while requiring strict field-level exact matching. Existing OCR systems and general-purpose vision–language models often fail to reliably parse such documents. We propose `MeDocVL`, a post-trained vision–language model for query-driven medical document parsing.
Our framework combines **Training-driven Label Refinement** to construct high-quality supervision from noisy annotations, with a **Noise-aware Hybrid Post-training** strategy that integrates reinforcement learning and supervised fine-tuning to achieve robust and precise extraction. Experiments on medical invoice benchmarks show that MeDocVL consistently outperforms conventional OCR systems and strong VLM baselines, achieving state-of-the-art performance under noisy supervision.


# Dataset
We re-annotated the invoices from the [Alibaba Cloud Tianchi invoice dataset](https://tianchi.aliyun.com/dataset/131815) to align with our internally labeled, proprietary data. We then reproduced our method on this dataset.

In this setup, Stage 1 contains 700 samples, and Stage 2 contains 100 samples. To simulate realistic annotation noise, we introduced artificial noise into the manually labeled Stage 1 dataset, with a noise ratio of 30%.
- stage 1 with human-annotated label: `dataset/a_li_yun_medical_train_stage1.jsonl`
- stage 2 with human-annotated label: `dataset/a_li_yun_medical_train_stage2.jsonl`
- test data with human-annotated label: `dataset/a_li_yun_medical_test.jsonl`
- stage 1 with noisy label: `dataset/a_li_yun_medical_train_stage1_noisy.jsonl`
- stage 1 reduce noisy by judge model: `dataset/a_li_yun_medical_train_stage1_noisy_from_judgeModelPred.jsonl`