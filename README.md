# 💰 Loan Repayment Prediction — Classification Models

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML%20Models-orange?logo=scikitlearn)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-lightgrey?logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

This project builds and evaluates multiple **machine learning classification models** to predict whether a loan applicant will **pay off their loan on time** or have it **go into collection**. Using a real-world-style loan dataset, the project walks through data exploration, feature engineering, model training, and performance evaluation across four different algorithms.

---

## 🎯 Objective

- Explore and visualise a loan dataset to understand patterns in repayment behaviour
- Engineer features (e.g., day of the week the loan was issued, weekend flag) to improve model performance
- Train and compare four classification algorithms: KNN, Decision Tree, SVM, and Logistic Regression
- Evaluate models using Jaccard Index, F1-score, and Log Loss

---

## 📊 Dataset

- **Records:** 346 loan applications
- **Target variable:** `loan_status` — `PAIDOFF` (260 records) or `COLLECTION` (86 records)
- **Key Features:**
  - `Principal` — loan amount
  - `terms` — repayment term length
  - `effective_date` / `due_date` — loan issue and due dates
  - `age` — applicant's age
  - `education` — applicant's education level
  - `Gender` — applicant's gender

---

## 🛠️ Tools & Libraries

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas / NumPy | Data loading, cleaning, and manipulation |
| Seaborn / Matplotlib | Data visualisation |
| Scikit-learn | Model training and evaluation (KNN, Decision Tree, SVM, Logistic Regression) |
| Jupyter Notebook | Interactive analysis environment |

---

## 🔍 Exploratory Analysis & Feature Engineering

- Visualised loan principal and applicant age distributions split by gender and loan status using Seaborn FacetGrids
- Discovered that **applicants who took out loans later in the week (Thursday–Sunday) were less likely to pay off on time**
- Engineered a new binary `weekend` feature (day of week > 3) based on this insight, to help models capture the pattern
- Converted categorical features (`education`, `Gender`) into numeric form for modelling

---

## 🤖 Model Performance

Four classification algorithms were trained and evaluated on a held-out test set:

| Algorithm | Jaccard Index | F1-score | LogLoss |
|-----------|--------------|----------|---------|
| KNN | 0.67 | 0.63 | NA |
| Decision Tree | 0.72 | 0.74 | NA |
| **SVM** | **0.80** | **0.76** | NA |
| Logistic Regression | 0.74 | 0.66 | 0.57 |

**SVM achieved the best overall performance**, with the highest Jaccard Index (0.80) and F1-score (0.76), making it the strongest model for this loan repayment classification task. Logistic Regression was the only model evaluated with Log Loss, since it directly outputs class probabilities.

---

## 📁 Project Structure

```
loan-prediction-ml/
├── ML0101EN-Proj-Loan-answer-py-v1.ipynb   # Full analysis: EDA, feature engineering, model training & evaluation
└── README.md                                # Project documentation (this file)
```

---

## ▶️ How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/Pragati2411/loan-prediction-ml.git
   cd loan-prediction-ml
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook ML0101EN-Proj-Loan-answer-py-v1.ipynb
   ```

---

## 💡 Insights Summary

> Out of 346 applicants, 260 paid off their loans on time while 86 went into collection. Loans issued later in the week showed a higher likelihood of non-repayment, leading to a useful engineered "weekend" feature. Among the four models tested, SVM delivered the best classification performance (Jaccard 0.80, F1-score 0.76), making it the most reliable choice for predicting loan repayment risk in this dataset.

---

## 🔗 Related Projects in This Series

| Project | Description |
|--------|-------------|
| space-falcon-eda | Initial EDA & data wrangling on SpaceX launch data |
| spacex-data-visualization | Visualisations & feature engineering on launch data |
| spacex-sql-analysis | SQL-based analysis of SpaceX launch data |

---

## 👩‍💻 Author

**Pragati Mistry** — Data Analyst | MSc Mathematics | IBM Data Science Professional Certificate  
📍 Surat, India | Open to Remote & Relocating to Mumbai / Hyderabad / Bangalore  
🔗 [GitHub Profile](https://github.com/Pragati2411)
