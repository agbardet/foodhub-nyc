# FoodHub NYC — Revenue & Demand Intelligence

> EDA surfacing a 39% customer feedback gap and $6K revenue concentration risk across 1,898 food delivery orders in New York City.

---

## Key Findings

- **38.77% of orders go unrated** — a critical blind spot in satisfaction measurement that directly undermines restaurant partnership decisions and quality control
- **Top-20% orders (>$20) generate 60% of platform revenue** despite representing only 29% of order volume, creating a concentration risk if high-value customers churn
- **Weekend order volume is 2.5× weekday** — the single largest demand pattern in the data, yet weekday revenue remains untapped
- **Weekday delivery is 5.87 minutes slower** than weekend (28.34 min vs 22.47 min), pointing to a staffing or routing inefficiency worth investigating
- **10.54% of orders exceed 60 minutes end-to-end** — the threshold most likely to drive low ratings and customer churn

---

## Business Context

FoodHub is a New York-based multi-restaurant aggregator that earns a **25% margin on orders above $20** and a **15% margin on orders between $5–$20**. This analysis examines 1,898 orders to surface demand patterns, delivery performance bottlenecks, revenue concentration risks, and satisfaction drivers — all directly tied to operational and marketing decisions.

---

## Repository Structure

```
foodhub-nyc/
├── notebooks/
│   └── foodhub_eda.ipynb      # Main analysis notebook (6-act structure)
├── data/
│   └── foodhub_order.csv      # 1,898 orders × 9 columns, no missing values
├── reports/
│   └── figures/               # All charts saved here at dpi=150
├── README.md                  # This file
├── key_findings.md            # Consulting-style findings report
├── data_dictionary.md         # Column definitions and revenue logic
├── portfolio_copy.md          # Website copy for portfolio page
└── requirements.txt           # Pinned Python dependencies
```

---

## Running the Notebook

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Launch Jupyter
jupyter notebook

# 3. Open and run
# notebooks/foodhub_eda.ipynb → Kernel → Restart & Run All
```

All charts are saved automatically to `reports/figures/` on full run.

---

## Dataset

| Property | Value |
|---|---|
| File | `data/foodhub_order.csv` |
| Rows | 1,898 orders |
| Columns | 9 (+ 1 derived: `total_time`) |
| Missing values | None |
| Time period | Not disclosed |
| Source | FoodHub internal order management system |

See [data_dictionary.md](data_dictionary.md) for full column definitions.

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Pandas](https://img.shields.io/badge/Pandas-2.2-blue)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-blue)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8-blue)

---

## Author

**Gary Bardet** — Senior Principal Engineer transitioning into AI/ML Engineering  
[GitHub](https://github.com/agbardet) · [LinkedIn](https://linkedin.com/in/garybardet)
