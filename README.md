
---

# ENIAC A/B Testing & Discounts Analysis

This repository contains code and analysis for:

* A/B testing on the **Shop Now** button variants (A, B, C, D)
* Statistical analysis of clicks, visits, and returns
* Discount impact analysis on product sales and revenue
* Visualization of discount percentages and revenue grouped by discount and price categories

---

## Project Overview

The goal is to analyze user behavior in an A/B test of different **Shop Now** button versions and understand the effects of discounts on product sales and revenue.

---

## Table of Contents

* [A/B Testing Analysis](#ab-testing-analysis)
* [Discounts Analysis](#discounts-analysis)
* [Visualizations](#visualizations)
* [Usage](#usage)
* [Dependencies](#dependencies)

---

## A/B Testing Analysis

The variants A, B, C, and D were tested using click and visit data. Statistical testing was done using the chi-squared test to check if click behavior differs between variants.

* Chi-squared contingency tables were created based on clicks and no-clicks.
* P-values were computed to determine statistical significance.
* Pairwise tests identified which variants had significant differences.
* Click-through rates (CTR) were calculated for each variant.

---

## Discounts Analysis

Using product price and orderline data:

* Calculated absolute discount and discount percentages per product purchase.
* Filtered for valid discounts (discount ≥ 0).
* Counted discounted vs. non-discounted products and their respective revenue contributions.
* Categorized discounts into ranges (e.g., 0%, 1-10%, ..., 91-100%) to analyze distribution and revenue contribution.
* Grouped and visualized revenue and quantity by discount groups and price categories.
* Explored different price category groupings to understand sales and revenue by price ranges.

---

## Visualizations

* Histogram of discount percentages.
* Bar charts for revenue and quantity by discount groups.
* Bar charts for revenue and quantity by price categories.
* Faceted bar plots of sales count by combined price and discount groups.

---

## Example Outputs

* **Discounted products:** 49,404
* **Non-discounted products:** 2,256
* **Revenue from discounts:** \~6.68M €
* **Revenue without discounts:** \~221K €
* \~96% of products sold with discounts, generating \~97% of revenue.

---

## How to Run

1. Install dependencies:

   ```bash
   pip install pandas numpy matplotlib seaborn scipy
   ```

2. Load your data files (CSV for orders, products, orderlines).

3. Run the provided scripts/notebooks to reproduce analyses and visualizations.

---

## Dependencies

* Python 3.x
* pandas
* numpy
* matplotlib
* seaborn
* scipy

---

