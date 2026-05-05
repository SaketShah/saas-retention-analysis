# SaaS Customer Retention & Unit Economics Analysis

## Project Overview
This project provides a comprehensive data analysis of SaaS customer behavior, focusing on unit economics, churn indicators, and product engagement. Utilizing Power BI and advanced DAX calculations, the analysis identifies critical inflection points in user adoption and quantifies actionable revenue risks. The primary objective is to transition from descriptive financial reporting to predictive, behavioral modeling to safeguard Monthly Recurring Revenue (MRR).

## Data Source
The dataset used for this analysis was sourced from [Analyst Builder](https://www.analystbuilder.com/projects/saas-revenue-churn-analysis-UPoYs). It contains synthetic SaaS subscription records, including monthly revenue, churn status, customer demographics, and product engagement telemetry.

## Executive Summary
The analysis reveals a highly efficient acquisition model offset by a substantial historical churn rate of 52.17%. By segmenting user behavior, the data identifies a strict feature-adoption threshold that dictates customer retention. Currently, 132 active accounts have been flagged as high-risk. Implementing targeted product adoption strategies based on these findings presents an immediate opportunity to protect highly valuable enterprise and business contracts.

## Key Financial Metrics & Unit Economics
The fundamental financial engine demonstrates exceptional market efficiency:
*   **Customer Lifetime Value (CLV):** $22.4K
*   **Customer Acquisition Cost (CAC):** ~$200 
*   **LTV:CAC Ratio:** 111.75x
*   **Total Active Customer Base:** 600
*   **MRR Trend:** Consistent, compounding positive growth over a two-year tracking period.

> **Strategic Insight:** The LTV:CAC ratio of 111.75 indicates highly efficient Go-To-Market (GTM) motions, generating over $22,000 in lifetime value for every dollar spent on acquisition.

## Methodology & Technical Implementation
This project was developed utilizing Power BI for data modeling, visualization, and metric calculation. Key technical methodologies include:

*   **Metric Normalization:** Standardized timeframe alignments to ensure accurate CLV calculations (converting all-time aggregate churn to monthly churn metrics against Average Monthly Revenue).
*   **Data Discretization (Binning):** Segmented continuous percentage data (Feature Usage) into decile bins to identify behavioral thresholds and non-linear churn trends.
*   **Categorical Logic (DAX):** Implemented nested `SWITCH(TRUE())` statements to dynamically categorize the active user base into "Low," "Moderate," and "High" risk tiers based on historical feature adoption data.
*   **Cohort Filtering:** Utilized `CALCULATE` and `DISTINCTCOUNT` functions to isolate active, at-risk users, actively removing historical/churned accounts from the risk pool.

## Key Findings & Behavioral Insights

### 1. The "50% Adoption Cliff"
A decile analysis of feature usage against aggregate churn rates revealed a critical operational threshold:
*   **High-Risk Zone (< 50% Usage):** Cohorts utilizing less than 50% of the platform’s features exhibit severe churn rates ranging from 56.67% to 87.85%.
*   **Retention Zone (>= 50% Usage):** Upon crossing the 50% adoption threshold, churn probability immediately plummets to 13.51%.

### 2. NPS Correlation & Quadrant Analysis
A scatter plot analysis correlating Net Promoter Score (NPS) with Feature Usage Percentage validated the adoption cliff:
*   **Detractors (Flight Risk):** Heavy concentration of users with low NPS (< 6) strictly correlates with the < 50% feature usage cohort. 
*   **Promoters (Champions):** High NPS scores strongly correlate with > 50% feature usage, indicating that product complexity is not a barrier to satisfaction, provided the user is properly onboarded.

### 3. Demographic Vulnerabilities
*   **Billing Cycles:** 68.05% of all historical churn is concentrated within Monthly billing cycles.
*   **Plan Tiers:** The "Starter" and "Enterprise" tiers represent the highest volume of churn (48.88% combined), suggesting value-alignment discrepancies at the absolute high and low ends of the pricing model.

## Strategic Recommendations
1.  **Trigger-Based Customer Success:** Deploy automated interventions and targeted onboarding refreshers for the 132 active accounts currently sitting below the 50% feature adoption threshold.
2.  **Contract Restructuring:** Partner with Sales/Marketing to aggressively incentivize Annual billing cycles, increasing the customer runway necessary to cross the 50% adoption threshold.
3.  **Qualitative Intervention for "Hostages":** Isolate the specific quadrant of users displaying High Feature Usage alongside Low NPS. This cohort requires immediate qualitative feedback sessions to identify UI/UX friction points.

