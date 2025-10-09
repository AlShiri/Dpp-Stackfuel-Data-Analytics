# Credit Risk Analysis 🚀

> Predicting the probability of loan default based on borrower information.

## 📊 Project Overview

**Problem Statement:** 
Can we predict whether a borrower will be able to pay back the loan or is there a risk of default?

**Goal:** 
The goal of this project is to build a predictive model that estimates the probability of loan default.

**Methods:** 
Exploratory Data Analysis
Logistic Regression

## 🎯 Key Findings

- 📈 **Key finding 1:** Kurze Beschreibung
- 🔍 **Key finding 2:** Kurze Beschreibung  
- 💡 **Key finding 3:** Kurze Beschreibung

## 📁 Repository Structure

```
├── data/
│   ├── raw/                        # Original Data
│   └── credit-risk-dataset         # Original Data 
│       └── credit-risk-dataset.csv # Original Data 
│   └── processed/                  # Cleaned Data
│       └── credit_risk_cleaned.csv # Cleaned Data
├── notebooks/                      # Jupyter Notebooks
│   └── 01_exploration.ipynb        # Datenexploration
│   └── 02_cleaning_loans.ipynb     # Data Cleaning
│   └── 03_eda_loans.ipynb          # EDA
├── src/dpp                         # Python Module
├── test/                           # Unit Tests
├── pyproject.toml                  # Projektkonfiguration
└── docs/                           # Zusätzliche Dokumentation
```

## 🔧 Technologies Used

**Programming Languages:**
Python

**Libraries & Frameworks:**
pandas, matplotlib, seaborn, numpy

**Tools:**
Jupyter, Git, GitHub, VS Code

## 📊 Data

**Source:** 
Kaggle: Credit Risk Dataset(https://www.kaggle.com/datasets/laotse/credit-risk-dataset) 

**Size:** 
32581 rows, 12 columns

**Important Features:** 
'cb_person_default_on_file' - renamed to -> 'default'
'loan_status' - target variable (0 - no default, 1 - default)
'loan_grade' - creditworthiness
'loan_amnt' - loan amount                  
'loan_int_rate' - interest rate 

## 🤖 Methodik

### Data Preprocessing
There are 2 columns with missing values:
'person_emp_length' - 895 values, ~2.75% of data. They were replaced by median.
'loan_int_rate' - 3116 values, ~9.56% of data. They were replace by medians grouped by each loan_grade.

There are 16 unrealistic values:
There are 5 cases with the person_age more than 100 years old.
There are 2 cases with the person employment length 123 years. 
There are 9 cases with the income more than 1000000.
All are deleted.

Discrepancies:
1010 values in column 'loan_int_rate' were calculated wrong. They are repaced with the correct ones. Formula used: loan_amnt/person_income

### Modeling Approach  
<!-- Welche Modelle hast du getestet? -->

### Evaluation
<!-- Wie hast du die Ergebnisse bewertet? -->

## 📈 Ergebnisse

**Model Performance:**
<!-- Deine besten Metriken (Accuracy, RMSE, etc.) -->

**Key Visualizations:**
<!-- Verweis auf Key-Plots in deinen Notebooks -->

## 🚀 Reproducibility

### Setup
```bash
# Clone Repository 
git clone [DEIN-REPO-LINK]
cd [REPO-NAME]

# Install Dependencies 
uv sync
```

### How to Run
```bash
# Run the notebooks in this order:
# 1. notebooks/01_exploration.ipynb
# 2. notebooks/02_preprocessing.ipynb  
# 3. notebooks/03_modeling.ipynb
# 4. notebooks/04_results.ipynb
```


## 🎓 About This Project

**Kontext:** 
<!-- Im Rahmen welches Kurses/welcher Veranstaltung? -->

**Time Period:** 
<!-- Wann hast du das Projekt durchgeführt? -->

**Author:** 
<!-- Dein Name -->

## 📞 Kontakt

**GitHub:** [@DeinUsername](https://github.com/DeinUsername)  
**E-Mail:** deine.email@beispiel.de  
**LinkedIn:** [Dein Profil](https://linkedin.com/in/dein-profil)

## 🙏 Acknowledgements

<!-- Hier kannst du Personen oder Ressourcen erwähnen, die dir geholfen haben -->

---

**⭐ If you like this project, feel free to give it a star!**
