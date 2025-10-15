# Credit Risk Analysis 🚀

> Predicting the probability of loan default based on borrower information.

## 📊 Project Overview

**Problem Statement:** 
Can we predict whether a borrower will be able to pay back the loan or is there a risk of default?

**Goal:** 
The goal of this project is to build a predictive model that estimates the probability of loan default.

**Methods:** 
Performed exploratory data analysis to identify key relationships and trends.  
Applied logistic regression to model the probability of loan default and interpret key risk drivers.

## 🎯 Key Findings

- 📈 **Key finding 1:** Borrowers with larger loan-to-income ratio and higher interest rates are more likely to default.
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
│   └── 03_modeling.ipynb           # Modeling
│   └── 03_results.ipynb            # Results
├── src/dpp                         # Python Module
├── test/                           # Unit Tests
├── pyproject.toml                  # Project configuration
└── docs/                           # Additional Documentation
```

## 🔧 Technologies Used

**Programming Languages:**
Python

**Libraries & Frameworks:**
pandas, matplotlib, seaborn, numpy, statsmodels

**Tools:**
Jupyter Notebook, VS Code, Git, GitHub

## 📊 Data

**Source:** 
Kaggle: https://www.kaggle.com/datasets/laotse/credit-risk-dataset

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
'person_emp_length': 895 missing (~2.75%) → replaced with the median
'loan_int_rate': 3,116 missing (~9.56%) → replaced with group medians by loan_grade

Unrealistic values:
Ages >100 and incomes >1,000,000 → removed

Discrepancies:
1,010 incorrect 'loan_int_rate' values → recalculated and corrected

### Modeling Approach  
We applied logistic regression to model the probability of loan default.  
- Tested multiivariate model ('loan_percent_income', 'loan_int_rate')  
- Fitted using statsmodels.formula.api.logit()

### Evaluation
- Model fit assessed using Pseudo R² (0.23)
- Probability curve visualized to interpret risk thresholds  

## 📈 Results

**Model Performance:**
- Logistic regression identifies high-risk borrowers effectively based on loan-to-income rato and interest rate  
- 50% risk threshold found around ~0.37 loan-to-income ratio

**Key Visualizations:**
1. Default rate by loan purpose
2. Default rate by home ownership
3. Actual vs. historical default
4. Logistic regression probability curve with 50% threshold line
5. Distribution of predicted probabilities

## 🚀 Reproducibility

### Setup
```bash
# Clone Repository 
git clone https://github.com/AlShiri/Dpp-Stackfuel-Data-Analytics.git
cd Dpp-Stackfuel-Data-Analytics

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

**Context:** 
This project was completed as part of a Data Analytics course, focusing on applying statistical modeling and data visualization to real-world business questions.

**Time Period:** 
October 2025

**Author:** 
Alla Shirinyan

## 📞 Kontakt

**GitHub:** [@AlShiri](https://github.com/AlShiri)  
**E-Mail:** allashirinyan@hotmail.com  
**LinkedIn:** [Alla Shirinyan](https://www.linkedin.com/in/alla-sh/)

## 🙏 Acknowledgements
Special thanks to StackFuel for learning platform, and guidance during the Data Analytics program.
Additional thanks to mentors and peers for feedback and discussions that helped shape this project.
Thanks to the Kaggle community for making open datasets available for educational and analytical purposes.

---

**⭐ If you like this project, feel free to give it a star!**
