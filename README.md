# Bank Customer Churn Analysis | Root Cause & Statistical Testing

---

## Overview

This project focuses on analyzing bank customer churn data to answer a critical business question: **Why did 20% of customers leave the bank?**

Using statistical analysis techniques, correlation evaluations, and hypothesis testing in Excel, this project isolates the primary root cause behind customer attrition.

---

## Analytical Workflow & Statistical Testing

### 1. Correlation Analysis
Initial correlation matrix was generated between customer churn (`Exited`) and multiple variables (`Age`, `Tenure`, `Balance`, `HasCrCard`, `EstimatedSalary`, `IsActiveMember`):
* **Finding:** `Age` showed the highest positive correlation coefficient with customer exit compared to all other variables.
* **Hypothesis:** Customer churn is primarily driven by advancing age.

### 2. Hypothesis Testing (t-Test)
To confirm whether the age difference between churned (`Exited`) and retained (`Stayed`) customers was statistically significant or merely due to random chance:
* **Test Applied:** Two-Sample t-Test assuming unequal variances.
* **Result:** The resulting p-value was significantly lower than the standard threshold ($p < 0.05$), proving that age is a statistically significant factor in customer departure.

### 3. Root Cause Investigation (Why older customers leave?)
Further correlation analysis was conducted to uncover the underlying mechanism:
* **Finding:** A strong negative correlation (**-0.90**) was identified between `Age` and `IsActiveMember`.
* **Conclusion:** As customer age increases, their activity and engagement with bank services drastically decrease.

### 4. Validation via Pivot Tables
Cross-tabulation using Excel Pivot Tables confirmed the statistical model: customer churn is directly tied to reduced activity and engagement among older demographics.

![Bank Churn Statistical Analysis Excel](projext.jpg)

---

## Key Takeaway & Business Finding

Customers leave the bank primarily due to **advancing age combined with low platform activity/engagement**, pointing toward a need for tailored engagement programs and targeted financial services for older customer segments.

---

## Tools Used

* **Microsoft Excel:** Data Analysis ToolPak, Pivot Tables, Statistical Functions
* **Statistical Methods:** Correlation Matrix, Two-Sample t-Test, Hypothesis Testing
