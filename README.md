# Crime Dynamics: How Socioeconomic Factors Influence Mischief and Break-and-Enter Crimes

This project investigates how neighborhood-level socioeconomic factors—**income inequality**, **education level**, **average age**, and **population density**—influence crime rates in Vancouver, specifically focusing on **Mischief** and **Break-and-Enter Residential/Other (BER)** crimes.

## 📝 Project Overview

- **Research Question:**  
  *How do demographic and economic factors contribute to the rates of Mischief and Break-and-Enter crimes in Vancouver neighborhoods?*

- **Datasets Used:**
  - 2021 Canadian Census (socioeconomic characteristics)
  - 2023 Vancouver Police Department (VPD) Crime Statistics

- **Key Variables:**
  - Gini Index (income inequality)
  - Average Age
  - Education Level
  - Population Density (control)

- **Crime Types Analyzed:**
  - Mischief
  - Break-and-Enter Residential/Other (BER)

## 🛠 Methods

- Data cleaning, feature selection, and merging neighborhood-level datasets.
- **Multiple Linear Regression** to estimate relationships between socioeconomic variables and crime rates.
- **Model specifications tested**:
  - Baseline model: Gini Index, Education Level, Average Age
  - Omitting Education Level
  - Adding Population Density as a control
  - Including quadratic term for Average Age (to model non-linear effects)
- **Specification Checks**:
  - **Variance Inflation Factor (VIF)** test for multicollinearity
  - **Breusch-Pagan Test** for heteroskedasticity
  - Corrected for heteroskedasticity using robust standard errors

## 🔧 Technologies Used

- R programming language
- Libraries: `tidyverse`, `car`, `stargazer`, `sandwich`, `lmtest`

## 📊 Key Findings

- **Income Inequality (Gini Index)**:
  - Strongest and most consistent predictor for both Mischief and Break-and-Enter (BER) crimes.
  - Higher Gini Index values correlated with higher crime rates across all model specifications.

- **Average Age**:
  - Negative association with Mischief crimes: older neighborhoods generally experienced fewer Mischief incidents.
  - Nonlinear relationship observed:
    - Mischief crimes peaked at average ages between **35–45** years.
    - Break-and-Enter crimes peaked around **40–50** years.

- **Education Level**:
  - Statistically significant for Mischief crimes (positive effect), but not significant for Break-and-Enter crimes.
  - Indicates education has a crime-type-specific influence.

- **Population Density**:
  - Positively and significantly associated with both Mischief and Break-and-Enter crimes.
  - Denser areas reported more incidents of both crime types.

- **Model Robustness**:
  - **VIF tests** confirmed no multicollinearity (all VIFs well below 5).
  - **Breusch-Pagan Tests** revealed heteroskedasticity; addressed using robust standard errors.
  - Main results (Gini Index, Population Density effects) remained stable across robustness checks.

- **Nonlinear Effects**:
  - Marginal effect plots confirmed a nonlinear influence of Average Age on crime rates, validating model extensions.

## 👥 Authors

- Srijan Sanghera
- Hrishikesh Dalal
- Vashisht Raghav

## 📂 Project Structure

- `FINAL_Project_Crime_Socioeconomic_Analysis.ipynb` — Jupyter Notebook containing data preparation, modeling, visualization, and robustness analysis.
- `Crime_Socioeconomic_Analysis_Vancouver_Report.pdf` — Research paper detailing the research motivation, methodology, results, and discussion.
