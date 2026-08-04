# Telecom Tariff Analysis — Code Tariff Pilot

An Excel-based business analysis exercise: evaluating whether a telecom company should migrate eligible subscribers to a new flat-rate "Code" tariff, based on a 9,999-subscriber dataset.

## About this project

This started as an assignment given by an instructor: a raw subscriber dataset and a business question. I treated it as a self-directed mini case study — deciding myself how to break the problem down.

It's a small project, but everything in it (the formulas, the pivot tables, the charts, the written analysis) is my own work, done to practice a realistic analyst workflow: understand the business question → build the supporting data → summarize it → say what it means → make a recommendation.

![Summary tab — the case and my approach](images/summary.png)



## The business question

A telecom company wants to pilot a new flat-rate tariff, "Code," priced at 20 AZN/month. Subscribers qualify for the pilot if they meet three usage conditions (minimum call minutes, an internet-usage range, and any SMS use). The question: what would happen — to subscriber counts and to revenue — if eligible subscribers were migrated to this new tariff?

## What's in the file

The workbook has four tabs:

| Tab | What it contains |
|---|---|
| **Summary** | The business case as given, plus my own outline of how I approached the analysis |
| **Dashboard** | A one-page summary: key numbers, a summary table by tariff, two charts, and my written recommendation |
| **Analysis** | The full working analysis — ten sub-tasks, each with a pivot table or chart, plus a short written takeaway under each one |
| **Raw** | The original subscriber data, plus two columns I added: eligibility for Code (`Code_Tariff_Eligibility`) and the resulting revenue impact per subscriber (`Revenue_Difference`) |


## Key finding

Of 9,999 subscribers, about 2,594 (26%) meet the usage criteria for Code. But migrating all of them to the flat 20 AZN rate would **reduce** total revenue by roughly 78,700 AZN/month — because a meaningful share of eligible subscribers currently pay more than 20 AZN, and the flat rate would cut their bill. The effect is nearly identical across all four existing tariffs, meaning tariff type doesn't predict who benefits — the subscriber's *current spending level* does.

My takeaway: the usage-based eligibility rule alone isn't a safe way to select migration candidates. Adding a revenue floor (e.g. only offering Code to subscribers currently paying under ~20–25 AZN) would target subscribers who'd actually benefit, without giving away revenue from those who already pay more.

## Tools / skills used

- Excel pivot-style summary tables (`SUMIFS`, `COUNTIFS`)
- Conditional logic (`IF`, `AND`) for eligibility flags and revenue-impact calculations
- Bar chart, Histogram, and Box-and-Whisker chart
- A one-page dashboard layout summarizing the analysis for a non-technical reader

## How to view it

Download `Telecom_Dichotomy_Designing_Optimal_Product_Sabina_Ismayilova.xlsx` and open it in Excel. Start with the **Dashboard** tab for the summary, or **Summary** for the full context and my approach. The **Analysis** tab has the full detail if you want to see the underlying work.

## Repository Structure

├── README.md
├── Telecom_Dichotomy_Designing_Optimal_Product_Sabina_Ismayilova.xlsx
└── images/
├── dashboard.png
├── bar-chart.png
├── histogram.png
├── boxwhisker.png
└── summary.png

## Screenshots

**Dashboard overview**
![Dashboard](images/dashboard.png)

**Eligible-subscriber revenue by tariff**
![Bar chart](images/bar-chart.png)

**Distribution of subscriber revenue**
![Histogram](images/histogram.png)

**Revenue-difference spread by tariff**
![Box-and-whisker chart](images/boxwhisker.png)

---
Sabina Ismayilova
