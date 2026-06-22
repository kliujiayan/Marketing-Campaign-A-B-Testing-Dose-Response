# Marketing Campaign | A/B Testing & Dose-Response Analysis

## Overview

This project analyzes a real-world marketing A/B test to determine whether an ad campaign
drove meaningfully higher conversions compared to a neutral public service announcement (PSA)
control group. Rather than stopping at a simple p-value, this analysis takes a more complete
approach — including confidence interval visualization, a chi-square cross-check, and a
dose-response analysis examining how ad exposure level influences conversion likelihood.

## Business Question

**Did the ad campaign work, and if so, how should it inform future campaign strategy?**

## Dataset

- **Source:** [Marketing A/B Testing by faviovaz (Kaggle)](https://www.kaggle.com/datasets/faviovaz/marketing-ab-testing)
- **Size:** ~588,000 users
- **Groups:** Ad group (treatment) vs. PSA group (control)
- **Primary metric:** Conversion rate (proportion of users who converted)

## Key Findings

|Metric                   |Value                      |
|-------------------------|---------------------------|
|Ad group conversion rate |2.55%                      |
|PSA group conversion rate|1.79%                      |
|Absolute lift            |0.77 percentage points     |
|Relative lift            |43.09%                     |
|Z-statistic              |7.37                       |
|P-value                  |< 0.0001                   |
|Result                   |Statistically significant ✓|

## Methodology

1. **Sanity check** — Sample ratio mismatch test to validate the experiment setup
1. **Statistical testing** — Two-proportion z-test and chi-square cross-check
1. **Confidence intervals** — 95% CIs computed and visualized for both groups
1. **Dose-response analysis** — Conversion rate examined across ad exposure buckets
1. **Temporal segmentation** — Conversion patterns analyzed by day of week and hour of day
1. **Stakeholder recommendation** — Business conclusions drawn from all findings

## Recommendations

- **Continue the ad campaign** — the 43.09% relative lift over the PSA control is statistically significant and practically meaningful
- **Increase ad frequency for engaged users** — conversion peaks at 81–200 ads seen (~17%), suggesting heavy exposure drives significantly higher conversion
- **Concentrate spend on Mondays and Tuesdays** — weekday conversion rates (3.28%, 2.98%) meaningfully outperform weekends (2.11%–2.45%)
- **Schedule ads between 2 PM and 10 PM** — conversion peaks at 4 PM (3.1%) and remains strong through the evening

## Tools & Libraries

- **Python** — pandas, numpy, scipy, statsmodels, matplotlib, seaborn
- **Statistical methods** — two-proportion z-test, chi-square test, proportion confidence intervals

## Files

- `marketing-campaign-ab-testing-dose-response.ipynb` — full analysis notebook

## Notebook

Full analysis available on Kaggle:
[Marketing Campaign | A/B Testing, Dose-Response](https://www.kaggle.com/code/kliujiayan/marketing-campaign-a-b-testing-dose-response/notebook)
