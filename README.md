# 📊 A/B Testing Analysis for an Ad-Tech Company

## 📘 Project Overview
This project performs a complete A/B test analysis on a dataset from an ad-tech company using both **frequentist and Bayesian statistical methods**, along with **ROI impact, revenue per click, and uplift analysis**. The goal is to evaluate the effectiveness of a test advertising campaign compared to a control.

---

## 📊 Dataset Description
**Source:** [Kaggle - A/B Testing Analysis for an Ad-Tech Company](https://www.kaggle.com/code/marta99/a-b-testing-analysis-for-an-ad-tech-company)

### Data Files:
- `control_group.csv`
- `test_group.csv`

### Columns:
- `Date`: Campaign run date
- `Spend [USD]`: Daily spend in USD
- `# of Website Clicks`: Number of clicks from the ad to the website
- `# of Purchase`: Number of purchases made from those clicks

### Derived Metrics:
- **Conversion Rate** = `# of Purchase / # of Website Clicks`
- **ROI** = `Total Revenue / Total Spend`
- **Revenue per Click** = `Total Revenue / Website Clicks`
- **Total Revenue** (assumed `$50` per purchase)
---

### 📐 Key Formulas

**Conversion Rate**  
`Conversion Rate = Number of Purchases / Website Clicks`

**Revenue Per Click**  
`Revenue per Click = Total Revenue / Website Clicks`

**ROI (Return on Investment)**  
`ROI = Total Revenue / Total Spend`

**Uplift (%)**  
`Uplift (%) = (Test - Control) / Control * 100`

---

## ⚙️ Methods Used
- Data Cleaning & Aggregation
- Frequentist Hypothesis Testing (Z-test for proportions)
- Bayesian Modeling with PyMC
- Posterior Visualizations
- ROI & Business Impact Metrics
- Uplift Calculations

---

## 🧪 Frequentist Results
- **Z-Statistic**: `11.84`
- **P-Value**: `< 0.0001`

**Interpretation:**  
The difference in conversion rates between control and test is statistically significant. The control group outperforms the test group.

---

## 🧠 Bayesian Results

### Posterior Mean Estimates:
- `p_control` ≈ **9.8%**
- `p_test` ≈ **8.6%**
- `Δ (test - control)` ≈ **−1.2%**

> ✅ The 95% HDI for delta is entirely **below 0**, indicating high confidence that the **control campaign is better**.


### 📈 Posterior Distributions of Conversion Rates

This visualization shows the posterior distributions of:
- **Control group conversion rate**
- **Test group conversion rate**
- **Delta (Test − Control)**

> The delta posterior is centered below 0, indicating that the control group performs better with high confidence.

![1](https://github.com/user-attachments/assets/ba043ab6-cdc6-44bb-900c-bf752ad80a85)


---

## 💰 Business Metrics Summary

| Group   | Total Clicks | Total Purchases | Conversion Rate | Total Revenue | Total Spend | ROI    | Revenue/Click |
|---------|---------------|------------------|------------------|----------------|--------------|--------|----------------|
| Control | 154,303       | 15,161           | **9.83%**         | $758,050       | $66,818      | **11.34x** | $4.91          |
| Test    | 180,970       | 15,637           | **8.64%**         | $781,850       | $76,892      | **10.17x** | $4.32          |

---

## 📉 Uplift Analysis (Test vs Control)

| Metric                | Uplift (%)   |
|-----------------------|--------------|
| Conversion Rate       | **−12.06%**  |
| Revenue per Click     | **−12.06%**  |
| ROI                   | **−10.37%**  |

> 💡 Despite slightly more total purchases, the **test campaign had worse ROI, lower efficiency, and reduced overall impact** compared to control.

### 💰 Revenue per Click Comparison

Control group generated more revenue per click than the test group.

![2](https://github.com/user-attachments/assets/2c226ab5-6c4b-4fce-8bed-c1bd8b0e6c98)


### 📉 ROI Uplift (Test vs Control)

The test group resulted in a **−10.37% ROI uplift**, meaning it underperformed compared to the control.


![3](https://github.com/user-attachments/assets/f9dc4c66-3f95-4319-945a-12ffb3404565)

---

## ✅ Conclusion

Both statistical and business metrics clearly show that the **control group performs better** than the test group.  
The test campaign results in **lower ROI, conversion rate, and revenue per click**.



