# Will the Customer Accept the Coupon?

**Module 5 – Practical Application 1**

## Project Overview

This project explores the question: **Will a customer accept a driving coupon?**

Using exploratory data analysis, statistical summaries, and visualizations, I analyze customer behavior to understand what factors influence coupon acceptance. The analysis focuses on comparing customers who accepted coupons versus those who rejected them, with a deep dive into Coffee House coupons.

[View the Jupyter Notebook](coupon_acceptance_analysis.ipynb)

---

## Dataset

**Source:** UCI Machine Learning Repository
**Collection Method:** Amazon Mechanical Turk survey

The survey describes different driving scenarios (destination, time, weather, passengers) and asks whether the driver would accept a coupon. Responses are labeled as:
- **Y = 1** — Accepted the coupon ("Right away" or "Later, before it expires")
- **Y = 0** — Rejected the coupon

**Coupon Types:**
1. Less expensive restaurants (under $20)
2. Coffee houses
3. Carry out & Take away
4. Bars
5. More expensive restaurants ($20–$50)

---

## Summary of Findings

1. **Food coupons outperform beverage coupons** — Carry out (74%) and budget restaurants (71%) have significantly higher acceptance rates than coffee houses (50%) and bars (41%)

2. **Practical needs beat discretionary wants** — Carry out acceptance stays high (65-92%) across all driving contexts because food is a necessity. Coffee acceptance is highly context-dependent.

3. **Coffee house coupons require the right conditions:**
   - Best scenario: No urgent destination + mid-morning (10AM) = 65-82% acceptance
   - Worst scenario: Heading home + evening (6PM/10PM) = 8-37% acceptance

4. **Target audience matters for coffee** — Frequent coffee drinkers accept at 65-82%, while non-visitors accept at only 8-25% regardless of context

5. **Time of day is critical for coffee** — 10AM has 64% acceptance vs. 6PM at 41%. The "Want vs. Need" dynamic means coffee is only appealing when drivers have leisure time.

---

## Recommendations

1. **Prioritize food-based coupons** for maximum acceptance rates across all driver contexts — they work regardless of destination, time, or passenger situation

2. **Time coffee house coupons strategically** — Target mid-morning (10AM) and early afternoon (2PM); avoid evening hours (6PM+) when drivers are focused on getting home

3. **Target coffee coupons based on behavior** — Focus on users with a history of coffee house visits; sending coffee coupons to non-coffee drinkers has only a 19% success rate

4. **Consider destination context** — Avoid sending discretionary coupons (coffee, bars) to drivers heading home; they're focused on arriving, not stopping

---

## Repository Contents

| File | Description |
|------|-------------|
| `coupon_acceptance_analysis.ipynb` | Main Jupyter notebook with analysis and visualizations |
| `data/coupons.csv` | Dataset from UCI Machine Learning Repository |
| `environment.yml` | Conda environment specification |
| `README.md` | Project overview and findings (this file) |

---

## Project Setup

### Prerequisites
- [Conda](https://docs.conda.io/en/latest/miniconda.html) (Miniconda or Anaconda)

### Steps

1. **Clone the repository**
   ```bash
   git clone git@github.com:avidavis/coupon-acceptance-analysis.git
   cd coupon-acceptance-analysis
   ```

2. **Create the conda environment**
   ```bash
   conda env create -f environment.yml
   ```

   If you encounter solver errors, use the classic solver:
   ```bash
   conda env create -f environment.yml --solver=classic
   ```

3. **Activate the environment**
   ```bash
   conda activate coupon-analysis
   ```

4. **Launch Jupyter**
   ```bash
   jupyter notebook
   ```

5. **Open the notebook**

   In your browser, open `coupon_acceptance_analysis.ipynb` and run the cells.

### Manual Setup (alternative)
```bash
conda create -n coupon-analysis python=3.11 pandas numpy matplotlib seaborn jupyter -y --solver=classic
conda activate coupon-analysis
jupyter notebook
```

---

## Evaluation Criteria

This project was completed as part of Module 5 and is evaluated on:

| Criteria | Points |
|----------|--------|
| **Project Organization** — README with findings, well-structured notebook, clean repository | 5 |
| **Syntax and Code Quality** — Correct imports, error-free code, pandas/seaborn competency | 5 |
| **Visualizations** — Appropriate plots, readable labels/titles, proper scaling | 5 |
| **Findings and Insights** — Clear problem statement, statistical interpretation, actionable recommendations | 5 |
| **Total** | **20** |

---

## Key Visualizations

The notebook includes:
- **Bar chart** comparing acceptance rates across all coupon types
- **Heatmaps** showing acceptance by destination × time of day
- **Side-by-side comparison** of Coffee House vs. Carry Out acceptance patterns
- **Bar chart** showing acceptance rate by coffee house visit frequency

Each visualization includes an explanation of why that chart type was chosen for the data.

---

## Author

Created as part of the UC Berkeley ML/AI Professional Certificate program.
