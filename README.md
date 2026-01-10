# Automated Cataract Classification using Deep Learning 👁️

![Status](https://img.shields.io/badge/Status-IEEE_Presented-blue)
![Accuracy](https://img.shields.io/badge/Best_Accuracy-96%25-success)
![Framework](https://img.shields.io/badge/Framework-TensorFlow-orange)

## 📌 Project Overview
This project focuses on the automated binary classification of ocular images into **Cataract** and **Normal** categories. The core contribution of this work is a rigorous **Comparative Analysis** of 5 different Deep Learning architectures to identify the most effective model for medical diagnosis.

> **Current Scope:** Binary Classification (Cataract vs Normal).
> **Future Scope:** Integration of XAI (Grad-CAM) for lesion localization.

## 🔬 Comparative Analysis (Benchmark Results)
We trained and validated 5 architectures. **VGG16** emerged as the best performing model with **96% validation accuracy**, followed closely by MobileNetV2.

| Rank | Model Architecture | Validation Accuracy | Performance Verdict |
|------|-------------------|---------------------|---------------------|
| 🥇 | **VGG16** | **96.0%** | ✅ **Best Model (Winner)** |
| 🥈 | MobileNetV2 | 95.0% | Excellent & Lightweight |
| 🥉 | InceptionV3 | 94.0% | Very Good |
| 4 | Custom CNN | 94.0% | Good Baseline |
| 5 | DenseNet121 | 93.0% | Moderate |

## 🛠️ Methodology
- **Data Augmentation:** Utilized `ImageDataGenerator` (Rotation, Zoom, Flip) to handle class imbalance.
- **Preprocessing:** Images were resized to **150x150 pixels** and normalized to scale pixel values (0-1).
- **Optimizer:** Adam Optimizer with Categorical Cross-Entropy Loss.

## 📄 Publication
**Presented at IEEE IETACS 2025 Conference (Mohali).**
*Title: Deep Learning-Based Cataract Detection Using CNN Architectures.*
*(Proceedings to appear in IEEE Xplore).*

## 👨‍💻 Tech Stack
- **Languages:** Python
- **Libraries:** TensorFlow, Keras, NumPy, Pandas, Matplotlib
