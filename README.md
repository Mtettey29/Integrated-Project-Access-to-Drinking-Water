# 🌍 Global Water Access Analysis (2000-2020)

## 📌 Project Overview
This project analyzes global trends in access to basic drinking water services over a two-decade period (2000-2020). Using a dataset of over 150 countries, the analysis investigates the disparities between **rural** and **urban** populations, identifies regional growth patterns, and uses statistical methods to understand the key drivers of national progress.

The entire project—from data cleaning to complex statistical modeling—was executed using **Google Sheets**, demonstrating the power of spreadsheet tools for end-to-end data analysis.

## 📂 The Data
The analysis is based on the **Estimates on the Use of Water (2000-2020)** dataset, which includes key indicators:
* **Populations:** National (`pop_n`), Rural (`pop_r`), and Urban (`pop_u`) population counts.
* **Water Access Levels:** Percentage of population with Basic (`wat_bas`), Limited (`wat_lim`), Unimproved (`wat_unimp`), and Surface (`wat_sur`) water access.
* **Income Groups:** Economic classification of each country (Low, Lower-Middle, Upper-Middle, High).
* **Annual Rates of Change (ARC):** Calculated metrics representing the speed of improvement year-over-year.

## 🛠️ Tools & Technologies
**Primary Tool: Google Sheets / Microsoft Excel**
* **Data Cleaning:** Used filter views, conditional formatting to spot outliers, and text functions to standardize country names.
* **Analysis:** Pivot Tables for regional aggregation, and statistical formulas (`AVERAGE`, `STDEV`, `CORREL`, `T.TEST`) for hypothesis testing.
* **Visualization:** Built dynamic Scatter Plots, Histograms, and Line Charts directly within the spreadsheet.
* **Modeling:** Utilized the "Trendline" feature and `SLOPE` / `INTERCEPT` functions for linear regression analysis.

## 🔍 Key Analysis & Methodology

### 1. Data Cleaning & Preparation
* **Handling Missing Data:** Identified gaps in rural/urban datasets using filters and marked them for exclusion in specific calculations.
* **Feature Engineering:** Calculated the **Annual Rate of Change (ARC)** using formulas to measure the *speed* of progress, not just the current status.

### 2. Exploratory Data Analysis (EDA)
* **Pivot Tables:** Grouped countries by `Income Group` and `Region` to calculate weighted averages for water access.
* **The Rural-Urban Gap:** Created comparative histograms to visualize how urban access clusters near 100% while rural access varies wildly (the "long tail" distribution).
* **Regional Deep Dive:** Identified **Sub-Saharan Africa** as the region with the highest variance—containing both the fastest-improving nations and those lagging behind.

### 3. Statistical Insights (Spreadsheet Functions)
* **Correlation Analysis** (`=CORREL`):
    * Calculated the correlation between **Rural ARC** and **National ARC**.
    * **Result:** `r ≈ 0.89`. This proves mathematically that national progress is almost entirely dependent on rural improvements.
* **Hypothesis Testing** (`=T.TEST`):
    * Conducted a Two-Sample T-Test assuming unequal variances.
    * **Result:** `p < 0.05`. We rejected the Null Hypothesis, confirming the "Rural-Urban Divide" is statistically significant and not just random chance.

### 4. Predictive Modeling
* **Linear Regression:**
    * Used Scatter Plots with the **Trendline** feature to fit a linear model (`y = mx + c`).
    * Displayed the **R² value** on the chart to assess goodness-of-fit.
* **Accuracy Check:**
    * Manually calculated **MAE (Mean Absolute Error)** using `=AVERAGE(ABS(Residuals))` to quantify the model's error margin.
    * Concluded that while the linear trend works for general predictions, demographic shifts require more complex modeling.

## 💡 Key Findings
1.  **Rural Focus is Key:** The data proves that urban improvements have diminishing returns. The fastest way to improve National statistics is to target Rural infrastructure.
2.  **Inequality by Income:** Low-income nations show the widest spread in performance, suggesting that funding and policy effectiveness vary more than in high-income nations.
3.  **The "S-Curve":** Progress is not linear. Countries start slow, accelerate rapidly during development (high ARC), and plateau once they reach ~95% access.

## 🚀 Future Work
* Integrate **GDP per capita** data to control for economic factors.
* Use the spreadsheet's `FORECAST.LINEAR` function to project specific timelines for achieving 100% access in lagging regions.

---
*This project was completed as part of the **ALX Data Analytics** program.*
