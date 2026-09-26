# 🌾 AgriLoan-Risk: Agricultural Loan Risk Prediction

> **My first complete Data Science & Machine Learning project**

AgriLoan-Risk is my first complete Data Science and Machine Learning project, where I explored how **financial, climate, and agricultural information** can be used together to understand agricultural loan risk.

The project started with a simple question:

> **Can agricultural loan risk be understood better by looking beyond financial information alone?**

To explore this question, I worked with a dataset containing **30,660 observations** and developed three different machine learning approaches covering **crop-loss prediction and loan-default prediction**.

---

## 📌 Project Overview

Agricultural loan repayment is closely connected to the success of farming.

A farmer may have a stable financial profile when taking a loan, but later face repayment difficulties because of:

* Poor harvest
* Extreme weather
* Pest problems
* Poor soil conditions
* Irrigation issues
* Previous crop losses
* Other agricultural risks

Because of this, this project explores whether combining **financial + climate + agricultural information** can provide additional signals for predicting loan default.

---

## 🎯 Objectives

The project focuses on four main questions:

1. Can climate and agricultural information help predict crop loss?
2. How well can financial information predict loan default?
3. Does adding climate and agricultural information improve loan-default prediction?
4. How do different machine learning models perform across these approaches?

---

## 📊 Dataset

The dataset contains **30,660 observations** with information related to:

### 🌦️ Climate Features

* Rainfall
* Humidity
* Temperature
* Sunshine
* Wind
* Atmospheric pressure
* Weather-stress indicators

### 🌱 Agricultural Features

* District
* Crop type
* Soil type
* Farm size
* Soil quality
* Pest risk
* Irrigation availability
* Crop insurance
* Previous crop loss
* Farm vulnerability

### 👨‍🌾 Farmer Features

* Farmer age
* Education level

### 💰 Financial Features

* Annual income
* Loan amount
* Debt-to-income ratio
* Previous repayment score
* Household expense ratio
* Financial resilience score
* Credit-risk index

### 🎯 Target Variables

* `crop_loss`
* `loan_default`

---

# 🔬 Three Experimental Approaches

Instead of putting every feature into one model from the beginning, I divided the project into three controlled approaches.

### Approach A — Financial Baseline

```text
Financial Features
        ↓
   Loan Default
```

This approach establishes a baseline for predicting loan default using financial information alone.

---

### Approach B — Climate + Agriculture

```text
Climate Features
       +
Agricultural Features
        ↓
     Crop Loss
```

This approach explores whether production-related information can help predict crop loss.

---

### Approach C — Integrated Agricultural Risk

```text
Financial Features
       +
Climate Features
       +
Agricultural Features
        ↓
   Loan Default
```

This is the main experiment of the project.

The purpose was to determine whether adding climate and agricultural information could improve loan-default prediction compared with the financial-only baseline.

---

# 🤖 Machine Learning Models

For each approach, I experimented with four classification algorithms:

* Logistic Regression
* Random Forest
* XGBoost
* CatBoost

This resulted in a total of:

> **3 Approaches × 4 Models = 12 Machine Learning Experiments**

The goal was not to assume that a more complex model would always perform better, but to compare different models using the same evaluation framework.

---

# ⚙️ Data Science Workflow

```text
Raw Dataset
     ↓
Data Understanding
     ↓
Data Cleaning
     ↓
Missing Value Analysis
     ↓
Categorical & Numerical Feature Processing
     ↓
Exploratory Data Analysis
     ↓
Feature Grouping
     ↓
Train-Test Split
     ↓
Model Training
     ↓
Model Comparison
     ↓
Evaluation
     ↓
Final Model Selection
```

---

# 📈 Model Evaluation

I evaluated the models using multiple metrics instead of relying only on accuracy:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC
* Confusion Matrix

This was an important part of the project because a model can achieve relatively high accuracy while still missing a significant number of positive cases.

---

# 🧪 Experimental Results

### Financial Baseline

The strongest financial-only model in my experiments was **CatBoost**.

| Metric   | Result |
| -------- | -----: |
| Accuracy | 81.85% |
| F1-score | 35.33% |
| ROC-AUC  | 77.14% |

