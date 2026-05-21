# 📊 Loan-Default-Risk-Analysis

## Executive Summary

Horizon Financial Group identified that approximately 24% of issued personal loans were defaulting, significantly exceeding the organization’s target default rate of 12%. The objective of this project was to analyze borrower demographics, financial characteristics, and loan application data to identify the primary drivers of loan default risk and provide data-driven underwriting recommendations.

Using SQL and Power BI, borrower and loan datasets were analyzed to evaluate relationships between default behavior and key risk indicators including credit score, debt-to-income ratio (DTI), employment stability, loan purpose, and interest rate. The analysis found that borrowers with lower credit scores, higher DTI ratios, and limited employment history demonstrated substantially higher default risk. Certain loan categories, including debt consolidation and medical loans, also showed elevated default rates.

The final deliverable includes an interactive Power BI dashboard that visualizes portfolio risk metrics and borrower segmentation trends. Recommendations were developed to support underwriting policy improvements and reduce future default exposure.

---

# Business Problem

Horizon Financial Group experienced loan default rates nearly double the company’s target threshold. The Risk Management division requested a comprehensive analysis of borrower and loan data to determine:

- Which borrower characteristics contribute most strongly to default risk
- Whether existing underwriting standards are too lenient
- Which loan categories represent elevated financial risk
- What approval thresholds should be implemented to reduce losses

The analysis was designed to support:
- underwriting policy adjustments
- risk segmentation
- credit approval optimization
- portfolio risk reduction

---

# Business Objectives

The primary business objectives of this project were to:

1. Measure and quantify the current portfolio default rate
2. Identify the strongest predictors of loan default
3. Segment borrowers into risk categories
4. Evaluate whether underwriting thresholds should be adjusted
5. Create an executive dashboard for ongoing monitoring

---

# Methodology

## 1. Data Collection & Import

Two datasets were used:

### Borrower Dataset
Contained borrower demographic and financial information:
- age
- annual income
- employment status
- years employed
- credit score
- home ownership
- monthly debt obligations

### Loan Application Dataset
Contained loan-level information:
- loan amount
- loan purpose
- interest rate
- monthly payment
- debt-to-income ratio
- delinquency history
- default status

The datasets were imported into SQL Server Management Studio (SSMS) for analysis.

---

## 2. Data Preparation

The following preparation steps were completed:

- imported CSV files into SQL Server
- validated data types
- checked for null values
- reviewed data consistency
- joined borrower and loan tables using borrower_id

SQL joins were used to combine borrower-level and loan-level information into a single analytical dataset.

---

## 3. Exploratory Data Analysis (EDA)

Exploratory analysis was conducted to:
- understand portfolio composition
- calculate overall default rate
- identify outliers and trends
- compare borrower segments

The following analyses were performed:
- credit score segmentation
- DTI segmentation
- employment stability analysis
- loan purpose comparison
- average loan amount comparison
- delinquency trend analysis

---

## 4. Risk Segmentation Analysis

Borrowers were grouped into categories to identify high-risk segments.

### Credit Score Buckets
- 520–599
- 600–649
- 650–699
- 700–749
- 750+

### DTI Buckets
- Under 20%
- 20–35%
- 36–50%
- Over 50%

### Employment Length Buckets
- Less than 2 years
- 2–5 years
- 5+ years

Default rates were calculated for each segment.

---

## 5. Dashboard Development

Power BI was used to create an interactive executive dashboard containing:
- KPI cards
- risk segmentation charts
- scatter plots
- loan purpose comparisons
- underwriting recommendation summaries

The dashboard was designed to support executive decision-making and underwriting strategy discussions.

---

# Tools & Technologies Used

| Tool | Purpose |
|---|---|
| SQL Server / SSMS | Data cleaning and analysis |
| SQL | Aggregation, joins, segmentation |
| Power BI | Dashboard and visualizations |
| Excel | Data validation and CSV management |

---

# Dashboard Features

The dashboard includes:

## KPI Cards
- Overall Default Rate
- Average Debt-to-Income Ratio
- Average Interest Rate
- Total Loans Issued

## Visualizations
- Default Rate by Credit Score Range
- DTI vs Default Risk Scatter Plot
- Default Rate by Loan Purpose
- Employment Status Risk Analysis
- Years Employed Risk Comparison

## Interactive Filters
- State
- Loan Purpose
- Employment Status
- Credit Score Range

---

# Key Findings

## 1. Credit Score Was the Strongest Predictor of Default

Borrowers with credit scores below 650 showed significantly higher default rates compared to higher-score borrowers.

Observed trends:
- lower credit scores corresponded with higher delinquency and default behavior
- borrowers above 700 showed substantially lower default risk

### Business Implication
The existing underwriting process may be approving borrowers with excessive credit risk exposure.

