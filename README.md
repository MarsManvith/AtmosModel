# 🌍 AtmosModel: King County $NO_2$ Prediction

[cite_start]**AtmosModel** is a machine learning project designed to quantify the impact of vehicle fleet composition—specifically the shift from internal combustion engines (ICE) to electric vehicles (EVs)—on urban air quality in King County, WA[cite: 32]. 

[cite_start]By integrating historical weather patterns with vehicle registration data, this model provides a data-driven look at how our transportation choices "raise the floor" of daily pollution[cite: 32].

---

## 🚀 Project Overview
* [cite_start]**Goal:** Predict daily $NO_2$ concentration levels and simulate long-term air quality scenarios[cite: 34].
* **The Problem:** While weather causes pollution to fluctuate, human activity creates a permanent baseline.
* [cite_start]**Key Finding:** Total fleet emissions account for **17.3%** of the model's decision-making logic, proving that vehicle mix is a primary driver of air quality[cite: 36].

---

## 🛠️ Technical Stack
* [cite_start]**Languages:** `Python` 🐍 [cite: 32]
* [cite_start]**ML Frameworks:** `Scikit-learn` (Gradient Boosting, Random Forest), `NumPy`, `Pandas` [cite: 32]
* [cite_start]**Visualization:** `Matplotlib`, `Seaborn` [cite: 32, 37]

---

## 🔮 15-Year Air Quality Forecast
To answer how fleet adoption trends influence air quality, I simulated three diverging futures (2025–2040) using the **Compound Annual Growth Rate (CAGR)** from historical data.

### 📉 The Three Scenarios
* **Scenario A: The Real Trend (Mixed EV) 📉** This represents the actual path King County is on. It includes a mix of Pure BEVs and Plug-in Hybrids (PHEVs). The "Hybrid Gap" quantifies the pollution cost of relying on transition technologies.

* **Scenario B: The Gas Boom (Counterfactual) 🏗️** A simulation where gas cars grow at the high EV rate. This confirms the **"Gas Penalty"**—air quality degrades significantly faster than under current trends.

* **Scenario C: The Pure BEV Boom (Ideal) ✨** The **"Pollution Floor."** Since pure BEVs emit zero tailpipe pollutants, this represents the baseline pollution caused solely by weather and background sources.

---

## 🧱 The "Pollution Ceiling"
* **Model Saturation:** In both the Gas and Mixed-EV high-growth scenarios, the model eventually hits a prediction ceiling of **24.75 ppb**. 
* **The Takeaway:** While Scenario A (current path) is better than a Gas Boom, achieving the absolute minimum pollution (Scenario C) requires a transition away from hybrids to 100% zero-emission vehicles.

---

## 📈 Key Sensitivity Results
* **+100,000 Pure BEVs:** Resulted in **0.00 ppb** change (Model successfully learned physical reality).
* [cite_start]**+100,000 Gas Cars:** Resulted in a measurable increase of **+1.25 ppb** in daily $NO_2$ concentration[cite: 35].

---

## ✍️ Author
[cite_start]**Manvith Kothapalli** *Computer Science @ University of Washington* [cite: 1, 4]  
[LinkedIn](https://linkedin.com/in/manvith-kothapalli) | [GitHub](https://github.com/MarsManvith)

> **Aspire to Inspire:** Building intelligent systems to solve "unsolvable" environmental problems.
