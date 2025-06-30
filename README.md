# Fooling the Fact-Checkers: Adversarial Attacks on Transformer-Based Fake News Detection Models

## Overview
This repository contains the code, models, and attack recipes from our research paper:

**"Fooling the Fact-Checkers: Adversarial Attacks on Transformer-Based Fake News Detection Models"**  
S M Jeevan, Ayush Sahu, Mentor Name  
Bennett University, 2025  
Manuscript submitted to the International Journal of Multimedia Information Retrieval.

## Project Description
We systematically analyze the adversarial vulnerabilities of three transformer-based models—**BERT**, **DistilBERT**, and **RoBERTa**—for fake news detection using the [Indian Fake News Detection (IFND) dataset]. Despite achieving high accuracy (BERT: 99.81%, DistilBERT: 97.32%, RoBERTa: 99.86%) on clean data, all models are susceptible to carefully crafted adversarial attacks.

Our key contributions:

- **Three-tier adversarial attack framework**: Implements character-level, word-level, and sentence-level perturbations to expose model weaknesses. Sentence-level attacks are most effective (success rates: 47.8–52.3%)[1][2].
- **Comparative robustness analysis**: DistilBERT (34.8% average attack success rate) shows comparable adversarial robustness to RoBERTa (34.5%) despite being 40% smaller.
- **Hybrid defense strategy**: Combines adversarial training and attention masking, reducing attack success rates by 42% with minimal impact on classification accuracy (maintaining 98.7%).
- **Reproducibility**: Public release of attack scripts and robust model checkpoints to support further research in adversarial NLP security.

## Features
- End-to-end training and evaluation scripts for BERT, DistilBERT, and RoBERTa.
- Modular adversarial attack pipeline with:
  - Character-level visual perturbations (e.g., "credit" → "cred1t")
  - Word-level synonym substitutions
  - Sentence-level semantic rephrasings (back-translation, style transfer)
- Hybrid defense implementation (adversarial training + attention masking)
- Detailed performance and robustness metrics (accuracy, F1, attack success rate, semantic similarity)
- Utilities for dataset preprocessing and evaluation

## Dataset

- **Indian Fake News Detection (IFND) dataset**
  - 4,261 labeled news articles (2,130 real, 2,131 fake)
  - Covers political, health, social, and other domains
  - [Dataset preprocessing scripts included]
