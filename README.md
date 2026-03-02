# 📊 Cross-Channel Marketing Optimization (Facebook vs AdWords)

## 🧠 Project Overview

This project is about comparing two advertising platforms — Facebook Ads and Google AdWords — to understand which one performs better in terms of conversions and cost efficiency.

As a marketing agency, the goal is to figure out where to spend money so that we get more conversions with less cost. Instead of just looking at totals, this project uses proper data analysis and statistics to make better decisions.

---

## 🎯 Problem Statement

Both Facebook and AdWords are generating clicks and conversions, but it is not very clear which platform is actually better in a consistent and cost effective way.

Simple comparison is not enough because performance changes daily and there can be hidden patterns in the data.

So the aim of this project is to:

* Compare conversion performance
* Understand cost efficiency
* Identify patterns and variations
* Make data-driven recommendations

---

## 📁 Dataset

The dataset contains daily campaign data for 1 year (2019), including:

* Ad Views
* Clicks
* Conversions
* Cost
* CTR, Conversion Rate, CPC

---

## 🔍 Approach

### 1. Data Cleaning

* Converted date columns
* Cleaned percentage and currency values
* Handled division errors

---

### 2. Feature Engineering

* Calculated Conversion Rate (CR)
* Calculated Cost Per Acquisition (CPA)
* Created time-based features

---

### 3. Exploratory Data Analysis

The analysis was done using multiple angles:

* **Trend:** Checked how conversions change over time
* **Segmentation:** Grouped days into low, medium, high performance
* **Deviation:** Identified outliers and variability
* **Distribution:** Checked how data is spread
* **Pareto:** Found top contributing days
* **Comparison:** Compared Facebook vs AdWords across all metrics

---

### 4. Statistical Testing

* Checked normality using Shapiro-Wilk test
* Since normality was violated, used **Mann-Whitney U test**

📌 Result:
There is a statistically significant difference between the two platforms

---

### 5. A/B Testing with Confidence Intervals

Instead of only relying on p-values, confidence intervals were used to measure real impact.

#### Conversion Rate (CR)

* Difference: **+0.1697**
* 95% CI: [0.1644, 0.1750]

👉 Facebook has clearly higher conversion rate

#### Cost Per Acquisition (CPA)

* Difference: **-16.64**
* 95% CI: [-17.76, -15.53]

👉 Facebook is cheaper per conversion

---

## 💡 Key Insights

* Facebook performs better in both:

  * Conversion efficiency (higher CR)
  * Cost efficiency (lower CPA)

* The difference is not only statistically significant but also practically meaningful

* A small portion of days contributes to most conversions (Pareto effect)

---

## 🤖 Predictive Modeling

A Linear Regression model was built to predict conversions based on clicks.

* R² Score: ~0.77
* Model captures strong relationship between clicks and conversions

### Business Use:

We can reverse the model to estimate:
👉 How many clicks are needed to achieve a target number of conversions

---

## ⚠️ Model Limitations

* Assumes linear relationship between clicks and conversions

* Does not include external factors like:

  * Audience quality
  * Ad creatives
  * Budget changes

* Residual analysis shows slight non-linearity and non-normality

So results should be used as **directional insights**, not exact predictions

---

## 📈 Strategic Recommendations

1. **Reallocate Budget**
   Shift 15–20% of budget to Facebook since it has lower CPA

2. **Funnel Optimization**
   Identify drop-offs between:

   * Views → Clicks
   * Clicks → Conversions

3. **Campaign Planning**
   Use predictive model to estimate required clicks for future targets

---

## 🚀 Conclusion

From this analysis, Facebook clearly outperforms AdWords in both performance and cost efficiency.

However, since this is based on observational data, results should be treated as strong directional insights and not absolute truth.

---

## 🛠️ Tools Used

* Python (Pandas, NumPy)
* Matplotlib, Seaborn
* SciPy (Statistical Testing)
* Scikit-learn (Modeling)

---

## 🙋‍♂️ Final Note

This project helped me understand how to go beyond basic analysis and actually connect data with real business decisions. Some parts may not be perfect but the goal was to learn and improve step by step.

---
