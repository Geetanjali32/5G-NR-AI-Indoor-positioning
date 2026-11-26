# 5G-NR-AI-Indoor-positioning
AI/ML-based indoor positioning using 5G NR Channel Impulse Response (CIR), combining CNN and Transformer architectures for accurate UE localization with reduced signal-processing overhead.
# AI/ML-Based Indoor Positioning for 5G NR Systems

## Overview

This project focuses on AI/ML-based direct indoor positioning for 5G New Radio (NR) systems using Channel Impulse Response (CIR) measurements.

A hybrid **Convolutional Neural Network (CNN) and Transformer architecture** is developed to extract spatial-frequency features and capture complex multipath characteristics from wireless channel measurements. The model directly estimates User Equipment (UE) coordinates without relying on explicit ranging or triangulation.

The framework considers a 3GPP-aligned indoor factory environment, focusing on high-accuracy localization and resource-efficient positioning.

## Objectives

- Develop an AI/ML-based direct positioning framework using 5G NR channel measurements.
- Extract meaningful spatial-frequency features from CIR data.
- Capture long-range dependencies using Transformer-based attention mechanisms.
- Estimate UE coordinates through supervised learning.
- Investigate the trade-off between positioning accuracy and data requirements through subcarrier reduction.

## Methodology

The proposed framework consists of the following stages:

1. **System Modelling:** Develop a multi-TRP 5G NR indoor positioning scenario aligned with 3GPP positioning specifications.
2. **Channel Data Processing:** Process complex CIR measurements using magnitude-phase and real-imaginary representations.
3. **Feature Extraction:** Apply convolutional layers to extract local channel characteristics.
4. **Transformer Encoding:** Utilize multi-head self-attention to capture global dependencies across channel features.
5. **Position Estimation:** Use a regression head to estimate the 2D UE coordinates.
6. **Performance Evaluation:** Analyze localization error distributions and investigate reduced-input configurations.

## Model Architecture

The hybrid CNN-Transformer architecture consists of:

- CNN-based feature extraction
- Learnable positional embeddings
- Multi-head self-attention
- Transformer encoder
- Global average pooling
- Fully connected coordinate regression layer

**Framework:** TensorFlow / Keras

## Experimental Results

The proposed architecture demonstrates promising indoor positioning performance in the considered experimental setup.

| Model Configuration | 90th Percentile Error |
|---|---:|
| Proposed CNN-Transformer (Full Input) | 12.7 cm |
| Reduced Input (32 → 8) | 44.36 cm |
| Reduced Input (32 → 16) | 30.95 cm |
| Reference CNN Baseline | 100 cm |

The reduced-input experiments investigate how selecting fewer subcarriers affects positioning accuracy and data requirements.

*Note: These values are results reported for the specific experimental setup and are not general performance guarantees.*

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

## Key Research Areas

- 5G NR Positioning
- AI/ML for Wireless Communications
- Channel Impulse Response (CIR)
- Deep Learning
- CNN and Transformer Architectures
- Multipath Channel Modelling
- Resource-Efficient Localization

## Future Directions

- Investigating robustness under dynamic multipath and environmental changes.
- Exploring adaptive subcarrier selection strategies.
- Improving computational efficiency for practical deployment.
- Evaluating generalization across different indoor environments.
- Extending the framework towards 5G-Advanced and 6G positioning applications.

## Research Context

This work explores the application of deep learning and signal processing techniques to improve indoor positioning accuracy in next-generation wireless communication systems.

---

**Note:** The original simulation datasets and proprietary simulator components are not included in this repository. Reproduction requires access to authorized datasets.
