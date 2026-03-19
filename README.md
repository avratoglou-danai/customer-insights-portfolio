# Customer Insights Portfolio

> End-to-end analyses on Customer Lifetime Value, Customer Acquisition Cost, and Cohort Retention — built with real-world public datasets.

[![Portfolio Site](https://img.shields.io/badge/Portfolio-Live%20Site-b89a74?style=flat-square)](https://yourusername.github.io/customer-insights-portfolio)
[![Python](https://img.shields.io/badge/Python-3.10+-3d2314?style=flat-square&logo=python&logoColor=white)](https://python.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-c4694f?style=flat-square)](LICENSE)

---

## Overview

This repository contains three independent case studies that reflect the type of customer analytics work I do professionally. Each study uses a freely available dataset, follows a reproducible analysis structure, and concludes with business-facing recommendations — not just charts.

The analyses are intentionally end-to-end: from raw data cleaning through to model output, visualisation, and strategic interpretation.

---

## Case Studies

### 01 — Customer Lifetime Value Modelling
**Dataset:** [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail) (541K transactions, UK e-commerce)

Probabilistic LTV estimation using the **BG/NBD + Gamma-Gamma** framework — the industry standard for non-contractual customer value modelling. Customers are segmented into four LTV tiers and mapped against their probability of still being active.

**Key outputs:**
- 12-month predicted LTV per customer
- LTV segmentation (Low / Mid / High / Champions)
- Customer map: LTV vs Probability Alive
- Top 20 customers by predicted revenue

**Tools:** Python, `lifetimes`, `pandas`, `matplotlib`

---

### 02 — Customer Acquisition Cost by Channel
**Dataset:** [Kaggle Marketing Data](https://www.kaggle.com/datasets/jackdaoud/marketing-data) (2,240 customers, multi-channel CRM)

CAC calculated per acquisition channel with LTV:CAC ratio and payback period analysis. Includes a campaign effectiveness breakdown showing which campaigns attracted higher-value customers.

**Key outputs:**
- CAC, LTV:CAC ratio, and payback period by channel
- Efficiency flags per channel (Excellent / Healthy / Marginal / Loss)
- Campaign accept rate and spend lift analysis
- Channel revenue share and budget allocation recommendations

**Tools:** Python, `pandas`, `matplotlib`, `seaborn`

---

### 03 — Cohort Retention & Churn Patterns
**Dataset:** [UCI Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail) (same as Case Study 01)

Month-over-month cohort retention analysis revealing where and when customers churn. The heatmap surfaces the critical drop-off window — the single most actionable output for re-engagement campaign planning.

**Key outputs:**
- Retention heatmap (cohort × months since acquisition)
- Average retention curve with annotated churn inflection point
- Revenue per customer by cohort
- Retention-based segmentation and re-engagement recommendations

**Tools:** Python, `pandas`, `seaborn`, `matplotlib`

---

## Repository Structure

```
customer-insights-portfolio/
│
├── index.html                        ← Portfolio site (GitHub Pages)
├── README.md
│
├── 01-ltv-analysis/
│   ├── notebook.ipynb
│   ├── data/                         ← Place online_retail.xlsx here
│   └── outputs/                      ← Charts and CSV exports
│       ├── bgnbd_validation.png
│       ├── frequency_recency_matrix.png
│       ├── probability_alive_matrix.png
│       ├── ltv_segmentation.png
│       ├── ltv_vs_prob_alive.png
│       ├── top20_customers.png
│       └── ltv_results.csv
│
├── 02-cac-analysis/
│   ├── notebook.ipynb
│   ├── data/                         ← Place marketing_data.csv here
│   └── outputs/
│       ├── cac_by_channel.png
│       ├── ltv_cac_ratio.png
│       ├── payback_period.png
│       ├── campaign_effectiveness.png
│       ├── channel_revenue_distribution.png
│       ├── cac_channel_summary.csv
│       └── campaign_effectiveness.csv
│
└── 03-cohort-analysis/
    ├── notebook.ipynb
    ├── data/                         ← Place online_retail.xlsx here
    └── outputs/
        ├── cohort_retention_heatmap.png
        ├── avg_retention_curve.png
        └── cohort_revenue_heatmap.png
```

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/customer-insights-portfolio.git
cd customer-insights-portfolio
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn lifetimes openpyxl jupyter
```

### 3. Download the datasets

| Dataset | Destination |
|---|---|
| [UCI Online Retail (.xlsx)](https://archive.ics.uci.edu/dataset/352/online+retail) | `01-ltv-analysis/data/online_retail.xlsx` and `03-cohort-analysis/data/online_retail.xlsx` |
| [Kaggle Marketing Data (.csv)](https://www.kaggle.com/datasets/jackdaoud/marketing-data) | `02-cac-analysis/data/marketing_data.csv` |

### 4. Run the notebooks

```bash
jupyter notebook
```

Open each notebook in order and run all cells. Charts and CSV exports are saved automatically to the `outputs/` folder.

---

## Skills Demonstrated

| Area | Details |
|---|---|
| **Data cleaning** | Handling cancellations, missing values, outliers, and encoding issues in raw transactional data |
| **Probabilistic modelling** | BG/NBD and Gamma-Gamma models for LTV prediction |
| **Customer segmentation** | Quartile-based and behaviour-based segmentation with business interpretation |
| **Marketing analytics** | CAC, LTV:CAC ratio, payback period, campaign lift analysis |
| **Cohort analysis** | Retention heatmaps, churn curve annotation, revenue cohort tracking |
| **Data visualisation** | Publication-quality charts with consistent visual identity across all notebooks |
| **Business communication** | Each notebook concludes with findings and recommendations written for non-technical stakeholders |

---

## Tools & Libraries

- **Python 3.10+** — core language
- **pandas** — data manipulation and aggregation
- **lifetimes** — BG/NBD and Gamma-Gamma probabilistic models
- **matplotlib / seaborn** — visualisation
- **openpyxl** — Excel file handling
- **Jupyter Notebook** — reproducible analysis environment

---

## Datasets

Both datasets are publicly available and free to use for non-commercial and educational purposes.

- **UCI Online Retail Dataset** — Daqing Chen, Sai Liang Sain, and Kun Guo, Data mining for the online retail industry: A case study of RFM model-based customer segmentation using data mining, Journal of Database Marketing and Customer Strategy Management, 2012.
- **Kaggle Marketing Dataset** — [jackdaoud/marketing-data](https://www.kaggle.com/datasets/jackdaoud/marketing-data)

---

## Contact

If you have questions about the methodology or want to discuss customer analytics, feel free to reach out.

- **LinkedIn:** [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- **Email:** your@email.com

---

*Built with real data. All analyses are reproducible from the public datasets linked above.*
