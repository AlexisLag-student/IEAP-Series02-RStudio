# Statistical Tests and Data Analysis

**Author:** Alexis LAGARDE  
**Date:** `r format(Sys.time(), '%d %B, %Y, %H:%M')`  
**Time to complete:** Approximatly 6.5 hours

---

## Overview

This project explores statistical concepts and performs data analysis using R. The main focus is on:

1. Understanding basic statistical concepts and tests.
2. Comparing groups to determine effects of treatments.
3. Exploring relationships and correlations among variables.
4. Testing common stereotypes using anthropometric data.

The analysis uses two datasets:  
- `PrePost.csv` — heart rate measurements before and after a rehabilitation program.  
- `snore.txt` — anthropometric and lifestyle data, including snoring status, weight, sex, alcohol consumption, and smoking habits.

---

## Project Structure

- `PrePost.csv` — contains heart rate data (`perf`) measured before and after rehabilitation (`time`).  
- `snore.txt` — contains information on participants including snoring status (`snore`), weight (`weight`), sex (`sex`), alcohol consumption (`alcool`), and smoking habits (`tabac`).  
- `Series02.Rmd` — R Markdown file containing all code, figures, and interpretations.  

---

## Analysis Summary

### 1. Statistical Concepts

- Median vs. Mean
- Variance and Standard Deviation
- Normal Distribution
- Parametric vs. Non-parametric Tests
- Paired vs. Unpaired Tests
- P-values and Type I/II Errors

### 2. Effect of Treatment Over Time

- **Dataset:** `PrePost.csv`
- **Objective:** Determine if rehabilitation increases heart rate performance.
- **Method:** Paired comparison of `perf` before and after treatment.  
  - Sample size is small, so a non-parametric test (Mann–Whitney U) is used.
- **Result:** Heart rate generally increased after rehabilitation, indicating that the treatment was effective.
- **Visualization:** Box plot showing `perf` distribution before and after rehabilitation.

### 3. Testing Stereotypes in Snorers

- **Dataset:** `snore.txt`
- **Findings:**
  - **Weight:** Snorers tend to have higher weight than non-snorers.
  - **Alcohol Consumption:** Snorers consume slightly more alcohol, but the difference is minor.
  - **Smoking Habits:** A higher proportion of snorers are smokers; this difference is more pronounced than for alcohol.
  - **Sex Differences:** 
    - Men are not fatter than women; women show slightly higher median weight.  
    - Women smoke significantly less than men (confirmed with Chi-squared test, p < 0.05).

### 4. Correlation Analysis

- Computed correlations among numeric variables: `age`, `weight`, `height`, `alcool`.
- **Findings:**
  - Height and weight are very strongly correlated (0.93).  
  - All other correlations are weak or negligible.
- **Conclusion:** Height and weight are the only strongly related variables; age and alcohol consumption show no meaningful correlations.

---

## Figures

1. **Box plots** for comparing weight by snoring status and sex.
2. **Bar plots** for alcohol and smoking status by snoring status and sex.
3. **Box plot** for heart rate before and after rehabilitation.
4. **Correlation plot** of numeric variables.

---

## Dependencies

The following R packages are used in this project:

- `ggplot2`
- `dplyr`
- `tidyr`
- `corrplot`
- `knitr`

Install missing packages using:

```r
install.packages(c("ggplot2", "dplyr", "tidyr", "corrplot", "knitr"))
```