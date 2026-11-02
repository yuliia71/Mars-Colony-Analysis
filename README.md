# 🚀 Mars Colony "Ares VI" Data Analysis

Exploratory data analysis of colony operations in **Python**: from cleaning a raw log with text-formatted values to time-series, ranking, and distribution analysis of resources and energy.

## 1. Project Introduction

This project analyses the operations log of the Mars colony "Ares VI" (2077+) with pandas and Matplotlib. It answers practical questions: how water, food, and oxygen reserves change over time, how energy production compares to consumption, which days were critical, and how often the colony ran an energy deficit.

## 2. Project Overview and Features

**Dataset:** `ares_vi_log.csv` with daily records of record date, colony population, water and food reserves, average oxygen reserve, energy generated, and energy consumed.

**Data preparation:** numeric values are extracted from text fields with regex, dates are converted to `datetime`, missing oxygen values are handled, and a derived metric, net energy balance (generated − consumed), is added.

| Section | Topic |
|---|---|
| 0 | Library versions and data loading, selection of the analysed month |
| 1 | Line charts for the chosen month: water, food, oxygen, net energy balance |
| 2 | Bubble (scatter) chart: energy consumption vs. population, bubble size by oxygen reserve |
| 3 | Average monthly net energy balance |
| 4 | Days with the minimum food reserve |
| 5 | Top 4 days by energy consumption in the chosen month |
| 6 | Energy-deficit days per month (pie chart) |
| 7 | Water-reserve classification (High / Medium / Low) per month (stacked bar chart) |
| 8 | Months where positive-balance days outnumber low-water days |
| 9 | Histogram of daily net energy balance |

## 3. Tech Stack, APIs, and Other Resources

- Python 3.8+
- pandas, NumPy, Matplotlib
- Jupyter Notebook or JupyterLab
- No external APIs

## 4. Getting Started: Setup and Running Instructions

```bash
git clone https://github.com/yuliia71/Mars-Colony-Analysis.git
cd Mars-Colony-Analysis
pip install pandas numpy matplotlib jupyter
jupyter notebook mars_colony_analysis.ipynb
```

1. Place the dataset `ares_vi_log.csv` in the same folder as the notebook.
2. Set the analysed month in section 0 (`P_month`).
3. Run all cells in order: sections 1–9 reuse the columns created in the preprocessing step.
