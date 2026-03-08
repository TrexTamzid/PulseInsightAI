# 🫀 PulseInsightAI
### Multi-Disease Risk Prediction Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![ML](https://img.shields.io/badge/ML-Scikit--learn%20%7C%20XGBoost-orange?style=flat)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

---

## 📌 Problem Statement

Chronic diseases like **Diabetes, Heart Disease, and Stroke** are among the leading causes of death worldwide. Early detection and preventive action can save millions of lives.

**PulseInsightAI** is a machine learning system that predicts the risk of multiple chronic diseases simultaneously using real-world public health survey data — and provides **actionable, interpretable insights** for healthcare professionals and individuals.

---

## 🎯 Objectives

- Predict the risk of **Diabetes**, **Heart Disease**, and **Stroke** from survey data
- Build a **multi-label classification** system (a patient can have 0, 1, 2, or all 3 conditions)
- Identify the **top risk factors** for each disease using SHAP interpretability
- Discover **high-risk patient clusters** using unsupervised learning
- Deliver results through an **interactive Streamlit dashboard**

---

## 📊 Dataset

| Property | Details |
|---|---|
| Source | [CDC BRFSS](https://www.cdc.gov/brfss/index.html) (Behavioral Risk Factor Surveillance System) |
| Rows | ~400,000 survey responses |
| Features | 50+ (demographics, lifestyle, health indicators) |
| Target Variables | Diabetes (0/1), Heart Disease (0/1), Stroke (0/1) |
| Type | Multi-label binary classification |

---

## 🗂️ Project Structure

```
PulseInsightAI/
│
├── data/
│   ├── raw/                  ← Original CDC BRFSS dataset
│   └── clean/            ← Cleaned & engineered data
│
├── notebooks/
│   ├── 01_EDA.ipynb          ← Exploratory Data Analysis
│   ├── 02_Preprocessing.ipynb← Cleaning & Feature Engineering
│   ├── 03_Modeling.ipynb     ← ML Model Training & Evaluation
│   ├── 04_Clustering.ipynb   ← Dimensionality Reduction & Clustering
│   └── 05_Insights.ipynb     ← SHAP Interpretability & Insights
│
├── src/
│   ├── preprocess.py         ← Data cleaning functions
│   ├── train.py              ← Model training pipeline
│   └── predict.py            ← Prediction functions
│
├── models/                   ← Saved trained models (.pkl)
├── output/
│   └── figures/              ← Saved plots and charts
├── dashboard/
│   └── app.py                ← Streamlit interactive dashboard
│
├── .gitignore
├── requirements.txt
└── README.md
```

---

## 🧠 Input Features

**Demographics**
- Age, Gender, Race, Education, Income, Region

**Lifestyle & Habits**
- Smoking, Alcohol use, Exercise frequency, Diet quality, Sleep hours

**Health Measurements**
- BMI, Blood pressure, Cholesterol levels, Past medical conditions, Medications

**Other Factors**
- Family history, Mental health / stress indicators

---

## ⚙️ Methods & Pipeline

### 1️⃣ Data Cleaning & Preprocessing
- Handle missing values (imputation / dropping)
- One-hot encoding for categorical features
- StandardScaler for numeric features
- Feature engineering: BMI categories, Age groups, Lifestyle composite scores

### 2️⃣ Exploratory Data Analysis (EDA)
- Target variable distribution
- Correlation heatmap
- Key risk factor visualizations
- Class imbalance analysis

### 3️⃣ Machine Learning Models
| Step | Model |
|---|---|
| Baseline | Multi-output Logistic Regression |
| Advanced | Random Forest (Multi-output) |
| Advanced | XGBoost (Multi-output) |

### 4️⃣ Model Evaluation
- Per disease: Accuracy, F1-score, Precision, Recall, ROC-AUC
- Multi-label metrics: Hamming Loss, Subset Accuracy
- Confusion matrix per disease

### 5️⃣ Clustering & Dimensionality Reduction
- PCA / t-SNE / UMAP for 2D/3D visualization
- KMeans & DBSCAN to identify high-risk patient clusters

### 6️⃣ Interpretability
- SHAP values for per-disease feature importance
- LIME for individual prediction explanations
- Top risk factor visualizations

---

## 📈 Results

> *(To be updated as models are trained)*

| Disease | Accuracy | F1-Score | ROC-AUC |
|---|---|---|---|
| Diabetes | - | - | - |
| Heart Disease | - | - | - |
| Stroke | - | - | - |

---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/TrexTamzid/PulseInsightAI.git
cd PulseInsightAI
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add the dataset
Download the CDC BRFSS dataset and place it in:
```
data/raw/
```

### 4. Run the notebooks in order
```
01_EDA.ipynb → 02_Preprocessing.ipynb → 03_Modeling.ipynb → 04_Clustering.ipynb → 05_Insights.ipynb
```

### 5. Launch the dashboard
```bash
streamlit run dashboard/app.py
```

---

## 🛠️ Tools & Libraries

| Category | Tools |
|---|---|
| Language | Python 3.x |
| Data | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn, Plotly |
| Machine Learning | Scikit-learn, XGBoost |
| Interpretability | SHAP |
| Dimensionality Reduction | UMAP-learn |
| Dashboard | Streamlit |
| Environment | Jupyter Notebook / VS Code |

---

## 💡 Real-World Applications

- **Hospitals & Clinics** → Early screening of high-risk patients
- **Insurance companies** → Risk profiling and premium calculation
- **Public Health departments** → Identify at-risk population groups
- **Individuals** → Personal health risk awareness and lifestyle guidance

---

## 👤 Author

**Your Name**
- GitHub: [@TrexTamzid](https://github.com/YOUR_USERNAME)
- LinkedIn: [Tamzid Hossain](https://www.linkedin.com/in/tamzid-hossain-34b856237/overlay/about-this-profile/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base%3BRMM%2FfTtvSVKUiFHYx3rspQ%3D%3D)

---

## 📄 License

This project is licensed under the MIT License.

---

> ⭐ If you found this project useful, please consider giving it a star!