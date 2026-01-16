# 👁️ Trustworthy AI for Cataract Classification: From Benchmarking to Ethical Reasoning

![Status](https://img.shields.io/badge/Status-IEEE_Presented-blue?style=flat-square)
![XAI](https://img.shields.io/badge/Feature-Explainable_AI-green?style=flat-square)
![Safety](https://img.shields.io/badge/Safety-Ethical_Guardrails-red?style=flat-square)
![Framework](https://img.shields.io/badge/Framework-TensorFlow-orange?style=flat-square)

## 📌 Project Overview
This project focuses on the automated binary classification of ocular images into **Cataract** and **Normal** categories. 

The project evolved in **two distinct phases**:
1.  **Comparative Analysis:** Benchmarking 5 Deep Learning architectures to find the best backbone.
2.  **Trustworthy AI Implementation:** Enhancing the best-performing model (VGG16) with **Explainability (Grad-CAM), Uncertainty Estimation (MC Dropout), and Ethical Safety Thresholds** for reliable medical diagnostics.

---

## 🏛️ Phase 1: Comparative Analysis (Benchmark Results)
In the initial research phase, we trained and validated 5 different architectures. **VGG16** emerged as the winner with the best balance of accuracy and feature extraction capability.

| Rank | Model Architecture | Validation Accuracy | Performance Verdict |
|------|-------------------|---------------------|---------------------|
| 🥇 | **VGG16** | **96.0%** | ✅ **Selected for Phase 2** |
| 🥈 | MobileNetV2 | 95.0% | Excellent & Lightweight |
| 🥉 | InceptionV3 | 94.0% | Very Good |
| 4 | Custom CNN | 94.0% | Good Baseline |
| 5 | DenseNet121 | 93.0% | Moderate |

> **Outcome:** VGG16 was selected as the backbone for further development due to its superior feature extraction on ocular textures.

---

## 🚀 Phase 2: Advanced Implementation (XAI & Ethics)
In this phase, we prioritized **Reliability over Raw Accuracy**. We fine-tuned the VGG16 model to be stable and transparent rather than just chasing high numbers.

### 📊 The Trade-off: Why 94% > 96%?
We optimized the model for **stability** (smooth loss convergence) instead of aggressive fitting.

| Model Version | Accuracy | Loss Graph | Verdict |
| :--- | :--- | :--- | :--- |
| **V1 (Benchmark)** | **96.00%** | Unstable/Jittery | High accuracy but prone to overfitting. |
| **V2 (Final Ethical Model)** | **94.21%** | **Smooth & Stable** | **Most Reliable.** Fully explainable & safe. |

### 🧠 1. Explainability (Grad-CAM)
The model provides visual reasoning for its predictions. The heatmap below confirms the model focuses strictly on the **lens opacity** (cataract region).

![Grad-CAM Reasoning](screenshots/Grad-CAM%20Reasoning.png)
*(Fig: Left - Original Image, Center - Heatmap, Right - Model focus on the infected lens)*

### 🛡️ 2. Ethical Risk Report & Uncertainty
We implemented an **Ethical Layer** that flags predictions if the model is uncertain (<85% confidence), even if the prediction is technically "correct". This prevents False Negatives in medical screening.

![Ethical Report](screenshots/Ethical%20Report.png)
*(Fig: The system detecting 'Risk' and suggesting medical consultation)*

### 📈 3. Training Stability
The final model demonstrates a robust learning curve with no signs of overfitting.

![Training Graph](screenshots/Training%20Graph.png)

---

## 🛠️ Methodology & Tech Stack
- **Preprocessing:** Resizing (150x150), VGG16-specific normalization.
- **Augmentation:** Rotation, Zoom, Flip using `ImageDataGenerator`.
- **Techniques:** Transfer Learning (ImageNet weights), Monte Carlo (MC) Dropout, Temperature Scaling.
- **Stack:** Python, TensorFlow/Keras, OpenCV, NumPy, Matplotlib.

## 📄 Publication
**Presented at IEEE IETACS 2025 Conference (Mohali).**
*Title: Deep Learning-Based Cataract Detection Using CNN Architectures.*

## 👨‍💻 Author
**[Sourabh]** *Research Focus: Medical AI, Computer Vision, Trustworthy Machine Learning*
