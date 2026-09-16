# 🍔 Food Delivery Order Analytics

**EDA of 12,000 food delivery orders across 12 Indian cities — uncovering what actually drives delivery delays and restaurant performance.**

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-4C72B0)](https://seaborn.pydata.org/)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen)]()

**Author:** Uday Garg — Data Analytics | [LinkedIn](https://www.linkedin.com/in/uday-garg-b08374295) · [GitHub](https://github.com/Udaygarg0034)

---

## 📌 Overview

This project analyzes **12,000 order-level records from a simulated food delivery platform** spanning October 2025 to September 2026 across 12 major Indian cities. The goal was to clean messy real-world data, engineer useful features, and use simple group comparisons to find what actually affects delivery time and restaurant performance — then turn those findings into business recommendations.

## 🎯 Business Questions

| # | Question |
|---|---|
| 1 | Does traffic level affect delivery time? |
| 2 | Does weather (rain/fog) cause a noticeable delay? |
| 3 | How does distance relate to delivery time? |
| 4 | Which cities drive the most order volume? |
| 5 | Does restaurant cost category relate to rating or delivery speed? |

## 🔍 Key Findings

| Finding | What the data shows |
|---|---|
| **Traffic level has the biggest impact on delivery time** | Average time rises from ~24 min (Low/Medium traffic) to ~32 min (High) to ~39 min (Jam) |
| **Rainy weather adds noticeable delay** | Orders in rain average ~36 min vs ~26 min in clear weather — about 10 minutes slower |
| **Distance has a moderate relationship with delivery time** | Correlation of 0.46 — distance matters, but traffic and weather matter just as much |
| **Restaurant price does not predict rating** | Budget, Mid-Range, Premium, and Luxury restaurants all average within ~0.15 rating points of each other |
| **Gurugram, Kolkata & Jaipur lead order volume** | Highest order counts of the 12 cities in the dataset |

> 💡 **Business takeaway:** Delivery ETAs should account for traffic and weather conditions, not just distance — and marketing shouldn't assume "premium = better," since price doesn't track with rating in this data.


## 🛠️ Tech Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Jupyter Notebook`

## 🧭 Methodology

1. **Data Cleaning** — resolved duplicate records, mixed-format ratings (`"4.1/5"`, `"NEW"`, `"-"`), comma-formatted costs, negative vote values, and inconsistent text casing
2. **Feature Engineering** — derived time-based features (hour, day, weekend flag), cost/rating tiers, and meal-slot segments from raw timestamps
3. **Exploratory Data Analysis** — distribution and category-level comparisons using histograms, boxplots, and bar charts
4. **Simple Group Comparisons** — used `groupby()` and `.mean()` to compare delivery time and rating across traffic levels, weather conditions, and cost categories, plus a basic correlation check between distance and delivery time
5. **Business Synthesis** — translated the observed patterns into five prioritized, actionable recommendations

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

- Formal statistical testing (t-tests, ANOVA) once comfortable with inferential statistics
- Predictive model for delivery time estimation
- Interactive dashboard (Streamlit/Power BI) for live monitoring

---

⭐ If you found this project useful, consider giving it a star — feedback and suggestions are welcome via Issues.