### Integrated Agricultural Risk

The selected integrated model was **Logistic Regression**.

| Metric   | Result |
| -------- | -----: |
| Accuracy | 83.40% |
| F1-score | 46.76% |
| ROC-AUC  | 83.08% |

### Financial Baseline vs Integrated Approach

| Metric   | Financial Baseline | Integrated Approach | Improvement |
| -------- | -----------------: | ------------------: | ----------: |
| Accuracy |             81.85% |              83.40% |    +1.55 pp |
| F1-score |             35.33% |              46.76% |   +11.43 pp |
| ROC-AUC  |             77.14% |              83.08% |    +5.94 pp |

Within this dataset and experimental setup, the integrated approach showed stronger overall predictive performance than the financial-only baseline.

---

# 🏆 Final Models

Based on the experiments:

### Crop-Loss Prediction

**Logistic Regression**

ROC-AUC:

```text
80.14%
```

### Loan-Default Prediction

**Logistic Regression**

Accuracy:

```text
83.40%
```

ROC-AUC:

```text
83.08%
```

The final model selection was based on the observed experimental results and the balance between performance and interpretability.

This does **not** mean Logistic Regression will always be the best model for agricultural datasets. It was the strongest choice among the models tested in this particular study.

---

# 💡 What I Learned

This project was an important learning experience for me because it was my **first complete Data Science and Machine Learning project**.

Through this project, I learned how to:

* Understand a real-world-style dataset
* Clean and prepare data
* Work with categorical and numerical features
* Perform exploratory data analysis
* Organize features into meaningful groups
* Build classification models
* Compare multiple ML algorithms
* Evaluate models using multiple metrics
* Understand the importance of recall and F1-score
* Compare a baseline model with an integrated approach
* Interpret machine learning results
* Document a complete data science workflow

One of the biggest lessons was that **high accuracy alone does not tell the complete story**.

Looking at precision, recall, F1-score, ROC-AUC, and confusion matrices helped me understand model performance more carefully.

---

# 📁 Repository Structure

```text
agri-loan-risk-prediction/
│
├── data/
│   └── agri_loan_risk.csv
│
├── notebooks/
│   └── agri_loan_risk_analysis.ipynb
│
├── reports/
│   └── agri_loan_risk_report.pdf
│
├── README.md
├── requirements.txt
├── .gitignore
└── LICENSE
```

---

# 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* XGBoost
* CatBoost
* Jupyter Notebook

---

# 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/agri-loan-risk-prediction.git
```

### 2. Open the project

```bash
cd agri-loan-risk-prediction
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook notebooks/agri_loan_risk_analysis.ipynb
```

---

# 🔮 Future Improvements

There are several ways I would like to improve this project in the future:

* Hyperparameter optimization
* Cross-validation
* Better handling of class imbalance
* Decision-threshold optimization
* Probability calibration
* SHAP-based model explainability
* Temporal validation
* Cross-district validation
* External validation using larger real-world datasets
* Updated weather and agricultural information
* Deployment through an API
* Interactive web-based prediction system

---

# ⚠️ Limitations

The loan-related dataset used in this project was prepared for research purposes because actual borrower-level banking data is private and confidential.

Therefore, the results should **not** be interpreted as evidence of real-world lending performance.

A future version would require real-world banking and agricultural credit data, proper validation, and a real-world pilot study before practical deployment.

---

# 📄 Research Report

A detailed report describing the methodology, experiments, results, limitations, and future work is available in:

```text
reports/agri_loan_risk_report.pdf
```

---

# 👨‍💻 About This Project

This project represents an important milestone in my journey into **Data Science and Machine Learning**.

It is my first project where I tried to follow a complete workflow:

> **Problem → Data → Analysis → Feature Design → Machine Learning → Evaluation → Comparison → Conclusion**

I built this project to strengthen my understanding of practical machine learning and to learn how data-driven solutions can be applied to real-world problems.

---

## ⭐ Future Direction

This project is also the starting point of my journey toward building more advanced systems involving:

**Data Science → Machine Learning → Generative AI → AI Engineering**

More advanced AI and ML projects will be added to my portfolio as I continue learning and building.
