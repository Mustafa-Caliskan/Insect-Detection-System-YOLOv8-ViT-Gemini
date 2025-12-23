# 📂 Trained Model Weights

Due to the large file size of high-performance deep learning models, the weights are hosted externally on Google Drive. 

### 🔗 Download Link
You can access all model versions (Baseline & Augmented) here:
👉 **[Access Model Weights on Google Drive](https://drive.google.com/drive/folders/1pA1X1xzFEiqZ38rm4fWkWOxOI_S2SDX2?usp=sharing)**

---

### 🧠 Model Specifications

#### 1. YOLOv8m (Detection)
- **Baseline:** Trained on 19,000 raw insect images.
- **Augmented:** Trained on 45,500 enhanced images for superior localization.
- **Format:** PyTorch (`.pt`)

#### 2. Vision Transformer - ViT (Classification)
- **Architecture:** `google/vit-base-patch16-224-in21k`
- **Output:** Fine-tuned for 20 insect species.
- **Format:** HuggingFace Model Weights (`pytorch_model.bin` / `config.json`)

### 🛠️ How to Use
1. Download the weights from the link above.
2. Place the YOLO `.pt` file and the ViT folder into your local `/proje_model` directory.
3. Update the `MODEL_PATH` variable in the notebook to match your local path.
