
# 💳 Credit Risk Analysis with R

This project involves a comprehensive analysis of credit risk using the German Credit Dataset. The goal is to investigate the relationship between different financial and demographic factors and the creditworthiness of individuals using statistical tests and machine learning models in R.

---

## 📁 Dataset Overview

- **Dataset:** german_credit_data.csv
- **Rows:** 1000
- **Columns:** 11
- **Target Variable:** `Risk` (good/bad credit)

---

## 📌 Key Questions Answered

### 1. **Does Employment Status (Job) Impact Credit Risk?**
- A Chi-square test was conducted.
- **Result:** No significant association (p = 0.5966).

### 2. **Does Housing Type Affect Credit Risk?**
- Housing types analyzed: own, rent, free.
- **Chi-square result:** Significant relationship (p = 0.0001).
- Individuals with “own” housing were more likely to have good credit.

### 3. **Do Savings and Checking Accounts Correlate with Credit Risk?**
- Both showed significant association via Chi-square tests.
- Individuals with little or missing account information had a higher risk.

### 4. **Does the Credit Amount Requested Affect Credit Risk?**
- **Wilcoxon rank-sum test:** Significant difference in credit amount across risk groups (p = 0.0059).
- **Logistic Regression:** Showed a slight impact but not statistically significant.

---

## 🔬 Statistical & Machine Learning Methods

- **Chi-square Tests** for independence
- **Wilcoxon Rank-Sum Test** for credit amount
- **Logistic Regression** using `glm()`
- **Multinomial Logistic Regression** using `vglm()` from VGAM package

---

## 📈 Key Model Insights

- **Significant Predictors:** Age, Duration, Checking & Saving Account types
- **Non-significant Predictors:** Credit Amount, Job, Housing, Purpose
- **Model Fit:**
  - Residual Deviance: 1013.43
  - Log-Likelihood: -506.71
- **Significant Variables (p < 0.05):**
  - Age (+)
  - Duration (+)
  - Checking.account ("little", "Not Available")
  - Saving.accounts ("little")

---

## 🧪 Libraries Used

- `dplyr`
- `ggplot2`
- `caret`
- `pROC`
- `VGAM`
- `glmnet`

---

## 📉 Visualizations

- Bar charts for Job, Housing, Saving, and Checking account distributions by Risk
- Logistic regression plots for probability estimation
- Contingency tables with corresponding p-values

---

## 📦 File Structure

```
├── german_credit_data.csv
├── final-project.docx
├── README.md
└── R analysis scripts
```

---

## ✅ Conclusion

This project revealed key relationships between account information and creditworthiness, showing strong evidence for using such variables in risk modeling. While some variables like job and credit amount had limited predictive power, others like account types and duration stood out. This lays a solid foundation for further predictive modeling using classification algorithms.

---

## ⚠️ Disclaimer

This analysis is for educational purposes only. Do not use it to make real financial decisions.
