# Credit Card Fraud Detection using Unsupervised Learning

This project explores multiple unsupervised anomaly detection techniques to detect fraudulent credit card transactions on a highly imbalanced dataset.

## 📊 Dataset

- 284,807 transactions
- 492 fraud cases (~0.17%)
- 30 anonymized features (PCA transformed)
- Target: `Class` (0 = Normal, 1 = Fraud)

Dataset source:
https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

⚠️ The dataset is not included in this repository due to size and licensing restrictions.

---

## 🚀 Models Implemented

- Isolation Forest
- Local Outlier Factor (LOF)
- One-Class SVM
- Autoencoder (Neural Network)

---

## 📈 Evaluation Metrics

Because the dataset is extremely imbalanced, the following metrics were used:

- ROC-AUC
- Average Precision (PR-AUC)
- Confusion Matrix
- Precision@K

PR-AUC is emphasized since it is more informative for rare-event detection.

---

## 🏆 Results Summary

| Model | ROC-AUC | PR-AUC |
|-------|---------|--------|
| Autoencoder | ~0.94 | **~0.31** ✅ |
| Isolation Forest | ~0.95 | ~0.16 |
| One-Class SVM | ~0.94 | ~0.10 |
| LOF | ~0.53 | ~0.004 |

The Autoencoder achieved the best Precision-Recall performance.

---

## ⚙️ Installation

```bash
git clone https://github.com/yourusername/credit-card-fraud-anomaly-detection.git
cd credit-card-fraud-anomaly-detection
pip install -r requirements.txt
