# MR604 - Parameter-Efficient Fine-Tuned Small Language Models for Resource-Efficient Academic Support Question Answering

**Author:** Shrawan Thapa (MIT243335)
**Degree:** Master by ICT Research
**Module:** MR604 Research Project

## Overview

This repository contains all implementation notebooks and evaluation results for my master thesis:
*Parameter-Efficient Fine-Tuned of Small Language Models for Resource efficient Question Answering*

Six fine-tuning conditions were evaluated using LoRA and QLoRA across three models on the SyllabusQA dataset with BM25Okapi retrieval-augmented context.

| ID | Model | Strategy | F1 (%) | VRAM (GB) |
|----|-------|----------|--------|-----------|
| R1 | Phi-3-mini-4k | LoRA | 19.701 | 4.982 |
| R2 | Phi-3-mini-4k | QLoRA | **20.084** | **3.237** |
| R3 | Mistral-7B | LoRA | 15.249 | 9.108 |
| R4 | Mistral-7B | QLoRA | 14.891 | 6.543 |
| R5 | Gemma-2B | LoRA | 17.432 | 4.871 |
| R6 | Gemma-2B | QLoRA | 16.987 | 3.912 |

**Best configuration:** Phi-3-mini QLoRA (R2) - composite score 87.659

## Repository Structure

    notebooks/   - Five Colab training and evaluation notebooks
    results/     - All CSV and JSON evaluation outputs (CONTEXT-aware)

## Notebooks

| Notebook | Purpose |
|----------|---------|
| MR604_Notebook1_Gemma2B | Gemma-2B LoRA and QLoRA training and evaluation |
| Phi_3_mini_4k_instrucct_ | Phi-3-mini LoRA and QLoRA training and evaluation |
| MR604_Notebook3_Mistral7B | Mistral-7B LoRA and QLoRA training and evaluation |
| MR604_Notebook4_Cross_Model | Cross-model comparison, Pareto analysis, composite scoring |
| MR604_FULL_PHASE_COMBINED_POC | Combined analysis and proof-of-concept Gradio application |

## Requirements

- Python 3.10+
- transformers >= 4.40.0
- peft >= 0.10.0
- bitsandbytes >= 0.43.0
- trl >= 0.8.6
- datasets
- rank_bm25
- gradio >= 4.0.0
- Google Colab (A100 GPU recommended)

## Citation

S. Thapa, *Parameter-Efficient Fine-Tuned Small Language Models for Resource-Efficient Academic Support Question Answering*. MR604 Master Thesis, (2026).
