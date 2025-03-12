## 📌 Impact of Insurance Type on Hospital Stay: A Propensity Score Approach

### Project Overview
This project examines the relationship between insurance type and hospital length of stay among surgical patients. Using NHANES inpatient data, we apply propensity score methods (logistic regression & random forest) to adjust for confounders and assess healthcare disparities.

### Data Sources
NHANES Hospital Inpatient Discharges (SPARCS De-Identified Data) – 2015
Variables: Length of Stay, Insurance Type, Age, Illness Severity, Admission Type, Mortality Risk, and Medical-Surgical Classification

### Methodology
🔹 Data Preprocessing & Cleaning
- Converted categorical variables to factors
- Handled missing data via imputation

🔹 Propensity Score Estimation
- Multinomial Logistic Regression Model
- Random Forest Model (ranger package)

🔹 Final Analysis
- Weighted Regression Model to assess the impact of insurance type on hospital stay

### Installation & Dependencies
To reproduce the analysis, install the following R packages:

```

 install.packages(c("tidyverse", "MatchIt", "randomForest", "caret", 
                   "VIM", "dplyr", "nnet", "ranger", "progress", "glmnet"))

```
### Running the Code
To execute the analysis, run:

```
# Load dataset & clean
source("data_preprocessing.R")
```
```
# Estimate propensity scores
source("propensity_score.R")
```
```
# Run final regression model
source("final_analysis.R")
```
### Results & Insights
📊 Findings:
- The type of insurance coverage is significantly associated with hospital length of stay
- Patients with public insurance tend to have longer stays than those with private insurance
- Medical condition severity and admission type also play key roles

📢 Future Work:
- Extend analysis with more recent inpatient datasets
- Explore causal inference methods beyond propensity score matching








