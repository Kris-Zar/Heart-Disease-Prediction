# 🫀 Heart Disease Prediction

A machine learning project that predicts the **10-year risk of coronary heart disease (CHD)** in patients using Logistic Regression — based on clinical and lifestyle features from the Framingham Heart Study dataset.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Features Used](#features-used)
- [Workflow](#workflow)
- [Model & Results](#model--results)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Visualizations](#visualizations)
- [License](#license)
- [Author](#author)

---

## 🔍 Overview

Cardiovascular disease is one of the leading causes of mortality worldwide. This project applies **Logistic Regression** to classify whether a patient is at risk of developing coronary heart disease within the next 10 years, based on demographic and medical attributes.

**Target Variable:** `TenYearCHD` — Binary (0 = No Risk, 1 = At Risk)

---

## 📊 Dataset

- **Source:** [Framingham Heart Study Dataset](https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset) (Heart_Disease.csv)
- **Records:** ~4,000 patient records
- **Task:** Binary Classification

### Key Columns

| Column       | Description                          |
|--------------|--------------------------------------|
| `male`       | Sex of the patient (renamed to `Sex_male`) |
| `age`        | Age of the patient                   |
| `cigsPerDay` | Cigarettes smoked per day            |
| `totChol`    | Total cholesterol level              |
| `sysBP`      | Systolic blood pressure              |
| `glucose`    | Glucose level                        |
| `TenYearCHD` | 10-year risk of CHD (target)         |

> The `education` column was dropped as it was not relevant to the prediction.

---

## 📁 Project Structure

```
Heart-Disease-Prediction/
│
├── Heart_Disease_Prediction.ipynb   # Main Jupyter Notebook
├── Heart_Disease.csv                # Framingham Heart Study dataset
├── requirements.txt                 # Python dependencies
├── LICENSE                          # MIT License
└── README.md                        # Project documentation
```

---

## ✅ Features Used

The following 6 features were selected for training:

```python
X = disease_data[['Sex_male', 'age', 'cigsPerDay', 'totChol', 'sysBP', 'glucose']]
```

- Missing values were handled using **mean imputation**
- Features were scaled using **StandardScaler** for better model performance

---

## 🔄 Workflow

1. **Data Loading** — Import the Framingham CSV dataset
2. **Exploratory Data Analysis (EDA)** — Distribution plots, correlation heatmaps, class imbalance check
3. **Data Preprocessing** — Handle missing values (mean imputation), rename columns, drop irrelevant features
4. **Feature Scaling** — StandardScaler applied to normalize features
5. **Train/Test Split** — 80/20 split with stratification
6. **Model Training** — Logistic Regression classifier
7. **Evaluation** — Accuracy, Confusion Matrix, Classification Report

---

## 📈 Model & Results

| Metric | Score |
|--------|-------|
| Accuracy | ~85% |
| Model | Logistic Regression |
| Scaler | StandardScaler |

> Detailed metrics including precision, recall, and F1-score are available in the notebook.

---

## 📦 Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 Getting Started

1. **Clone the repository**

```bash
git clone https://github.com/Kris-Zar/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run the notebook**

```bash
jupyter notebook Heart_Disease_Prediction.ipynb
```

---

## 📊 Visualizations

The notebook includes:
- Correlation heatmap of all features
- Distribution plots for key features
- Confusion matrix visualization
- Class imbalance analysis

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE).

---

## 👤 Author

**Parth Saxena** — [@Kris-Zar](https://github.com/Kris-Zar)

- 💼 [LinkedIn](https://www.linkedin.com/in/parth-saxena-dev)
- 📧 [lordzar79@gmail.com](mailto:lordzar79@gmail.com)

---

> ⭐ If you found this project useful, consider giving it a star!
