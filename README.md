# MasterControl Sales Lead Conversion Analysis
**Spring 2026 MSBA Capstone | University of Utah**

## Project Overview

MasterControl is a B2B SaaS company selling quality management software to life sciences
and manufacturing companies. Their sales team generates thousands of qualified leads
(QALs) each year across two product lines — Mx and Qx — but conversion rates vary
significantly across customer segments, and it wasn't clear which leads were worth
prioritizing.

Our team analyzed 16,644 historical sales leads to answer two questions:
1. Which leads are most likely to convert?
2. What actions can sales leadership take to improve conversion rates?

## What I Did

- Cleaned and explored the full QAL dataset, identifying patterns across industry,
  account type, title, and product line
- Built a logistic regression model to predict lead conversion probability
- Investigated cross-sell opportunities between Mx and Qx product lines using
  contact-level ID matching
- Translated model outputs into concrete, actionable business recommendations

## Key Findings

**The conversion gap is real and addressable.**
Mx converts at 13.0% vs. Qx at 20.2% — a 56% relative gap. The model (AUC = 0.816)
identified the drivers behind this gap.

**Segment targeting matters more than volume.**
CMO/CDMO accounts convert at 17.1% on Mx — significantly above average. Pharma accounts
show a strong interaction effect with CMO/CDMO, amplifying conversion even further.

**High-intent leads are your best asset.**
Leads flagged as high-priority convert at 28.2%, nearly double the baseline.
Focusing outreach here is the highest-leverage move available.

**Title signals are counterintuitive.**
Manager-level contacts actually outperform executive-level contacts on Mx — 
suggesting that the person closest to the pain point, not the budget holder,
drives more conversions at this stage.

**Cross-sell opportunity exists but is underutilized.**
Contact-level analysis revealed accounts with both Mx and Qx touchpoints,
pointing to a structured cross-sell motion MasterControl hasn't fully operationalized.

## Business Impact

If MasterControl shifts outreach toward high-conversion segments — CMO/CDMO accounts,
high-priority leads, and manager-level contacts — our model projects moving Mx
conversion from 13% to 17%, yielding approximately **163 additional conversions per year**.
At typical SaaS deal values, this represents a meaningful revenue lift without
increasing the size of the lead pool.

## Tools & Methods

- Python (pandas, scikit-learn, matplotlib, seaborn)
- Logistic Regression with interaction terms
- Exploratory Data Analysis
- PowerPoint for executive-facing presentation

## Files in This Repo

- `EDA_notebook.ipynb` — Exploratory analysis of lead data by segment, industry, and title
- `Modeling_notebook.ipynb` — Logistic regression model, feature interpretation, and
   interaction term analysis
