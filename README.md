# A/B Test Analysis: Landing Page Conversion

## Overview
This project analyzes the results of an A/B test designed to evaluate whether a new website page improves user conversion rates compared to an existing version. The analysis focuses on validating the experiment setup, comparing conversion performance between control and treatment groups, and applying statistical hypothesis testing to support a data-driven business decision.

---

## Data
The dataset consists of anonymized website experiment data, including:
- User assignment to control or treatment groups
- Landing page exposure (old vs. new)
- Binary conversion outcomes
- Timestamps for user sessions

The dataset is not included in this repository due to size constraints.

---

## Experiment Validation and Cleaning
Before analysis, the experiment setup was validated to ensure users were exposed to the correct landing page for their assigned group. A small number of sessions were found where group assignments did not match page exposure. These mismatched 
records were removed to prevent contamination of the treatment effect and preserve experimental integrity.

---

## Conversion Analysis
After cleaning, conversion rates were calculated for both groups:
- The control group (old landing page) showed a slightly higher conversion rate than the treatment group.
- The observed difference between groups was small and required statistical testing to determine whether it represented a true effect or random variation.

---

## Hypothesis Testing and Results
A two-proportion z-test was conducted at a 5% significance level to compare conversion rates between the control and treatment groups.

- **Null Hypothesis:** The conversion rates of the new and old landing pages are equal.
- **Alternative Hypothesis:** The conversion rates of the new and old landing pages differ.

The resulting p-value exceeded the significance threshold, indicating no statistically significant difference between the two landing pages. As a result, the null hypothesis was not rejected.

---

## Business Decision
Based on this analysis, there is insufficient evidence to support rolling out the new landing page. The data suggests that the change does not improve conversion performance and could introduce unnecessary risk without measurable benefit. Resources would be better allocated toward testing alternative designs or targeted user segments.

---

## Limitations and Next Steps
This analysis evaluates overall conversion performance and does not account for potential differences across user segments such as device type, geography, or visit timing. Additionally, only conversion outcomes were analyzed, excluding downstream metrics like revenue or retention.

Future work could include segmented A/B tests, alternative landing page designs, or multivariate testing to identify targeted improvements.

---

## Tools & Technologies
- Python
- pandas, NumPy
- statsmodels
- matplotlib
- Jupyter Notebook
