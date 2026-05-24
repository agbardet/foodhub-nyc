# Data Dictionary — FoodHub Order Dataset

**Source:** FoodHub internal order management system  
**Snapshot period:** Not disclosed (used as-is for analysis)  
**Rows:** 1,898 orders | **Columns:** 9 | **Missing values:** None

---

| Column | Type | Description | Notes |
|---|---|---|---|
| `order_id` | int64 | Unique identifier for each order | Range: 1,477,147 – 1,478,444 |
| `customer_id` | int64 | Unique identifier for the customer who placed the order | 1,200 unique customers across 1,898 orders; repeat customers exist |
| `restaurant_name` | object | Name of the restaurant fulfilling the order | 178 unique restaurants |
| `cuisine_type` | object | Cuisine category of the restaurant | 14 categories: American, Japanese, Italian, Chinese, Mexican, Indian, Middle Eastern, Mediterranean, Thai, French, Southern, Korean, Spanish, Vietnamese |
| `cost_of_the_order` | float64 | Total cost of the order in USD | Range: $4.47 – $35.41; median ~$14.14; 29.24% exceed $20 |
| `day_of_the_week` | object | Whether the order was placed on a weekday or weekend | Two values: `"Weekday"` (547 orders) or `"Weekend"` (1,351 orders) |
| `rating` | object | Customer rating out of 5 submitted after delivery | **Mixed type:** values are `"3"`, `"4"`, `"5"` (as strings), or `"Not given"` (736 orders, 38.77%). Cast to numeric before any rating analysis; filter out `"Not given"` rows |
| `food_preparation_time` | int64 | Minutes from order confirmation to courier pickup | Range: 20–35 min; mean 27.37 min; near-uniform distribution |
| `delivery_time` | int64 | Minutes from courier pickup to customer drop-off | Range: 15–33 min; mean 24.16 min; right-skewed |

---

## Derived Column

| Column | Type | Description | Created in |
|---|---|---|---|
| `total_time` | int64 | `food_preparation_time + delivery_time` — end-to-end fulfillment time in minutes | Act 4 of the notebook |

---

## Revenue Logic

FoodHub earns a margin on each order (not included as a column — calculated analytically):

- **25% margin** on orders where `cost_of_the_order > 20`
- **15% margin** on orders where `5 <= cost_of_the_order <= 20`
- Orders below $5 are excluded from revenue calculation (edge case; none present in this dataset)
