# Key Findings — FoodHub NYC Order Analysis

**Dataset:** 1,898 food delivery orders | **Scope:** NYC multi-restaurant aggregator  
**Analysis type:** Exploratory Data Analysis (Python / Pandas / Seaborn)

---

## Executive Summary

FoodHub's $6,166 net revenue is structurally concentrated: 29% of orders (those above $20) generate 60% of income, and the top 5 restaurants account for roughly 1 in 3 orders. At the same time, 38.77% of customers submit no rating, creating a persistent blind spot in quality measurement. Correcting these three risks — revenue concentration, restaurant concentration, and feedback absence — represents the clearest path to sustainable revenue growth.

---

## 1. Data Quality

| Metric | Value |
|---|---|
| Total orders | 1,898 |
| Missing values | None |
| Unrated orders | 736 (38.77%) |

The dataset is clean with no null values across all 9 columns. However, the `rating` field is stored as a mixed-type object — containing numeric strings (`"3"`, `"4"`, `"5"`) and the literal string `"Not given"` — requiring type conversion before any satisfaction analysis.

**Business implication:** A 39% unrated rate is not a data quality issue — it is a product failure. Without post-delivery rating prompts, FoodHub cannot reliably identify underperforming restaurants, cannot set performance-based partnership terms, and cannot detect satisfaction trends before they manifest as churn.

---

## 2. Demand & Volume Patterns

### Day-of-week split
Weekend orders (1,351) outpace weekday orders (547) by **2.5:1**. This is the dominant demand pattern in the dataset. FoodHub's operational model — staffing, courier availability, restaurant SLA agreements — is effectively optimized for weekend volume only.

### Cuisine preference
American cuisine leads overall demand and holds a dominant position on weekends (415 orders, 30.72% of weekend volume). Japanese cuisine ranks second. These two categories should anchor any restaurant recruitment or promotional strategy.

### Customer concentration
The top 3 customers by order frequency (IDs 52832, 47440, 83287) placed 13, 10, and 9 orders respectively. This group represents loyal, high-LTV customers — strong candidates for retention incentives before they churn to a competitor.

---

## 3. Delivery Performance

| Metric | Weekday | Weekend | Delta |
|---|---|---|---|
| Mean delivery time | 28.34 min | 22.47 min | **5.87 min slower** on weekdays |
| Orders >60 min total | — | — | **200 orders (10.54%)** |

Weekend delivery is meaningfully faster despite higher order volume — likely because couriers are more densely deployed on weekends. The 5.87-minute weekday penalty is substantial at scale and points to a staffing or routing gap that operational intervention could close.

**SLA risk:** 10.54% of orders exceed 60 minutes end-to-end (food preparation + delivery). These are the orders most likely to generate low ratings or no rating at all. An automated SLA alert at 45 minutes would allow proactive customer communication before experience deteriorates.

---

## 4. Revenue Analysis

| Segment | Order count | Revenue | Share of revenue |
|---|---|---|---|
| Orders >$20 (25% margin) | 555 (29.24%) | $3,688.73 | **59.8%** |
| Orders $5–$20 (15% margin) | 1,343 (70.76%) | $2,477.58 | 40.2% |
| **Total** | **1,898** | **$6,166.30** | 100% |

The asymmetry is stark: less than one-third of orders produce nearly two-thirds of revenue. This makes the high-value order segment disproportionately important to protect. Any initiative that grows average order value above the $20 threshold — bundling, upsells, premium restaurant recruitment — has an outsized revenue impact.

---

## 5. Restaurant Concentration

| Restaurant | Orders | Promo eligible? |
|---|---|---|
| Shake Shack | 219 | Yes |
| The Meatball Shop | 132 | Yes |
| Blue Ribbon Sushi | 119 | Yes |
| Blue Ribbon Fried Chicken | 96 | Yes |
| Parm | 68 | No |

The top 5 restaurants handle approximately 634 orders — **33.4% of all volume**. Critically, the same 4 restaurants that drive the most orders are also the ones with both high rating volume (>50 ratings) and high average ratings (>4.0), meaning quality and popularity are co-located at the top.

**Concentration risk:** FoodHub's revenue is meaningfully exposed to the operational stability of a small number of partners. A closure, contract renegotiation, or quality decline at Shake Shack alone would affect ~11.5% of all orders.

---

## 6. Satisfaction Drivers

Analysis of rated orders (1,162 of 1,898) reveals two meaningful relationships:

- **Order cost → rating (positive):** Higher-cost orders tend to receive higher ratings. Customers spending more likely have higher expectations for restaurant quality, and the premium restaurants they choose tend to deliver.
- **Delivery time → rating (negative):** Longer delivery times are associated with lower ratings. This is the clearest operational lever for improving satisfaction: faster delivery directly predicts better ratings.
- **Preparation time → rating:** No meaningful relationship observed. Customers appear tolerant of kitchen preparation time; the dissatisfaction occurs during the delivery leg.

---

## 7. Strategic Recommendations

### P0 — Close the feedback gap
**38.77% unrated orders is the highest-priority issue.** Implement a mandatory or prominently nudged one-tap rating prompt immediately post-delivery. Target: reduce unrated rate below 15% within 90 days. Without this, all satisfaction analysis is structurally unreliable.

### P1 — Activate weekday demand
Weekend volume is 2.5× weekday. Targeted weekday promotions — time-limited discounts, cuisine-specific offers, loyalty multipliers — could materially grow revenue without adding weekend operational complexity.

### P2 — Diversify the restaurant portfolio
The top 5 restaurants representing one-third of volume is a supply-side concentration risk. Recruit 10–15 high-quality restaurants across underrepresented cuisine categories (Mexican, Indian, Thai) to reduce dependency and broaden customer acquisition.

### P3 — Protect and grow the >$20 segment
High-value orders (>$20) generate 60% of revenue. Priority initiatives: recruit premium restaurants, offer loyalty perks for high-spend customers, and test bundling or add-on upsells that push orders over the $20 margin threshold.

### P4 — Set automated 60-minute SLA alerts
10.54% of orders exceed 60 minutes end-to-end. Implement an automated alert at 45 minutes (the pre-breach warning window) enabling proactive outreach — a discount voucher, an ETA update, a direct message — before the experience fails. This is a high-ROI operational change with low implementation cost.
