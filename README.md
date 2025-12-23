🐝 Hybrid Insect Detection & Smart Agricultural AI Consultant
This project presents a state-of-the-art hybrid AI solution for identifying agricultural insects and providing expert-level farming advice. It combines the speed of YOLOv8, the precision of Vision Transformers (ViT), and the reasoning power of Google Gemini 2.0 Flash.

🏗️ System Architecture
Detection (Localization): YOLOv8m identifies insect coordinates in the field.

Classification (Diagnosis): A fine-tuned Vision Transformer (ViT) classifies species with 99% accuracy.

Decision Support (LLM): Google Gemini 2.0 Flash generates professional reports based on the insect category (Harmful, Beneficial, or Neutral).

📊 Performance & Data Science Experiment
We evaluated the impact of data augmentation on model performance, scaling the dataset from 19,000 to 45,500 images.
YOLOv8 Performance (Baseline vs. Augmented)
Metric,Baseline (19k),Augmented (45.5k)
Visual Result,,
ViT Classification Results
The Vision Transformer achieved near-perfect diagonal clarity on the confusion matrix after augmentation.

Visual Evidence: See results/confusion_matrix_vit_augmented.png for detailed class separation.

📂 Repository Structure
/notebooks: Contains Baseline and Augmented pipeline notebooks.

/results: Includes Confusion Matrices, Training Metrics, and Dashboards.

/models: Technical specifications and external hosting for weights.

/docs: Project documentation and supplementary files.

🔗 Links & Resources
Trained Model Weights (Google Drive): Download "proje_model" Folder Here.

Baseline Notebook:

Optimized (Augmented) Notebook:

🛡️ Security & Integrity Notes
Data Safety: The linked Google Drive folder is set to Viewer mode; files cannot be deleted or modified by external users.

Notebook Execution: Clicking "Open in Colab" creates a temporary copy in the user's environment; the original source on GitHub remains untouched.

API Keys: Remember to use your own GEMINI_API_KEY for execution.

Developed as part of an advanced AI research project with a focus on sustainable agriculture.
