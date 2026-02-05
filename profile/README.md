# TennisProAI

AI-powered tennis stroke analysis using Apple Watch sensor data.

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
| [tennis-data-labeler](https://github.com/tennisproai/tennis-data-labeler) | PyQt5 GUI application for visualizing sensor data, synchronizing with video, and manually labeling tennis strokes |
| [tennis-model-training](https://github.com/tennisproai/tennis-model-training) | LSTM neural network training pipeline with feature engineering and CoreML export |
| [tennis-shot-detector](https://github.com/tennisproai/tennis-shot-detector) | iOS/watchOS app for real-time stroke detection |

## Supported Strokes

- **Forehand** - Forehand drive
- **Backhand** - Backhand drive
- **No Stroke** - Non-stroke movements

## Technology Stack

- **Data Collection**: Apple Watch (accelerometer, gyroscope, rotation rate)
- **Annotation**: Python, PyQt5, Matplotlib
- **ML Training**: TensorFlow/Keras, LSTM neural networks
- **Deployment**: CoreML for iOS/watchOS

## Model Performance

- **Accuracy**: 93% on test set
- **Architecture**: 2-layer LSTM (64 → 32 units) with dropout
- **Features**: 17 engineered features from raw sensor data
- **Sequence Length**: 200 timesteps (2 seconds at 100Hz)

## License

MIT License
