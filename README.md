# 💼 Employment Across Regions

### Interactive Dashboard & Analytical Memory (CRISP-DM Approach)

![R](https://img.shields.io/badge/R-Data%20Science-blue?logo=r)
![Shiny](https://img.shields.io/badge/Shiny-Interactive%20Dashboard-red)
![CRISP-DM](https://img.shields.io/badge/Methodology-CRISP--DM-orange)

An **end-to-end labor market analysis project** that explores **employment dynamics across Europe and the Canary Islands**, combining:

* 🧭 an **interactive Shiny dashboard** for exploratory analysis
* 📄 a **[comprehensive analytical memory (HTML)](https://javierruanohdez.github.io/employment-across-regions/Employment_across_regionsMemory.html)** with structured results, modeling and interpretation

The project follows a **top-down analytical journey**, from **EU-wide aggregates** to **municipal-level insights in the Canary Islands**.

---

## 🧠 Analytical Framework – CRISP-DM

The project is structured according to the **CRISP-DM methodology**, ensuring analytical rigor and reproducibility:

### 1️⃣ Business Understanding

* Understand long-term employment evolution in Europe
* Identify **regional, sectoral, gender and age disparities**
* Relate employment to **economic development and social indicators**

### 2️⃣ Data Understanding

* Exploration of official labor market and demographic datasets
* Detection of trends, cycles, structural breaks and spatial heterogeneity

### 3️⃣ Data Preparation

* Cleaning, harmonization and reshaping
* Geographic alignment:
  **EU27 → Geographic regions → NUTS 0 → NUTS 2 → NUTS 3 → Municipal level**
* Variable transformations (e.g. **Yeo-Johnson**)

### 4️⃣ Modeling

* Time series analysis and decomposition
* **ARIMA modeling and forecasting**
* Correlation analysis and **PCA**

### 5️⃣ Evaluation

* Interpretation of trends, forecasts and multivariate structures
* Identification of methodological limitations

### 6️⃣ Deployment

* Interactive **Shiny dashboard**
* Reproducible **HTML analytical memory**

---

## 🧭 Interactive Shiny Dashboard

The **dashboard** is a Shiny-based interactive application structured into **eight main tabs**, following the analytical journey of the study.

### 🌍 Flexible Geographic Selection

Across the dashboard, users can dynamically select:

* **EU27_2020 aggregate**
* **European geographic regions** (North, South, East, West)
* **NUTS levels**:

  * NUTS 0 (countries)
  * NUTS 1
  * NUTS 2
  * NUTS 3

---

### 📌 Dashboard Tabs

#### 🔹 Intro

* Project objectives and analytical scope
* Tools and methodology
* Data sources overview

#### 🔹 Overview

* High-level employment evolution
* Sectoral participation
* Gender employment gap
* Dynamic comparison across regions and scales

#### 🔹 Time Series

* Detailed time series analysis by:

  * Sector
  * Sex
  * Age group
* Individual and grouped visualizations
* Implemented using **fpp3**

#### 🔹 EuroMap Explorer

Geospatial analysis hub with **three interactive Leaflet maps**:

1. Employment by region (NUTS)
2. Employment by sex & age
3. Key indicators vs employment

#### 🔹 Attribute Showdown

* Bivariate analysis
* Linear regressions
* Variable transformations (Yeo-Johnson)

#### 🔹 ARIMA Forecast

* Time series forecasting
* Manual parameter tuning
* Shock interpolation
  *(extended and formalized in the analytical memory)*

#### 🔹 Correlation Matrix & PCA Analysis

* Interactive correlation matrix
* Principal Component Analysis
* Identification of latent dimensions

#### 🔹 Canary Insights

* Municipal employment maps
* Sankey diagram (age → sex → employment)
* Radar chart (FP vs University)
* Contract typology and 2022 labor reform impact

---

## 📄 Analytical Memory – Results & Interpretation

The **analytical memory** expands and formalizes the insights explored in the dashboard, providing **context, interpretation and methodological depth**.

It includes:

* EU-wide employment evolution (2000–2022)
* Regional and national disparities
* Gender and age gap analysis
* Sectoral structure and transformation
* Spain and Canary Islands deep-dive
* ARIMA modeling and counterfactual scenarios
* Correlation and PCA analysis
* Methodological evaluation and limitations

---

## 📊 Data Sources

### 🇪🇺 Eurostat

**Main dataset**

* `nama_10r_3empers`
  *Employment (thousand persons) by NUTS 3 region*

**Secondary datasets**

* `demo_r_pjanaggr3`
  *Population by age group, sex and NUTS 3*
* `lfst_r_lfe2emprt`
  *Employment rates by sex, age and NUTS 2 (%)*

---

### 🌍 Our World in Data (OWID)

Socioeconomic and structural indicators used for correlation and multivariate analysis:

* population
* median_age
* life_expectancy
* GDP_per_capita
* working_hours_per_year
* productivity
* human_development_index
* only_basic_education
* till_secondary_education
* tertiary_education
* gender_wage_gap
* immigrant_share_of_population
* fertility_rate
* extreme_poverty_share
* extreme_poverty_number
* prevalence_undernourishment_share
* education_expenditure_share_gdp
* healthcare_expenditure_share_gdp
* land_use_in_hectares
* emissions_total_per_capita

---

### 🇮🇨 ISTAC (Instituto Canario de Estadística)

* Labor insertion:

  * FP vs University degree
* Municipal employment indicators (2024)

---

### 🇮🇨 OBECAN (Observatorio Canario de Empleo)

* Employment contracts by island
* Period: 2018–2024

---

## ⚙️ Installation & Data Requirements

### 🔴 Required Data (Critical)

All **ZIP files inside `required_data/` must be extracted**.

👉 **The extracted files must be placed at the same directory level as:**

```
Employment_across_regionsDashboard.Rmd
Employment_across_regionsMemory.Rmd
```

They must coexist in the **project root**.
Otherwise, **neither the dashboard nor the analytical memory will run correctly**.

---

## ▶ Usage

### Run the Dashboard

You can run the dashboard in **two equivalent ways**:

**Option 1 – From the console**

```r
shiny::runApp()
```

**Option 2 – From RStudio**

* Open `Employment_across_regionsDashboard.Rmd`
* Click **Run Document**

---

### Generate the Analytical Memory

1. Open:

```
Employment_across_regionsMemory.Rmd
```

2. Click **Knit** to generate:

```
Employment_across_regionsMemory.html
```

---

## 🧠 Conclusions

* Aggregate EU employment growth masks **deep territorial and structural inequalities**
* Productive structure strongly conditions employment outcomes, gender gaps and income
* Southern and island economies exhibit higher volatility and shock sensitivity
* Labor market reforms can have **rapid and measurable effects**
* A **multiscale, data-driven approach** is essential for informed territorial policy design

---
