# Quantium Data Analytics Job Simulation — Forage

![Quantium](https://img.shields.io/badge/Quantium-Data%20Analytics-1D9E75?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.10-blue?style=for-the-badge&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge&logo=pandas)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## Overview

This repository contains my completed work for the **Quantium Data Analytics Job Simulation** hosted on [Forage](https://www.theforage.com/simulations/quantium/data-analytics-rqkb).

The simulation placed me in the role of a data analyst on Quantium's retail analytics team, working with real-world transaction and customer behaviour data to deliver commercial insights and recommendations to a client Category Manager.

**Analyst:** Dinesh Navaneethan  
**Programme:** Quantium Data Analytics | Forage  
**Completed:** April 2025  
**Tools:** Python · Pandas · NumPy · Matplotlib · Seaborn · Scipy · PowerPoint  

---

## Repository Structure

```
quantium-data-analytics-forage/
│
├── Task1/
│   └── QVI_Task1_Dinesh.ipynb        # Customer analytics & segmentation
│
├── Task2/
│   └── QVI_Task2_Dinesh.ipynb        # Uplift testing & trial assessment
│
├── Task3/
│   └── Quantium_Task3_Dinesh.pptx    # Client-ready presentation (Pyramid Principle)
│
├── outputs/
│   ├── plot_sales_by_segment.png
│   ├── plot_customers_by_segment.png
│   ├── plot_brand_affinity.png
│   ├── plot_price_per_unit.png
│   ├── plot_monthly_sales.png
│   ├── plot_pack_size.png
│   ├── plot_pretrial_alignment.png
│   ├── plot_trial_assessment_sales.png
│   ├── plot_trial_assessment_customers.png
│   └── plot_uplift_summary.png
│
└── README.md
```

---

## Task 1 — Customer Analytics & Segmentation

**Objective:** Analyse transaction and customer behaviour data to understand chip purchasing trends across customer segments and deliver commercial recommendations.

### What I did
- Loaded and performed high-level quality checks on `QVI_transaction_data.xlsx` and `QVI_purchase_behaviour.csv`
- Fixed date formatting (Excel serial integers → datetime), removed salsa products and outlier customers purchasing 200+ units
- Extracted `PACK_SIZE` and `BRAND` features from product name strings using regex
- Merged transaction and behaviour datasets and created a `LIFESTAGE × PREMIUM_CUSTOMER` segment column
- Analysed total sales, unique customers, units per transaction and average spend per segment
- Ran a two-sample t-test to confirm whether Mainstream Young Singles/Couples pay significantly more per unit than the rest of the population
- Computed brand and pack size affinity scores for the target segment

### Key Findings
| Insight | Finding |
|--------|---------|
| Top revenue segment | Budget – Older Families |
| Highest growth potential | Mainstream – Young Singles/Couples |
| Price premium confirmed | Mainstream Young Singles/Couples pay more per unit (p < 0.05) |
| Brand affinity | Over-index on Tyrrells vs general population |
| Pack size preference | 150g–175g packs — consistent with impulse/on-the-go occasions |

### Sample Output

![Sales by Segment](outputs/plot_sales_by_segment.png)
![Brand Affinity](outputs/plot_brand_affinity.png)

---

## Task 2 — Experimentation & Uplift Testing

**Objective:** Assess whether the new trial store layout (stores 77, 86, 88) drove a statistically significant uplift in chip sales and customer numbers vs comparable control stores.

### What I did
- Built monthly store-level metrics (total sales, unique customers, transactions) for the pre-trial (Jul 2018–Jan 2019) and trial (Feb–Apr 2019) periods
- Developed a control store matching function using two complementary similarity metrics:
  - **Pearson correlation** — tracks whether stores move together over time
  - **Magnitude distance** — measures whether absolute sales levels are similar
- Selected the highest-scoring control store for each trial store
- Scaled control store performance to the trial store's pre-trial baseline
- Used **paired t-tests** to determine whether trial period performance was statistically significantly different from control

### Control Store Mapping
| Trial Store | Control Store | Method |
|-------------|---------------|--------|
| Store 77 | Best matched via combined score | Pearson + Magnitude |
| Store 86 | Best matched via combined score | Pearson + Magnitude |
| Store 88 | Best matched via combined score | Pearson + Magnitude |

### Sample Output

![Pre-Trial Alignment](outputs/plot_pretrial_alignment.png)
![Uplift Summary](outputs/plot_uplift_summary.png)

---

## Task 3 — Client Report (Pyramid Principle)

**Objective:** Compile findings from Tasks 1 and 2 into a structured, client-ready presentation for Julia (Category Manager), following Quantium's Pyramid Principle reporting standard.

### Slide Structure
| Slide | Content |
|-------|---------|
| 1 | Cover |
| 2 | Agenda |
| 3 | Executive Summary |
| 4 | Section break — Category |
| 5 | Category Overview |
| 6 | Customer Segmentation |
| 7 | Section break — Trial |
| 8 | Control Store Methodology |
| 9 | Trial Results — Sales Uplift |
| 10 | Trial Results — Customer Numbers |
| 11 | Recommendations |
| 12 | Next Steps |
| 13 | Closing |

---

## Skills Demonstrated

- **Data cleaning & wrangling** — handling missing values, outliers, date formatting, regex feature extraction
- **Exploratory data analysis** — segment profiling, distribution analysis, trend identification
- **Statistical testing** — two-sample t-tests, paired t-tests, p-value interpretation
- **Control experiment design** — Pearson correlation matching, magnitude distance scoring
- **Data visualisation** — Matplotlib, Seaborn, chart design for business audiences
- **Business communication** — Pyramid Principle, stakeholder-ready reporting, commercial recommendations


## Certificate

Completed via the [Quantium Data Analytics Job Simulation on Forage](https://www.theforage.com/simulations/quantium/data-analytics-rqkb).

---

*Built as part of an ongoing data analytics portfolio. Connect with me on [LinkedIn](https://linkedin.com/in/dineshnavaneethan).*
