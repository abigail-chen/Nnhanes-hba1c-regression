# NHANES HbA1c Regression Analysis

**Multiple Linear Regression | R | Statistical Modeling | Model Diagnostics**

## Overview

This project investigates the associations between HbA1c levels and demographic, physiological, and dietary factors using data from the National Health and Nutrition Examination Survey (NHANES).

The analysis focuses on developing an interpretable multiple linear regression model, addressing model assumption violations, and evaluating the stability of estimated associations across survey cycles.

📄 **[View Research Poster](NHANES_HbA1c_Research_Poster.pdf)**

## Data

- **Training:** NHANES 2021–2023, 5,556 observations
- **Validation:** NHANES 2017–2018, 5,787 observations

Variables include HbA1c, age, gender, race/ethnicity, BMI, and dietary intake measures.

## Methodology

1. **Exploratory Data Analysis:** Examined variable distributions, outliers, and relationships with HbA1c.
2. **Model Development:** Fitted multiple linear regression models and refined predictor selection.
3. **Transformations:** Applied response and predictor transformations to address skewness and heteroskedasticity.
4. **Model Diagnostics:** Assessed residual patterns, influential observations, normality, and multicollinearity using VIF.
5. **Cross-Cycle Validation:** Compared model estimates, statistical significance, and diagnostics across NHANES survey cycles.

## Key Results

- The final model was statistically significant (F(14, 5541) ≈ 108, p < 2.2 × 10⁻¹⁶).
- Training adjusted R²: **0.2128**.
- Validation adjusted R²: **0.2582**.
- Age and BMI showed positive associations with HbA1c.
- Dietary variables, including sugar, fibre, and carbohydrate intake, showed significant associations in the fitted model.
- Model refinement reduced multicollinearity, although some residual assumption violations remained.

These findings represent statistical associations rather than causal effects. Cross-cycle comparisons indicate relative stability in several estimated associations but do not establish out-of-sample predictive accuracy.

## Repository Contents

- `analysis.Rmd` — Complete R Markdown analysis
- `data/` — Training and validation datasets
- `NHANES_HbA1c_Research_Poster.pdf` — Research poster presenting the methodology and findings
- `references.bib` — Bibliographic references
- `apa.csl` — APA citation formatting

## Reproducibility

The analysis was conducted in R using R Markdown.

To reproduce the analysis:

1. Download or clone this repository.
2. Install the R packages referenced in `analysis.Rmd`.
3. Confirm the dataset paths match those used in the R Markdown file.
4. Open `analysis.Rmd` in RStudio and knit the document.

## Project Context

University of Toronto — STA302: Methods of Data Analysis.
