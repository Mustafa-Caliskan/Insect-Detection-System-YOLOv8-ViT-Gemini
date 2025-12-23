# 🛠️ Technical Methodology & System Design

This document provides a deep dive into the hybrid AI architecture used for insect detection and classification.

## 1. Hybrid Pipeline Logic
The system uses a sequential hybrid approach to ensure both speed and high-granularity accuracy:
- **Phase 1 (Localization):** YOLOv8m (Medium) is deployed for real-time object detection. It identifies the presence and bounding box coordinates of insects within a complex agricultural background.
- **Phase 2 (Classification):** Once detected, the cropped image is passed to a **Vision Transformer (ViT)**. ViT uses self-attention mechanisms to capture global dependencies in the image, achieving a classification accuracy of **99%**.
- **Phase 3 (Reporting):** The classification result is sent as a prompt to **Google Gemini 2.0 Flash**, which acts as a virtual agronomist to provide ecological advice.

## 2. Data Science & Augmentation Strategy
A critical part of this project was the transition from a baseline model to an optimized version:
- **Initial Dataset:** 19,000 raw images.
- **Expanded Dataset:** Through advanced augmentation (rotation, scaling, noise injection, and color jittering), the dataset was increased to **45,500 images**.
- **Impact:** As seen in the `results/` directory, this expansion eliminated class confusion and stabilized the loss curves.

## 3. Evaluation Metrics
We use standard computer vision metrics to evaluate performance:
- **mAP (mean Average Precision):** To measure YOLOv8's localization success.
- **Confusion Matrix:** To visualize the ViT model's per-class precision and recall.
- **Loss Curves:** Monitored via the `training_metrics` plots to ensure no overfitting occurred during the 45.5k image training phase.

## 4. Troubleshooting
- **GitHub Rendering:** Large notebook files may occasionally fail to render directly on GitHub. In such cases, the "Open in Colab" badge in the main README is the recommended viewing method.
