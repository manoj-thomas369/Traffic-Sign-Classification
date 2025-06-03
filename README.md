
# 🚦 Traffic Sign Classification
## 🧠 Overview

This project builds a deep learning model to **classify traffic signs** using image data. It aims to support **autonomous driving** and **intelligent traffic systems** by detecting traffic signs in real-time.

---

## 🎯 Business Objective

- Improve road safety by helping vehicles recognize traffic signs accurately.
- Assist autonomous vehicles and smart systems with real-time classification.
- Handle classification under diverse conditions (angles, lighting, occlusion).
- Enable scalable, automated traffic monitoring and control.

---

## 📊 Dataset

- **Source**: Provided directory containing labeled traffic sign images.
- **Classes**: 43 types of traffic signs.
- **Image Format**: RGB, resized to 50x50 pixels.

---

## 🛠 Preprocessing

- Resized images to uniform shape (50x50x3)
- Converted grayscale images to RGB
- Encoded class labels (one-hot encoding)
- Normalized pixel values (0–1 range)

---

## 🧪 Train-Test Split

- 80% Training
- 20% Testing
- Stratified sampling to maintain class balance

---

## 🧠 Model Architectures & Performance

| Model         | Accuracy | Loss   |
|---------------|----------|--------|
| CNN           | 98.54%   | 0.0561 |
| DenseNet121   | 97.62%   | 0.1056 |
| MobileNetV2   | 63.16%   | 3.1149 |

✅ CNN achieved the **best performance** among all models.

---

## ✅ Final Recommendation

**Deploy the CNN Model** – It achieved the highest accuracy (*98.54%*) and lowest loss (*0.0561*), making it the most reliable and efficient choice for traffic sign classification, especially with limited computational resources.

---

## 🔄 Further Enhancements

- **Add Real-time Functionality** – Integrate the model with a camera feed using OpenCV.
- **Optimize for Deployment** – Convert CNN model to a lightweight format (e.g., TensorFlow Lite) for Raspberry Pi or mobile devices.
- **Data Augmentation** – Enhance training data variety to improve model robustness.
- **Evaluation Metrics** – Use confusion matrix and classification report to analyze misclassifications and guide further model refinement.

---

## 💻 How to Run

1. Mount Google Drive in Google Colab.
2. Upload dataset into `/sign_detection` with subfolders: `Train`, `Test`, and `labels.csv`
3. Run all cells in the notebook sequentially.

---

## 📦 Installation

```bash
pip install tensorflow keras opencv-python matplotlib seaborn
