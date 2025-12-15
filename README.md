🫁 Lung Segmentation and Disease Classification using Deep Learning (Explainable AI)

This repository presents an end-to-end deep learning pipeline for automated lung disease detection from chest X-ray images, with a strong focus on explainability and clinical interpretability.
The project integrates lung segmentation, disease classification, and visual explanation into a single unified system and deploys it through an interactive Streamlit web application.

🔍 Project Overview

Manual interpretation of chest X-rays is time-consuming and highly dependent on expert radiologists, especially in low-resource settings. To address this challenge, this project proposes a segmentation-guided and explainable AI framework that:

Precisely segments lung regions from chest X-rays

Performs disease classification (Normal vs Tuberculosis) only on the relevant lung area

Provides visual explanations using Grad-CAM to show where the model is focusing

Offers an easy-to-use web interface for real-time inference

🧠 Methodology

The pipeline consists of three major stages:

1️⃣ Lung Segmentation

Model: U-Net

Accurately isolates lung regions from chest X-rays

Reduces background noise and irrelevant anatomical structures

Achieved a Dice Coefficient of 0.96

2️⃣ Disease Classification

Model: ResNet-18 (transfer learning)

Operates on segmented lung images rather than full X-rays

Improves classification reliability and robustness

Achieved 84% classification accuracy

3️⃣ Explainability (XAI)

Technique: Grad-CAM

Generates heatmaps highlighting lung regions influencing predictions

Enhances transparency and trust in model decisions

🖥️ Web Deployment

The complete pipeline is deployed using Streamlit, enabling users to:

Upload chest X-ray images (PNG/JPG)

View predicted lung masks and masked lungs

Receive disease prediction with confidence score

Visualize Grad-CAM heatmaps for explainability

This makes the system accessible to non-technical users, students, and clinicians.

📊 Results
Task	Metric	Performance
Lung Segmentation	Dice Coefficient	0.96
Disease Classification	Accuracy	84%
Precision	Macro Avg	0.84
Recall	Macro Avg	0.83
F1-Score	Macro Avg	0.84

The segmentation-guided approach significantly outperforms baseline CNN models trained on full images.

🛠️ Tech Stack

Framework: PyTorch

Segmentation: U-Net

Classification: ResNet-18

Explainable AI: Grad-CAM

Image Processing: OpenCV, Pillow

Deployment: Streamlit

⚠️ Disclaimer

This project is intended for research and educational purposes only.
The model was trained on a limited dataset and is not suitable for direct clinical use without extensive validation on large, multi-center datasets.

🚀 Future Work

Training on larger and multi-institutional datasets

Exploring advanced architectures (Vision Transformers, Swin Transformers)

Reducing false negatives for improved clinical reliability

Integrating multimodal clinical data

Privacy-preserving training using federated learning
