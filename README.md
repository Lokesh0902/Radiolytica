# 🩻 Radiolytica: AI-Enhanced Radiology Workflow Revolution

Radiolytica is a deep learning-based diagnostic support system that assists radiologists in detecting **Pneumonia**, **Tuberculosis**, and **Cardiomegaly** from chest X-ray images. It provides rapid, interpretable, and accurate predictions with Grad-CAM visualizations and severity scoring, all through a secure and user-friendly web interface.

---

## 🚀 Features

- 🔍 **Lung Segmentation** using a custom-trained U-Net model
- 🧠 **Pneumonia & Tuberculosis Detection** using fine-tuned DenseNet201 models
- ❤️ **Cardiomegaly Detection** via Cardiothoracic Ratio (CTR) calculation
- 📈 **Grad-CAM Heatmaps** for visual interpretability
- 📋 **Severity Scoring** for Pneumonia & TB
- 📂 **Image Upload Interface** (Flask-based)
- 💾 **Patient Record Logging** for follow-up analysis

---

## 🧠 System Architecture

User Upload X-ray → Preprocessing → → Lung Segmentation → → Disease Classification (DenseNet201) → → Heatmap Generation (Grad-CAM) → → Cardiomegaly Detection (CTR) → → Web Interface Output


---

## 🧰 Technologies Used

| Task                        | Technology / Model              |
|----------------------------|----------------------------------|
| Frontend Interface         | HTML, CSS, JavaScript           |
| Backend                    | Flask (Python)                  |
| Pneumonia Detection        | DenseNet201 + Grad-CAM          |
| Tuberculosis Detection     | DenseNet201 + Grad-CAM          |
| Lung Segmentation          | U-Net (Custom trained)          |
| Cardiomegaly Detection     | CTR (image-based calculation)   |
| Image Preprocessing        | CLAHE, Gaussian Blur, Canny     |


---

## 🖼 Sample Output

- ✅ Disease prediction (Normal / Pneumonia / TB / Cardiomegaly)
- 🔥 Grad-CAM overlay within segmented lung region
- 🧮 Cardiothoracic Ratio with threshold comparison
- 📊 Severity scoring based on intensity of infection

---

📌 Notes
Lung segmentation masks are applied before Grad-CAM to focus only on relevant areas.

The project uses mixed precision training and warm-up cosine decay learning rate schedules for optimized GPU training.

Predictions are stored in the backend for further analysis or audit trails.

🧪 Evaluation Metrics
Accuracy, Precision, Recall, F1-Score

ROC-AUC

Specificity (for TB/Pneumonia)

CTR Threshold (≥ 0.50 → Cardiomegaly

## 🔗 Model Downloads

You can download the trained model files used in this project from the links below:

- 🫁 **Lung Segmentation Model (U-Net)**: [Download from Kaggle](https://www.kaggle.com/models/lokesh0929/unet_segmentation)
- 📦 Pneumonia & TB Classifier models will be added upon request.
