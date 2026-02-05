<p align="center">
  <img src="https://raw.githubusercontent.com/tennisproai/.github/main/profile/assets/logo.svg?v=2" alt="TennisProAI - Infinity Ball" width="240"/>
</p>

<h1 align="center">Tennis Pro <span style="color: #D45C11;">AI</span></h1>

<p align="center">
  <strong>The Infinity Loop of Excellence</strong><br/>
  <em>AI-powered tennis stroke analysis using Apple Watch sensor data</em>
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#architecture">Architecture</a> •
  <a href="#repositories">Repositories</a> •
  <a href="#technology-stack">Tech Stack</a>
</p>

---

## Overview

Tennis Pro AI is a complete machine learning pipeline for classifying tennis strokes in real-time using motion sensors from Apple Watch. The system captures accelerometer, gyroscope, and rotation data during tennis sessions and uses deep learning to identify different types of strokes.

> *"An unbroken cycle of data-driven coaching — where every swing is recorded, analyzed, and transformed into improvement."*

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
| **tennis-data-labeler** | PyQt5 GUI for visualizing sensor data, video sync, and manual stroke labeling |
| **tennis-model-training** | LSTM neural network training pipeline with feature engineering and CoreML export |
| **tennis-shot-detector** | iOS/watchOS app for real-time stroke detection |

## Supported Strokes

| Stroke | Description |
|--------|-------------|
| **Forehand** | Forehand drive |
| **Backhand** | Backhand drive |
| **No Stroke** | Non-stroke movements |

## Technology Stack

| Layer | Technologies |
|-------|--------------|
| **Data Collection** | Apple Watch (accelerometer, gyroscope, rotation rate) |
| **Annotation** | Python, PyQt5, Matplotlib |
| **ML Training** | TensorFlow/Keras, LSTM, scikit-learn |
| **Experiment Tracking** | Weights & Biases |
| **Deployment** | CoreML for iOS/watchOS |

## Model Performance

| Metric | Value |
|--------|-------|
| **Accuracy** | 93% on test set |
| **Architecture** | 2-layer LSTM (64 → 32 units) |
| **Features** | 17 engineered features |
| **Sequence Length** | 200 timesteps (2s @ 100Hz) |

---

<p align="center">
  <sub>Built for tennis players who want to improve their game</sub><br/>
  <sub><strong>Continuous Progression</strong> • <strong>Dynamic Balance</strong> • <strong>Infinite Potential</strong></sub>
</p>
