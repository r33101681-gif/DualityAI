# DualityAI Falcon – Offroad Semantic Scene Segmentation

## Overview

This project was developed as part of the Duality AI Offroad Semantic Segmentation Hackathon. The primary objective was to train a robust semantic segmentation model capable of understanding and classifying various offroad desert environments using synthetic data generated from Falcon Digital Twin simulations.

The system is designed to perform pixel-level classification for autonomous navigation and terrain understanding in challenging offroad scenarios.

The trained model demonstrates strong performance on unseen environments and achieves a Mean Intersection over Union (mIoU) score of **0.725**.

---

# Problem Statement

Offroad autonomous systems require highly accurate scene understanding for safe navigation, path planning, and obstacle avoidance. Traditional datasets are expensive and time-consuming to collect and annotate, especially for remote desert environments.

To solve this problem, Duality AI provided a synthetic dataset generated using Falcon Digital Twin simulations. The challenge involved training a semantic segmentation model that could generalize effectively across different desert terrains and environmental conditions.

---

# Objectives

- Train a semantic segmentation model using synthetic offroad data
- Improve generalization on unseen environments
- Optimize segmentation accuracy and inference speed
- Analyze failure cases and improve model robustness
- Build a scalable training pipeline for future research

---

# Classes

The segmentation model predicts the following classes:

| Class ID | Class Name |
|----------|-------------|
| 100 | Trees |
| 200 | Lush Bushes |
| 300 | Dry Grass |
| 500 | Dry Bushes |
| 550 | Ground Clutter |
| 600 | Flowers |
| 700 | Logs |
| 800 | Rocks |
| 7100 | Landscape |
| 10000 | Sky |

---

# Project Architecture

The project pipeline consists of the following stages:

1. Dataset Preparation
2. Data Augmentation
3. Model Training
4. Validation
5. Inference
6. Visualization
7. Performance Evaluation

The model was trained using a semantic segmentation architecture optimized for synthetic offroad environments.

---

# Tech Stack

| Component | Technology |
|-----------|------------|
| Framework | PyTorch |
| Language | Python |
| Training Platform | Falcon Digital Twin |
| Model Architecture | DeepLabV3+ |
| GPU Support | CUDA |
| Visualization | OpenCV + Matplotlib |
| Experiment Tracking | TensorBoard |

---

# Dataset Structure

```bash
dataset/
│
├── Train/
│   ├── images/
│   └── masks/
│
├── Val/
│   ├── images/
│   └── masks/
│
└── testImages/
