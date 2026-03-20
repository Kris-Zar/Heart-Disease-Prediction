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
├── Heart_Disease.csv                # Dataset (not included — see Dataset section)
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

## ⚙️ Workflow

```
1. Load Dataset
       ↓
2. Data Preprocessing
   - Drop irrelevant columns (education)
   - Rename columns for clarity
   - Handle missing values (mean fill)
       ↓
3. Feature Selection & Splitting
   - Select 6 key features
   - 70/30 train-test split (random_state=4)
       ↓
4. Feature Scaling
   - StandardScaler normalization
       ↓
5. Model Training
   - Logistic Regression
       ↓
6. Evaluation
   - Accuracy Score
   - Classification Report
   - Confusion Matrix Heatmap
```

---

## 📈 Model & Results

**Model Used:** `sklearn.linear_model.LogisticRegression`

**Evaluation Metrics:**
- ✅ Accuracy Score
- ✅ Precision, Recall, F1-Score (via Classification Report)
- ✅ Confusion Matrix (visualized as a heatmap)

**Sample Output:**

```
Train Set: (2803, 6), (2803,)
Test Set:  (1202, 6), (1202,)

Accuracy Score: ~0.85
```

> Actual results may vary slightly depending on your dataset version.

---

## 🛠️ Requirements

Install all dependencies with:

```bash
pip install -r requirements.txt
```

**Required Libraries:**

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

Or install manually:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn notebook
```

---

## 🚀 Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/heart-disease-prediction.git
   cd heart-disease-prediction
   ```

2. **Add the dataset:**
   - Download `Heart_Disease.csv` from [Kaggle](https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset)
   - Place it in the project root directory

3. **Update the dataset path in the notebook:**
   ```python
   # Change this line in the notebook:
   disease_data = pd.read_csv('Heart_Disease.csv')
   ```

4. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook Heart_Disease_Prediction.ipynb
   ```

5. **Run all cells** (`Kernel → Restart & Run All`)

---

## 📉 Visualizations

The notebook includes:

- **Count Plot** — Distribution of patients with and without 10-year CHD risk
- **Confusion Matrix Heatmap** — Visual breakdown of True/False Positives and Negatives

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for improvements such as:

- Adding more models (Random Forest, XGBoost, SVM)
- Hyperparameter tuning
- Feature engineering
- Cross-validation

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## 👤 Author

**Your Name**
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [your-linkedin](https://linkedin.com/in/your-linkedin)

---

> ⭐ If you found this project helpful, give it a star!
