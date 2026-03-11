# Credit-Risk-Portfolio-Analysis-
Hands-on Credit Risk Analysis project using Python and SQL with real-world datasets from Kaggle.
credit-risk-eda/
│
├── README.md
├── credit_risk_analysis.ipynb
├── images/
# Credit Risk Portfolio Analysis (EDA)
📌 Project Overview

This project explores key drivers of loan default risk using Exploratory Data Analysis (EDA) techniques.

The objective was to:

Identify the primary factors influencing loan default and determine which borrower segments contribute most to overall portfolio risk — without building a machine learning model.

This analysis focuses on affordability, exposure, risk segmentation, and business-driven insights.

# Business Problem

Loan defaults significantly impact financial institutions through increased credit losses.

The goal of this analysis was to:

Understand borrower characteristics associated with default

Evaluate the effectiveness of the internal loan grading system

Identify which portfolio segments drive the most risk

Provide actionable business recommendations

# Dataset Source

This project uses the Credit Risk dataset obtained from Kaggle.

Dataset Name: Credit Risk

Source: Kaggle

Link: https://www.kaggle.com/datasets/laotse/credit-risk-dataset

The dataset includes borrower-level demographic, financial, and loan-related variables.

⚠ Note: The raw dataset is not included in this repository. Please download it directly from Kaggle using the link above.

# Tools & Technologies

Python

Pandas

NumPy

Matplotlib / Seaborn

Jupyter Notebook

# Key Variables Analyzed

person_income

loan_amnt

loan_percent_income

loan_int_rate

loan_grade

cb_person_cred_hist_length

loan_status (0 = Non-default, 1 = Default)

# Key Findings
1️⃣ Loan-to-Income Ratio Is the Strongest Risk Driver
Loan Status	Avg Loan % of Income
Non-default	~14.9%
Default	~24.7%

Borrowers who default allocate significantly more of their income toward loan repayment.

# Insight:
Repayment burden (affordability) is the most powerful driver of default risk.

2️⃣ Loan Amount Has Moderate Impact
Loan Status	Avg Loan Amount
Non-default	~9,237
Default	~10,850

Defaulters borrow larger amounts on average, but loan size alone is less predictive than affordability.

3️⃣ Risk-Based Pricing Is Evident
Loan Status	Avg Interest Rate
Non-default	~10.49%
Default	~12.87%

Higher-risk borrowers are charged higher interest rates.

This suggests risk-based pricing is applied, though higher rates may increase repayment pressure.

4️⃣ Credit History Length Shows Weak Predictive Power
Loan Status	Avg Credit History Length
Non-default	~5.84 years
Default	~5.69 years

Minimal difference observed.

# Insight:
Repayment capacity is more influential than length of credit history in this dataset.

5️⃣ Loan Grade Effectiveness

Default rate increases consistently from Grade A to Grade G:

Grade	Default Rate
A	~10%
B	~16%
C	~21%
D	~59%
E	~64%
F	~70%
G	~98%

# Insight:
The loan grading system demonstrates strong discriminatory power.

# Portfolio Risk Contribution

Although extreme-risk grades (F & G) show very high default rates, they represent a very small portion of the portfolio.

The largest contributor to overall portfolio risk is:

Grade D

~11% of portfolio

~59% default rate

This segment combines significant exposure with high default probability, making it the primary loss driver.

# Business Recommendations

1️⃣ Implement Loan-to-Income Threshold Controls
Introduce stricter approval criteria for borrowers exceeding affordability thresholds (e.g., >20%).

2️⃣ Reassess Grade D Underwriting Standards
Tighten eligibility requirements and reduce exposure within this segment.

3️⃣ Balance Risk-Based Pricing with Affordability
Ensure interest rates do not increase repayment strain beyond sustainable levels.

4️⃣ Include Loan Tenure in Future Analysis
Loan duration data would improve installment-level affordability assessment.

# Limitations

Loan repayment duration was not available.

No macroeconomic or behavioral repayment variables were included.

This analysis focuses on EDA and does not include predictive modeling.


