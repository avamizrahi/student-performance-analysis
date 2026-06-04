# Student Performance & Alcohol Consumption Analysis

## Overview
Statistical analysis examining how weekday alcohol consumption, study 
habits, and demographic factors predict student academic performance. 
Uses data from Portuguese secondary school students in math and 
Portuguese courses.

## Data
- UCI Student Performance Dataset (included in repo)
- `student-mat.csv` — math course (395 students)
- `student-por.csv` — Portuguese course (649 students)
- Combined dataset: 1,044 students across both subjects

## Methods
- Data cleaning and feature engineering (alcohol consumption groups,
  pass/fail outcome)
- Exploratory data analysis with ggplot2
- Two-way ANOVA (sex × weekday alcohol group) — low R², violated
  normality, abandoned
- Logistic regression predicting pass/fail (final grade ≥ 10)
- Odds ratios and 95% confidence intervals
- Model comparison: full vs reduced model using AIC, BIC, chi-square test
- Cook's Distance outlier detection and model refitting

## Key Findings
- Two-way ANOVA explained only ~1% of variance — poor fit
- Logistic regression pseudo R² = 0.118 — meaningful improvement
- Prior failures and study time are the strongest predictors of passing
- Weekday alcohol consumption and going out frequency have negative
  effects on pass probability
- Model accuracy improved after removing influential points

## Tools & Libraries
R, RMarkdown, tidyverse, ggplot2, dplyr, car, broom, ggpubr