---

## 2. High Debt-to-Income Ratios Increased Default Risk

Borrowers with DTI ratios above 35% demonstrated noticeably elevated default rates.

The scatter plot analysis showed:
- default concentrations increased sharply between 35–50% DTI
- borrowers with lower DTI values defaulted less frequently

### Business Implication
Borrowers with excessive debt obligations may lack sufficient repayment capacity.

---

## 3. Employment Stability Influenced Repayment Behavior

Borrowers employed for less than 2 years exhibited higher default rates than borrowers with longer employment histories.

Additional findings:
- unemployed and part-time borrowers showed elevated risk
- stable employment correlated with lower default frequency

### Business Implication
Employment stability is an important indicator of repayment reliability.

---

## 4. Certain Loan Purposes Were Higher Risk

Debt consolidation and medical loans displayed higher default rates than other loan categories.

Possible explanations:
- financially distressed borrowers seeking consolidation
- emergency borrowing behavior
- unstable repayment conditions

### Business Implication
Certain loan categories may require enhanced underwriting scrutiny.

---

# Results & Business Recommendations

Based on the analysis, the following underwriting recommendations are proposed:

---

## Recommendation 1 — Implement Minimum Credit Score Threshold

### Proposed Policy
Minimum credit score:
- 650 for standard loan approvals

### Rationale
Borrowers below 650 demonstrated significantly higher default rates.

### Expected Impact
- reduction in portfolio default exposure
- improved portfolio credit quality
- lower delinquency rates

---

## Recommendation 2 — Establish Maximum DTI Threshold

### Proposed Policy
Maximum DTI ratio:
- 35%

### Rationale
Default concentrations increased sharply above the 35% threshold.

### Expected Impact
- improved borrower repayment capacity
- reduced overleveraged borrower approvals
- lower financial stress exposure

---

## Recommendation 3 — Enhance Verification for Limited Employment History

### Proposed Policy
Additional underwriting review for borrowers employed less than 2 years.

### Rationale
Limited employment tenure correlated with elevated repayment risk.

### Expected Impact
- improved income stability validation
- reduced early-stage defaults
- stronger borrower quality assessment

---

## Recommendation 4 — Apply Stricter Review for High-Risk Loan Purposes

### Proposed Policy
Enhanced underwriting procedures for:
- debt consolidation loans
- medical loans

### Rationale
These categories demonstrated above-average default rates.

### Expected Impact
- reduced exposure to distressed borrowers
- improved loan portfolio stability

---

# Business Impact

If implemented, the proposed underwriting adjustments could help Horizon Financial Group:

- reduce default rates toward target thresholds
- improve portfolio profitability
- reduce delinquency management costs
- strengthen credit approval quality
- improve long-term lending stability

Potential operational benefits include:
- lower charge-off rates
- improved risk-adjusted returns
- enhanced portfolio monitoring capabilities

---

# Next Steps

Future enhancements to this project may include:

## Predictive Modeling
Develop machine learning models to predict loan default probability using:
- logistic regression
- random forest
- gradient boosting

## Time-Series Monitoring
Track:
- monthly default trends
- delinquency progression
- economic sensitivity

## Geographic Risk Analysis
Evaluate:
- state-level risk concentrations
- regional economic impacts
- localized default behavior

## Automated Risk Scoring
Build a borrower risk scoring model for:
- automated underwriting
- approval recommendations
- risk tier assignment

---

# Limitations

Several limitations should be considered:

## Synthetic Dataset
The dataset used was simulated and may not fully represent real-world borrower behavior.

## Limited Historical Time Range
The analysis covered a relatively short lending period and may not capture long-term economic cycles.

## External Economic Factors Not Included
Variables such as:
- inflation
- unemployment rates
- macroeconomic conditions
were not included.

## Simplified Default Definition
The project used a binary default flag and did not model:
- severity of delinquency
- partial repayments
- recovery rates

---

# Project Files

| File | Description |
|---|---|
| credit_risk_analysis.sql | SQL queries used for analysis |
| credit_risk_dashboard.pbix | Power BI dashboard |
| borrower_profiles.csv | Borrower demographic dataset |
| loan_applications.csv | Loan application dataset |

---

# Dashboard Preview

![Dashboard Screenshot](images/dashboard_screenshot.png)
<img width="558" height="322" alt="image" src="https://github.com/user-attachments/assets/3146ed80-21db-4d11-aa20-3a3f3e8c8e64" />

---

# Skills Demonstrated

- SQL querying
- Data cleaning and preparation
- Risk segmentation analysis
- Financial analytics
- Dashboard development
- Data storytelling
- Business recommendations
- Underwriting analysis
- KPI reporting

---

# Author

Brianna Leonte
