# Medicaid Pharmaceutical Spending Analysis

A Tableau-driven healthcare analytics project analyzing Medicaid pharmaceutical reimbursement, high-cost specialty drugs, population-adjusted spending, and state-level cost variation.

This project investigates where Medicaid pharmaceutical cost pressure is concentrated and identifies opportunities for more targeted cost-management strategies.

---

## Project Overview

Medicaid is a joint federal and state program that provides health coverage to millions of low-income Americans, including children, pregnant women, seniors, and people with disabilities.

Because Medicaid is publicly funded and serves vulnerable populations, improving pharmaceutical spending efficiency is important. The goal of this project was to identify whether Medicaid cost pressure is primarily driven by high prescription volume, high-cost specialty drugs, or state-level reimbursement variation.

The final analysis was built in Tableau using Medicaid pharmaceutical reimbursement data and U.S. Census population data.

---

## Business Problem

Medicaid pharmaceutical costs are increasing, but the source of spending pressure is not always obvious from raw prescription volume.

A drug can appear frequently in the dataset without being the largest financial burden. Similarly, states with larger total reimbursement may not always be the highest-cost states after adjusting for population.

This project focuses on answering:

> Where is Medicaid pharmaceutical spending pressure actually concentrated?

The analysis separates:

* High-volume drugs vs. high-cost drugs
* Medicaid vs. non-Medicaid reimbursement
* Total spending vs. per-capita spending
* State-level spending differences after population normalization

---

## Data Sources

This project uses public government data sources:

1. **Medicaid Pharmaceutical Spending Data**

   * Drug name
   * National Drug Code
   * Number of prescriptions
   * Units reimbursed
   * Medicaid amount reimbursed
   * Non-Medicaid amount reimbursed
   * Total reimbursement
   * State
   * Reporting period

2. **U.S. Census Population Data**

   * 2024 state population estimates
   * Used to normalize reimbursement by population

The Medicaid dataset was joined with Census population data to calculate population-adjusted spending metrics.

---

## Tools Used

* Tableau
* Excel
* Healthcare Analytics
* Data Visualization
* Public Policy Analysis
* Medicaid Reimbursement Analysis

---

## Data Preparation

The project involved cleaning and preparing both Medicaid and population datasets.

Key preparation steps included:

* Loaded Medicaid data into Tableau
* Cleaned data types for fields such as NDC, labeler code, product code, year, and quarter
* Converted year and quarter fields into a usable date field
* Cleaned Census population data in Excel
* Added two-letter state abbreviations to match Medicaid state codes
* Removed unnecessary population-year columns
* Joined Medicaid data with Census population data using state abbreviation

---

## Calculated Fields

The analysis used calculated fields to normalize reimbursement across states and compare spending more accurately.

### Medicaid Reimbursement per Capita

```text
SUM([Medicaid Amount Reimbursed]) / SUM([2024 Population])
```

### Non-Medicaid Reimbursement per Capita

```text
SUM([Non Medicaid Amount Reimbursed]) / SUM([2024 Population])
```

### Total Reimbursement per Capita

```text
SUM([Total Amount Reimbursed]) / SUM([2024 Population])
```

These fields were used to identify high-cost drugs and high-spending states relative to population size.

---

## Tableau Dashboard Views

The project includes several Tableau visualizations:

### 1. Top 15 Product Units Reimbursed

Identifies the highest-volume reimbursed drugs by product units.

This view showed that many high-volume drugs were common medications such as IV fluids, antibiotics, diabetes drugs, and allergy medications.

### 2. Top 15 Drugs per Capita

Ranks drugs by reimbursement per capita.

This view helped identify high-cost specialty drugs that create stronger financial pressure despite not always having the highest prescription volume.

### 3. Medicaid vs. Non-Medicaid Reimbursement per Capita

Compares Medicaid and non-Medicaid reimbursement responsibility for the highest-cost drugs.

This showed that Medicaid carries most of the reimbursement burden for many top high-cost drugs.

### 4. Top 15 States Spending per Capita

Ranks states by reimbursement per capita.

This helped identify states where Medicaid pharmaceutical spending is disproportionately high relative to population.

### 5. State-Level Geographic Spending Map

Maps reimbursement per capita by state to identify regional spending concentration.

The analysis showed concentration in the Northeast, with additional Southern outliers.

### 6. Population vs. Total Reimbursement Scatter Plot

Compares state population against total Medicaid reimbursement.

The trend showed a strong relationship between population and total reimbursement, supporting the need for per-capita analysis.

---

## Key Findings

### 1. High prescription volume is not the main cost problem

The highest-volume drugs were mostly common, lower-cost medications. This showed that prescription count alone is not enough to identify the largest financial pressure points.

### 2. Specialty drugs drive stronger reimbursement pressure

High-cost specialty drugs such as Vraylar, Cabenuva, and Trikafta created greater reimbursement pressure than many high-volume generic drugs.

### 3. Medicaid carries most of the cost burden

For many high-cost drugs, non-Medicaid reimbursement was minimal, meaning Medicaid was responsible for most of the financial burden.

### 4. State-level cost concentration matters

States such as New York, Kentucky, Connecticut, Louisiana, and West Virginia showed high Medicaid reimbursement per capita.

### 5. Per-capita analysis is more useful than total spending alone

Larger states naturally have higher total reimbursement. Normalizing by population helped reveal states with disproportionate spending relative to size.

---

## Business Recommendations

Based on the analysis, Medicaid should focus on targeted cost-control strategies rather than broad spending reductions.

Recommended actions include:

* Prioritize rebate negotiation for high-cost specialty drugs
* Explore supplemental rebate agreements
* Use prior authorization where appropriate
* Review therapeutic alternatives when medically reasonable
* Focus on reimbursement impact, not prescription volume alone
* Investigate high-spending states for regional policy patterns
* Apply state-level or regional cost-management strategies

---

## Project Structure

Recommended GitHub structure:

```text
Medicaid-Pharmaceutical-Spending-Analysis/
│
├── README.md
├── paper/
│   └── medicaid_pharmaceutical_spending_analysis.pdf
├── dashboard/
│   └── tableau_dashboard_link.txt
├── images/
│   ├── top_15_drugs_per_capita.png
│   ├── top_15_states_per_capita.png
│   ├── medicaid_vs_non_medicaid.png
│   └── state_spending_map.png
└── data/
    └── data_sources.md
```

---

## Portfolio Summary

Built a Tableau-driven healthcare analytics project analyzing Medicaid pharmaceutical spending. The analysis showed that cost pressure is driven less by prescription volume and more by high-cost specialty drugs and state-level reimbursement concentration. The project used per-capita reimbursement metrics, Medicaid vs. non-Medicaid comparisons, and state-level dashboards to recommend targeted rebate negotiation, prior authorization, and regional cost-management strategies.

---

## Author

Yajat Mehta
Data Analytics & AI
GitHub: mehtaversehq
