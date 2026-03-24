# Fast Food Density & Obesity Analysis

**Tools:** Power BI, Microsoft Excel
**Data Sources:** Datafiniti Fast-Food Restaurants Dataset · CDC Nutrition, Physical Activity & Obesity (2023)
**Course:** ITEC 4210 — Georgia Gwinnett College, Spring 2025

---

## Project Overview

Does living in a state with more fast-food restaurants make you more likely to be obese? This project set out to test that assumption using real-world, state-level data from across the United States.

By joining restaurant count data with CDC obesity prevalence rates, the analysis examines whether fast-food availability is a meaningful predictor of adult obesity — or whether the relationship is more nuanced than the popular narrative suggests.

---

## Datasets

| Dataset | Source | Key Fields Used |
|---|---|---|
| Datafiniti Fast-Food Restaurants | Datafiniti / Kaggle | `state`, `restaurant_id` |
| CDC Nutrition, Physical Activity & Obesity | CDC (2023) | `state`, `obesity_rate (%)` |

Both datasets were joined on **state abbreviation**.

---

## Data Wrangling Steps

- Removed irrelevant fields (addresses, phone numbers, URLs)
- Standardized state abbreviations across both datasets
- Converted obesity values to numeric format
- Engineered two summary tables:
  - `RestaurantsByState` — total restaurant count per state
  - `ObesityByState2023` — obesity rate + tier category per state
- Classified states into obesity tiers: **Low** (<35%), **Medium** (35–38%), **High** (>38%)

---

## Dashboard

The Power BI dashboard contains four panels:

| Visual | Purpose |
|---|---|
| **Bubble Map** | Geographic distribution of fast-food restaurants across the U.S. |
| **Bar Chart** | Top states ranked by restaurant count (CA, TX, FL lead) |
| **Scatter Plot** | Restaurant count vs. obesity rate — tests the core hypothesis |
| **Treemap** | States grouped by obesity tier (Low / Medium / High) |

> 📊 See `Digital_Story_Dashboard.pdf` for a static export of the full dashboard.
> 📁 See `Digital_Story_Dashboard.pbix` to open the interactive Power BI file.

---

## Key Findings

The scatter plot trendline is nearly **flat** — indicating **no strong linear correlation** between fast-food restaurant count and adult obesity rate.

- States with the **most** fast-food restaurants (CA, TX, FL) are **not** the most obese
- Several states with **low** restaurant counts still show **high** obesity rates
- Most states cluster in the **medium** obesity tier (35–38%) regardless of restaurant density

**Conclusion:** Fast-food availability alone is not a reliable predictor of obesity. Factors such as income, physical activity levels, and lifestyle likely play a larger role. This analysis demonstrates how data can challenge commonly held assumptions and surface a more accurate picture of public health trends.

---

## Future Work

- Incorporate additional variables: median income, physical activity rates, food desert data
- Extend to a multi-year time series to track trends over time
- Apply regression modeling to quantify the strength of each contributing factor

---

## Files

```
FastFood_Obesity_Analysis/
├── README.md
├── Digital_Story_Dashboard.pbix       ← Interactive Power BI dashboard
├── Digital_Story_Dashboard.pdf        ← Static dashboard export
└── Digital_Story_Report.docx          ← Full written analysis report
```

---

*Individual project — Wendy Calderon · Georgia Gwinnett College · Spring 2025*
