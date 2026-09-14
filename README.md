# 🍔 Food Delivery Order Analytics

**End-to-end EDA & statistical analysis of 12,000 food delivery orders across 12 Indian cities, uncovering the real drivers of delivery delays and restaurant performance.**

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)](https://seaborn.pydata.org/)
[![SciPy](https://img.shields.io/badge/SciPy-Hypothesis%20Testing-8CAAE6?logo=scipy&logoColor=white)](https://scipy.org/)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()

**Author:** Uday Garg — Data Analytics | 
[LinkedIn](www.linkedin.com/in/uday-garg-b08374295) · [GitHub](https://github.com/Udaygarg0034)

---

## 📌 Overview

This project analyzes **12,000 order-level records from a simulated food delivery platform** spanning October 2025 to September 2026 across 12 major Indian cities. The goal was to move beyond surface-level charts and use **statistical hypothesis testing** to identify which operational factors — traffic, weather, distance, pricing — actually drive delivery delays and customer ratings, then translate those findings into business recommendations.

## 🎯 Business Questions

| # | Question |
|---|---|
| 1 | Does traffic level significantly affect delivery time? |
| 2 | Does weather (rain/fog) cause a measurable delay? |
| 3 | How strongly does distance correlate with delivery time? |
| 4 | Which cities drive the most order volume? |
| 5 | Does restaurant cost category predict rating or delivery speed? |

## 🔍 Key Findings

| Finding | Statistical Evidence |
|---|---|
| **Traffic is the single strongest delay driver** | ANOVA: F = 2379.47, p < 0.001 |
| **Rain adds ~10 minutes per delivery** (36.2 min vs 26.0 min) | t-test: t = 40.48, p < 0.001 |
| **Distance moderately correlates with delivery time** | Pearson r = 0.46, p < 0.001 |
| **Online ordering is linked to table booking availability** | Chi-square: χ² = 13.94, p < 0.001 |
| **Gurugram, Kolkata & Jaipur lead order volume** | ~1,170 / ~1,150 / ~1,140 orders respectively |
| **Price does NOT predict rating or speed** | All cost tiers cluster within 0.16 rating pts & 0.4 min |

> 💡 **Business takeaway:** Delivery ops should weight *traffic and weather conditions* into ETA calculations far more than distance alone — and marketing should stop assuming "premium = better," since the data shows no such link.

## 📊 Sample Visuals

| Delivery Time by Traffic Level | Correlation Matrix |
|---|---|
| ![Traffic Boxplot](images/traffic_boxplot.png) | ![Heatmap](images/correlation_heatmap.png) |

*(export your charts as PNGs into `/images` — see instructions below)*

## 🛠️ Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `SciPy` · `Jupyter Notebook`

## 🧭 Methodology

1. **Data Cleaning** — resolved duplicate records, mixed-format ratings (`"4.1/5"`, `"NEW"`, `"-"`), comma-formatted costs, negative vote values, and inconsistent text casing
2. **Feature Engineering** — derived time-based features (hour, day, weekend flag), cost/rating tiers, and meal-slot segments from raw timestamps
3. **Univariate & Bivariate EDA** — distribution analysis and category-level comparisons using histograms, boxplots, and regression plots
4. **Statistical Hypothesis Testing** — independent t-test, one-way ANOVA, Pearson correlation, and Chi-square test of independence
5. **Business Synthesis** — translated statistical output into five prioritized, actionable recommendations

## 📂 Repository Structure

```
food-delivery-analytics/
├── data/
│   └── food_delivery_analytics_data.csv
├── notebook/
│   └── food_delivery_analytics.ipynb
├── images/
│   └── (exported chart PNGs)
├── README.md
└── requirements.txt
```

## ▶️ How to Run

```bash
git clone https://github.com/Udaygarg0034/food-delivery-analytics.git
cd food-delivery-analytics
pip install -r requirements.txt
jupyter notebook notebook/food_delivery_analytics.ipynb
```

## 📈 Dataset

12,000 orders · 19 features · 450 restaurants · 12 cities · Oct 2025 – Sep 2026
Columns include `order_date`, `city`, `cuisines`, `cost_for_two`, `rating`, `distance_km`, `traffic_level`, `weather_condition`, `delivery_time_min`, and more.

## 🔮 Future Improvements

- Predictive model for delivery time estimation (regression)
- Restaurant churn/rating decline early-warning signals
- Interactive dashboard (Streamlit/Power BI) for live monitoring

---

⭐ If you found this project useful, consider giving it a star — feedback and suggestions are welcome via Issues.
