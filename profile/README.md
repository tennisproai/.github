<p align="center">
  <img src="https://raw.githubusercontent.com/tennisproai/.github/main/profile/assets/logo.svg" alt="TennisProAI Logo" width="200"/>
</p>

<h1 align="center">TennisProAI</h1>

<p align="center">
  <strong>AI-powered tennis stroke analysis using Apple Watch sensor data</strong>
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#repositories">Repositories</a> •
  <a href="#technology-stack">Tech Stack</a>
</p>

---

## Overview

TennisProAI is a complete machine learning pipeline for classifying tennis strokes in real-time using motion sensors from Apple Watch. The system captures accelerometer, gyroscope, and rotation data during tennis sessions and uses deep learning to identify different types of strokes.

## Architecture

```
┌─────────────────┐     ┌──────────────────────┐     ┌───────────────────────┐
│   Apple Watch   │────▶│  tennis-data-labeler │────▶│  tennis-model-training│
│  (Sensor Data)  │     │   (Annotation GUI)   │     │    (ML Pipeline)      │
└─────────────────┘     └──────────────────────┘     └───────────────────────┘
                                                               │
                                                               ▼
                                                     ┌───────────────────┐
                                                     │  CoreML Model     │
                                                     │  (iOS/watchOS)    │
                                                     └───────────────────┘
```

## Repositories

| Repository | Description |
|------------|-------------|
| **tennis-data-labeler** | PyQt5 GUI application for visualizing sensor data, synchronizing with video, and manually labeling tennis strokes |
| **tennis-model-training** | LSTM neural network training pipeline with feature engineering and CoreML export |
| **tennis-shot-detector** | iOS/watchOS app for real-time stroke detection |

## Supported Strokes

| Stroke | Description |
|--------|-------------|
| 🎾 **Forehand** | Forehand drive |
| 🎾 **Backhand** | Backhand drive |
| ⏸️ **No Stroke** | Non-stroke movements |

## Technology Stack

| Layer | Technologies |
|-------|--------------|
| **Data Collection** | Apple Watch (accelerometer, gyroscope, rotation rate) |
| **Annotation** | Python, PyQt5, Matplotlib |
| **ML Training** | TensorFlow/Keras, LSTM neural networks, scikit-learn |
| **Experiment Tracking** | Weights & Biases |
| **Deployment** | CoreML for iOS/watchOS |

## Model Performance

| Metric | Value |
|--------|-------|
| **Accuracy** | 93% on test set |
| **Architecture** | 2-layer LSTM (64 → 32 units) with dropout |
| **Features** | 17 engineered features from raw sensor data |
| **Sequence Length** | 200 timesteps (2 seconds at 100Hz) |

---

<p align="center">
  <sub>Built with ❤️ for tennis players who want to improve their game</sub>
</p>
