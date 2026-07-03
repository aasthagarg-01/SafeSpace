# SafeSpace: AI-Based Multimodal Stress Detection Platform

SafeSpace is an intelligent mental health support platform that detects stress levels using a multimodal deep learning approach. The system analyzes physiological signals, facial expressions, audio patterns, and psychological survey responses to provide accurate stress prediction along with personalized AI-based recommendations.

The project combines Machine Learning, Deep Learning, IoT-based physiological sensing, and Generative AI to create an end-to-end stress detection and wellness assistance system.

---

# Overview

Stress detection is challenging because human emotions cannot always be identified accurately using a single source of information. A person may appear calm externally while experiencing high internal stress.
SafeSpace solves this limitation by combining multiple indicators:

- Physiological body signals
- Facial expression analysis
- Voice emotion analysis
- Psychological questionnaire responses

Predictions from individual models are combined using an Agreement-Aware Fusion technique to generate a more reliable final stress classification.
The system also integrates an LLM-based assistant that provides personalized stress management suggestions based on the detected stress level.

---

# Key Features

- Multimodal stress detection system
- Facial emotion recognition using CNN
- Audio-based stress analysis using MFCC features
- Physiological signal classification using Deep Neural Networks
- DASS-21 based psychological survey analysis
- Agreement-Aware Fusion for combining model predictions
- AI-generated personalized wellness recommendations
- Real-time web application interface
- Wearable sensor integration for physiological monitoring

---

# System Architecture

The SafeSpace pipeline consists of four independent stress detection modules followed by decision-level fusion.


User Input
│
├── Facial Expression
│   └── CNN Model
│
├── Audio Signal
│   └── MFCC Extraction + CNN Model
│
├── Physiological Signals
│   └── Deep Neural Network
│
├── Survey Responses
│   └── Neural Network Model
│
↓
Agreement-Aware Fusion
↓
Stress Classification
↓
AI Recommendation System


---

# Tech Stack

## Machine Learning & Deep Learning

- Python
- TensorFlow
- PyTorch
- Scikit-learn
- OpenCV
- Librosa
- NumPy
- Pandas

## Frontend

- React.js
- TypeScript
- Vite
- Tailwind CSS

## Backend & Integration

- Python
- Supabase
- API Integration

## Generative AI

- Hugging Face Transformers
- Microsoft Phi-2
- Whisper Speech-to-Text Model

## Hardware Integration

- ESP32 Microcontroller
- EDA Sensor
- MAX30102 Pulse Sensor
- Temperature Sensor
- Accelerometer Module

---

# Dataset Information

Multiple datasets were used to train different stress detection modules.

| Modality | Dataset | Details |
|--------|---------|---------|
| Physiological Signals | WorkStress3D | EDA, BVP, temperature, accelerometer readings |
| Facial Expression | WorkStress3D Facial Dataset | 48x48 facial emotion images |
| Audio | RAVDESS Dataset | Emotional speech recordings |
| Survey | DASS-21 Dataset | Depression, anxiety and stress questionnaire responses |

---

# Machine Learning Models

| Module | Model Used | Purpose |
|------|------------|---------|
| Facial Analysis | CNN | Extract facial stress patterns |
| Audio Analysis | CNN + MFCC Features | Detect emotional patterns from speech |
| Physiological Analysis | Deep Neural Network | Classify stress using biosignals |
| Survey Analysis | Feedforward Neural Network | Analyze psychological responses |
| Recommendation System | LLM | Generate personalized suggestions |

---

# Multimodal Fusion Approach

SafeSpace uses an Agreement-Aware Fusion (AAF) technique instead of simple averaging.

Each model generates an individual stress probability score.

The fusion algorithm:

- Measures agreement between different modalities
- Assigns higher importance to reliable predictions
- Reduces the effect of inconsistent outputs
- Produces the final stress confidence score

This improves robustness compared to single-modality stress detection systems.

---
