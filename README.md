# 🔐 AI-Powered Intrusion Detection System (Cybersecurity + Machine Learning)

## 📖 Overview
This project is an AI-based Intrusion Detection System (IDS) that classifies network traffic as **Normal** or **Attack** using Machine Learning.

It uses the **NSL-KDD dataset**, a widely used benchmark dataset in cybersecurity, to detect malicious activity in network traffic.

The goal of this project is to combine **Cybersecurity + AI** skills to build a real-world security solution.

---

## 🚀 Features

- Detects malicious network traffic using ML
- Classifies traffic into:
  - ✅ Normal
  - ⚠️ Attack
- Provides:
  - Accuracy score
  - Classification report
  - Confusion matrix
- Feature importance analysis
- Real-time threat detection simulation
- Model saving & loading using `joblib`

---

## 🛠️ Tech Stack

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib

---

## 📂 Dataset

- **NSL-KDD Dataset**
- File used: `KDDTrain+.txt`

---

## ⚙️ Project Workflow

### 1. Data Loading
- Loaded dataset using Pandas
- Assigned column names manually

### 2. Data Preprocessing
- Removed unnecessary column (`difficulty`)
- Converted labels:
  - `normal → normal`
  - others → `attack`

### 3. Encoding
- Categorical columns encoded:
  - protocol_type
  - service
  - flag

### 4. Train-Test Split
- 80% training
- 20% testing

### 5. Model Training
- Used **Random Forest Classifier**
- Trained on network traffic features

### 6. Evaluation
- Accuracy Score
- Classification Report
- Confusion Matrix
- Recall Score (important for attack detection)

### 7. Feature Importance
- Identified top features contributing to attack detection

### 8. Model Saving
- Saved trained model using `joblib`

---

## 📊 Results

- High accuracy in detecting attacks
- Strong recall score for attack class
- Clear separation between normal and malicious traffic

---

## 🧠 Key Learnings

- How intrusion detection systems work
- Handling real cybersecurity datasets
- Feature engineering in security data
- Importance of recall in security models
- Model evaluation in real-world scenarios

---

## 🔍 Sample Prediction

```python
sample = X_test.sample(1)
prediction = model.predict(sample)
