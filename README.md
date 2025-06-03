# 🛡️ Intrusion Detection System using Hybrid Model (DNN + MLP)

This project implements a deep learning-based **Intrusion Detection System (IDS)** using a **hybrid architecture** that combines a **Deep Neural Network (DNN)** and a **Multi-Layer Perceptron (MLP)**. It is trained and evaluated on the NSL-KDD dataset to classify network traffic as either normal or attack.

---

## 📚 Dataset

- Source: [NSL-KDD Dataset on Kaggle](https://www.kaggle.com/datasets/hassan06/nslkdd)
- Files used:
  - `KDDTrain+.txt`
  - `KDDTest+.txt`

---

## ⚙️ Model Architecture

- **Input features**: 41 features extracted and preprocessed from NSL-KDD
- **Two parallel branches**:
  - **DNN Branch**: Dense(128) → Dropout → Dense(64) → Dropout
  - **MLP Branch**: Dense(64) → Dropout → Dense(32) → Dropout
- Outputs merged using `Concatenate` and passed to a final classification layer
- Binary classification using a `sigmoid` output

Includes regularization and generalization techniques:
- **Dropout**
- **EarlyStopping**
- **Class Weighting**

---

## 📈 Results Summary

The model achieved:
- ✅ High **precision** for detecting attacks
- ⚠️ Moderate **recall** for attack class (some missed detections)
- ⚖️ Balanced performance across normal and malicious classes

---

## 🚀 How to Run This Project

### 1. Clone the Repository

```bash
git clone https://github.com/architakulkarni10/Intrusion-Detection-System-using-Hybrid-Model-DNN-MLP-.git
cd Intrusion-Detection-System-using-Hybrid-Model-DNN-MLP-
