# 🌍 AtmosModel: King County $NO_2$ Prediction

**AtmosModel** is a machine learning project designed to quantify the impact of vehicle fleet composition—specifically the shift from internal combustion engines (ICE) to electric vehicles (EVs)—on urban air quality in King County, WA.

By integrating historical weather patterns with vehicle registration data, this model provides a data-driven look at how our transportation choices "raise the floor" of daily pollution.

---

## 🚀 Project Overview

* **Goal:** Predict daily $NO_2$ concentration levels and simulate long-term air quality scenarios.
* **The Problem:** While weather causes pollution to fluctuate, human activity creates a permanent baseline. This project quantifies that "Human Signal".
* **Key Finding:** Total fleet emissions account for **17.3%** of the model's decision-making logic, proving that vehicle mix is a primary driver of air quality, not just background noise.

---

## 🛠️ Technical Stack

* **Languages:** `Python` 🐍
* **ML Frameworks:** `Scikit-learn` (Gradient Boosting, Random Forest), `NumPy`, `Pandas`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Infrastructure:** Engineered a `total_fleet_emissions_index` to bridge the gap between monthly registration data and daily sensor readings.

---

## 📈 Key Results

### 1. Model Selection (The "Leaderboard") 🏆
After a systematic Grid Search with 5-Fold Cross-Validation, the **Gradient Boosting Regressor** emerged as the winner:
* **Gradient Boosting:** RMSE = 8.0784 ppb ✅
* **Random Forest:** RMSE = 8.1731 ppb
* **Ridge Regression:** RMSE = 8.7761 ppb

### 2. The "Gas Penalty" vs. "EV Dividend" ⚡
We performed a controlled sensitivity analysis to see what happens when you add 100,000 vehicles to the county:
* **+100,000 Pure BEVs:** **0.00 ppb** increase (Validated zero-tailpipe reality).
* **+100,000 Mixed EVs (BEV+PHEV):** **+0.46 ppb** increase.
* **+100,000 Gas Cars:** **+1.25 ppb** increase (A measurable degradation of the "pollution floor").

### 3. Feature Importance 🔍
The model successfully identified that while weather (Wind Speed & Temperature) is the strongest predictor, our engineered **Fleet Emissions Index (17.3%)** is the most significant human-controlled factor.

---

### 📉 Diverging Futures: The Three Scenarios

To ensure a fair comparison, the same "High Growth" rate was applied across all three models to see how technology alone changes the outcome.

* **Scenario A: The Real Trend (Mixed EV) 📉** This is the actual path King County is currently on. While EV adoption is growing rapidly, **18.5%** of those vehicles are currently Plug-in Hybrids (PHEVs). This scenario tracks the "pollution cost" of relying on transition technologies that still emit tailpipe exhaust.

* **Scenario B: The Gas Boom (Counterfactual) 🏗️** An "Alternate Universe" simulation where gasoline vehicle ownership grows at the same high rate as current EVs. This represents the "dirty" future and illustrates the **"Gas Penalty"**—a future where air quality degrades significantly faster than our current trend.

* **Scenario C: The Pure BEV Boom (Ideal) ✨** The **"Pollution Floor"**. This scenario simulates a future where the entire EV boom consists of 100% Zero-Emission Vehicles (BEVs). Because pure BEVs have zero tailpipe emissions, this line remains flat, representing the baseline pollution caused solely by weather and background sources.

---

### 🧱 The "Pollution Ceiling" & Model Saturation

A key discovery during the forecasting phase was the identification of a **Prediction Ceiling**.

* **Saturation Point:** Due to the sheer volume of projected vehicles in the "High Growth" models, both the Gas and Mixed-EV scenarios eventually hit a model-predicted ceiling of **24.75 ppb**.
* **Interpretation:** This suggests that beyond a certain vehicle density, the local atmosphere becomes saturated with $NO_2$, and the model hits its maximum historical learning limit.
* **The Hybrid Gap:** The gap between Scenario A (Mixed) and Scenario C (Pure BEV) quantifies the necessity of transitioning away from hybrids to reach the absolute minimum possible pollution levels.

---

## 📂 Project Structure

* `Exploratory Data Analysis V2.ipynb`: The whole project notebook.

---

## ✍️ Author
**Manvith Kothapalli**
*Computer Science @ University of Washington*
[LinkedIn](https://linkedin.com/in/manvith-kothapalli) | [GitHub](https://github.com/MarsManvith)

> **Aspire to Inspire:** Building intelligent systems to solve "unsolvable" environmental problems.
