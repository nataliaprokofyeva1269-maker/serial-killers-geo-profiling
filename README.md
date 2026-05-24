Hunting the Pattern: Geographic & Temporal Profiling of Serial Killers

An end-to-end Data Science and Machine Learning project analyzing the operational footprint, historical trends, and predictive behavioral features of extreme offenders globally.

---

##  Project Overview

This project deconstructs the common mythology surrounding serial crime into clinical, mathematical truths. By integrating exploratory data analysis (EDA), geospatial visualization, and machine learning models, the project isolates the structural and systemic drivers that govern an offender's total impact.

### Key Datasets Integrated:
* **Primary Numerical Data:** 305 records containing proven/possible victim counts, operational years, and countries.
* **Cross-Referenced Wikipedia Registry:** 328 additional records providing granular data on execution methods, judicial status, and gender.
* **Combined Master Database:** **633 distinct offenders across 101 countries spanning 6 continents.**

---

##  Repository Structure

The project is modularized into dedicated Jupyter Notebooks mirroring professional data pipelines:

* **`01_EDA_profiling.ipynb`**: Data cleaning, deduplication, demographic profiling, and baseline distribution checks.
* **`02_geographic_analysis.ipynb`**: Geospatial density calculations ($Per\ Capita$), normalization for demographic size, and interactive mapping.
* **`03_predictive_model.ipynb`**: Feature engineering and training of Machine Learning models to analyze structural factors.

---

##  Machine Learning Architecture & Key Insights

Rather than chasing pure predictive accuracy on a highly volatile and compact dataset ($N=633$), the analytical focus was placed on **Feature Importance** and **Partial Effects Analysis** using a Random Forest framework.

###  Model A: Predicting Scale (Total Victim Count)
* **Core Takeaway:** Geography is the ultimate spatial predictor of scale.
* **Key Feature Weights:** Operating in the US ($0.265$ importance) or Europe ($0.169$) drastically impacts the expected death toll.
* **The Western Suppressor Effect:** Partial effects modeling mathematically demonstrates that operating within the US or Europe cuts the expected victim count nearly in half compared to non-Western regions, highlighting the impact of systemic law enforcement containment.

###  Model B: Predicting Longevity (Years Active Before Capture)
* **Core Takeaway:** Technology and historical era completely override individual "criminal genius."
* **Key Feature Weights:** The operational decade (`Era`) absolutely dominates the model with a feature importance of **$0.611$**.
* **The 1990s Boundary:** The inclusion of the `Active after 1990` variable identifies a permanent structural break. The globalization of DNA profiling (CODIS) and digitized cross-jurisdictional databases fundamentally collapsed the evasion window for modern offenders.

---

## Critical Analytical Discoveries

1.  **The Power Law Distribution:** Serial homicide is highly skewed. A strict Pareto dynamic applies: the top **$10\%$** most lethal offenders drive approximately **$36\%$** of all recorded fatalities globally.
2.  **The Per-Capita Illusion (Documentation Bias):** While the US dominates absolute volume ($95$ offenders), it ranks low adjusted for population ($3.2$ per $10\text{M}$). Massive per-capita spikes in small nations (e.g., Estonia at $60.0$) represent a classic documentation bias where minor sample sizes skew relative metrics.
3.  **The Poison Anomaly & The Judicial Paradox:** * While male methodology is fragmented, over **$80\%$** of female offenders heavily concentrate on poisoning *(among cases with known methods)*.
    * This high degree of premeditation eliminates the legal defense of impulsivity, explaining why **$>50\%$** of female offenders face execution, outstripping the male execution rate ($\sim 35\%$).

---

## Tech Stack & Libraries

* **Data Manipulation:** `Python`, `pandas`, `NumPy`
* **Visualization:** `matplotlib`, `seaborn`, `Folium` (Interactive Choropleth Maps)
* **Machine Learning:** `scikit-learn` (Random Forest Regressor, Feature Importance, Partial Dependence)

---

## Factual Limitations & Caveats

* **Sample Scale:** $633$ historical records provide an exploratory baseline; results are structural signals rather than definitive deployment forecasting.
* **Reporting Bias:** Missing categorical data (specifically regarding execution methods, which are documented for only $\sim 20\%$ of the data) represents systemic international archiving variances.

```
