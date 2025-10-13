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

- 📈 **Key finding 1:** Borrowers with higher interest rates and larger loan-to-income ratios are more likely to default.
- 🔍 **Key finding 2:** Past default history strongly predicts future defaults, with repeat defaulters about twice as likely to default again.
- 💡 **Key finding 3:** Borrower profile—including lower loan grades, certain loan purposes (debt consolidation, medical, home improvement), and renting versus owning—also influences risk, highlighting how both creditworthiness and personal circumstances affect default likelihood.

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
│   └── 02_preprocessing.ipynb      # Data Cleaning
│   └── 03_modeling.ipynb           # EDA
├── src/dpp                         # Python Module
├── test/                           # Unit Tests
├── pyproject.toml                  # Projektkonfiguration
└── docs/                           # Zusätzliche Dokumentation
```

## 🔧 Technologies Used

**Programming Languages:**
Python

**Libraries & Frameworks:**
pandas, matplotlib, seaborn, numpy, statsmodels

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
'loan_int_rate' - loan interest rate 
'loan_percent_income' - loan to income ration

## 🤖 Methodik

### Data Preprocessing
Missing values:
person_emp_length: 895 missing (~2.75%) → replaced with the median
loan_int_rate: 3,116 missing (~9.56%) → replaced with group medians by loan_grade

Unrealistic values:
Unrealistic ages (>100) and extremely high incomes (>1,000,000) → removed

Discrepancies:
1,010 incorrect values in loan_int_rate → recalculated and corrected

### Modeling Approach  
We applied logistic regression to model the probability of loan default.  
- Tested univariate models ('loan_percent_income', 'loan_int_rate')  
- Fitted using statsmodels.formula.api.logit()

### Evaluation
- Model fit assessed using Pseudo R² (0.13 for main model), coefficient significance, and visual inspection of probability curves.  

## 📈 Results

**Model Performance:**
- Logistic regression successfully identifies borrowers at high risk based on key features.  
- Probability curves allow identification of the 50% risk threshold

**Key Visualizations:**
1. Logistic regression probability curve with 50% threshold line.
2.

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
