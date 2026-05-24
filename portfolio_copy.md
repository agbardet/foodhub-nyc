# Portfolio Copy — FoodHub NYC

> Use this file to populate your GitHub Pages portfolio page and project cards.

---

## Project Card

**Title:** FoodHub NYC — Revenue & Demand Intelligence

**One-line description:**
EDA surfacing a 39% customer feedback gap and $6K revenue concentration risk across 1,898 food delivery orders in New York City.

**Three bullet highlights:**
- Identified that 38.77% of orders go unrated, creating a blind spot in satisfaction measurement that directly impacts restaurant partnership decisions
- Found that top-20% orders (>$20) generate 60% of platform revenue — a concentration risk requiring strategic diversification
- Quantified a 5.87-minute weekday delivery penalty pointing to a staffing optimization opportunity worth investigating

**Tags:** `Python` `Pandas` `Seaborn` `Matplotlib` `EDA` `Business Analytics`

---

## Extended Project Blurb

FoodHub is a New York-based multi-restaurant food delivery aggregator that earns margins of 15–25% per order depending on order value. This exploratory data analysis examines 1,898 orders across 178 restaurants and 14 cuisine categories to answer the business questions that matter most: where is revenue concentrated, what drives customer satisfaction, and where are the operational gaps that cost money?

The analysis surfaces three compounding risks in FoodHub's current model. First, a 39% unrated order rate means the platform is flying blind on quality — unable to enforce performance standards or detect churn signals early. Second, revenue is structurally concentrated: the top 5 restaurants handle one-third of all orders, and the top 20% of orders by value generate 60% of revenue. Third, weekday demand is dramatically under-served at just 40% of weekend volume, representing a direct growth lever. The notebook closes with five prioritized, evidence-backed recommendations mapped directly to these findings.

---

## GitHub Pages Project Page (index.html stub)

Paste this into a `docs/index.html` if you want a hosted project page via GitHub Pages:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>FoodHub NYC — Revenue & Demand Intelligence | Gary Bardet</title>
  <style>
    body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif; max-width: 860px; margin: 60px auto; padding: 0 24px; color: #1a1a1a; line-height: 1.65; }
    h1 { font-size: 2rem; margin-bottom: 0.25rem; }
    .subtitle { color: #555; font-size: 1.1rem; margin-bottom: 2rem; }
    .tags span { background: #f0f0f0; border-radius: 4px; padding: 3px 10px; margin-right: 6px; font-size: 0.85rem; }
    .findings { background: #f9f9f9; border-left: 4px solid #E8603C; padding: 16px 20px; border-radius: 4px; margin: 2rem 0; }
    .cta a { display: inline-block; background: #1a1a1a; color: #fff; padding: 10px 22px; border-radius: 6px; text-decoration: none; margin-right: 12px; }
  </style>
</head>
<body>
  <h1>FoodHub NYC — Revenue & Demand Intelligence</h1>
  <p class="subtitle">EDA surfacing a 39% customer feedback gap and $6K revenue concentration risk across 1,898 food delivery orders in New York City.</p>
  <div class="tags">
    <span>Python</span><span>Pandas</span><span>Seaborn</span><span>Matplotlib</span><span>EDA</span><span>Business Analytics</span>
  </div>
  <div class="findings">
    <strong>Key findings:</strong>
    <ul>
      <li>38.77% of orders go unrated — a satisfaction measurement blind spot</li>
      <li>Top-20% orders (&gt;$20) generate 60% of platform revenue</li>
      <li>Weekend volume is 2.5× weekday — an untapped weekday growth opportunity</li>
      <li>Weekday delivery is 5.87 min slower, pointing to a staffing gap</li>
      <li>10.54% of orders exceed 60 min end-to-end — the churn-risk threshold</li>
    </ul>
  </div>
  <p>FoodHub is a NYC multi-restaurant food delivery aggregator earning 15–25% margins per order. This analysis examines 1,898 orders to surface demand patterns, delivery bottlenecks, revenue concentration risks, and satisfaction drivers — backed by five prioritized operational recommendations.</p>
  <div class="cta">
    <a href="https://github.com/agbardet/foodhub-nyc">View on GitHub</a>
    <a href="notebooks/foodhub_eda.ipynb" style="background:#E8603C;">Open Notebook</a>
  </div>
</body>
</html>
```

---

## Resume / LinkedIn Bullet Points

- Conducted end-to-end EDA on 1,898 food delivery orders, surfacing a 39% rating gap and revenue concentration risk ($6K total; 29% of orders → 60% of revenue) with five evidence-backed strategic recommendations
- Built portfolio-quality visualizations in Seaborn/Matplotlib with business-narrative framing; quantified a 5.87-min weekday delivery underperformance and 10.54% SLA breach rate
