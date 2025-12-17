# 🧪 A/B Testing Analysis: Landing Page Conversion Rate

## Project Overview

This project analyzes the results of a high-stakes A/B test conducted on an e-commerce platform. The goal was to determine if a **new landing page design** (`Treatment`) achieved a **statistically significant** change in the conversion rate compared to the existing page (`Control`).

The analysis used Python for data cleaning and **Two-Sample Z-Test** and **Confidence Interval estimation** for statistical rigor, leading to a definitive "Do Not Launch" recommendation.

## 🎯 Executive Summary & Recommendation

**Recommendation:** Do NOT launch the new landing page (Treatment).

### Key Finding
The Treatment Group (New Page) achieved a conversion rate of **$11.88\%$**, which was numerically *worse* than the Control Group's **$12.04\%$**. Crucially, the statistical analysis yielded a **P-value of $0.1892$**.

### Conclusion
Since the P-value ($0.1892$) is much greater than the standard significance level ($\alpha = 0.05$), we **Fail to Reject the Null Hypothesis ($H_0$)**. We cannot conclude that the New Page is genuinely different from the Old Page. The observed difference is likely due to random chance, not the design itself. Launching the new page would cost resources without a proven benefit.

---

## Methodology and Technical Workflow

### 1. Hypothesis Definition (Two-Tailed Test)

* **Null Hypothesis ($H_0$):** There is no difference in conversion rates. $H_0: p_{new} - p_{old} = 0$
* **Alternative Hypothesis ($H_A$):** There is a statistically significant difference. $H_A: p_{new} - p_{old} \neq 0$

### 2. Statistical Results Summary

| Group | Total Users | Conversion Rate (CR) | 95% CI Range |
| :--- | :--- | :--- | :--- |
| **Control (Old Page)** | 145,274 | **$12.04\%$** | $[11.87\%, 12.21\%]$ |
| **Treatment (New Page)** | 145,313 | **$11.88\%$** | $[11.71\%, 12.05\%]$ |
| **P-value** | \- | \- | **$0.1892$** |

### 3. Confidence Interval Visualization

The visualization below confirms that the $95\%$ Confidence Intervals for both groups overlap significantly. This visual proof reinforces the P-value finding: the true conversion rates of the new and old pages are likely within the same range, and thus, the new page does not offer a reliable lift.

![A/B Test Confidence Interval Plot](ab_test_confidence_intervals.png)

---

### **View the Full Analysis**

The complete Python code, data cleaning steps, statistical calculations, and raw data outputs are available in the linked Jupyter Notebook:

➡️ **[ab\_test\_analysis.ipynb](ab_test_analysis.ipynb)**
