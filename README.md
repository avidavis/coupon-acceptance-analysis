# Will the Customer Accept the Coupon?

## Overview
This project explores a survey dataset of driving scenarios and asks one question: will a customer accept a coupon. The analysis compares customers who accepted a coupon versus those who rejected it, using exploratory data analysis, statistical summaries, and clear visualizations.

The notebook focuses on one coupon group and highlights which factors most strongly relate to acceptance, such as context, passenger situation, time, weather, and prior venue behavior.

## Dataset
Source: UCI Machine Learning Repository
Collection method: Amazon Mechanical Turk survey
Target label:
1. Y = 1 means the customer accepted the coupon (right away or later before it expires)
2. Y = 0 means the customer did not accept the coupon

Coupon types in the dataset include:
1. Less expensive restaurants under 20
2. Coffee houses
3. Carryout and takeaway
4. Bars
5. More expensive restaurants 20 to 50

## Key Questions
1. What is the overall acceptance rate for the selected coupon group
2. Which customer attributes differ most between acceptance and rejection
3. Which driving context variables differ most between acceptance and rejection
4. What actionable recommendations follow from these differences

## Summary of Findings
Add 3 to 5 short bullets here after you run the notebook. Keep them specific and tied to plots.
Example format:
1. Finding 1
2. Finding 2
3. Finding 3

## Recommendations
Add 2 to 4 actions that a business could take based on the findings.
Example format:
1. Recommendation 1
2. Recommendation 2
3. Recommendation 3

## Repository Contents
1. Practical_Application_1.ipynb
2. data/coupons.csv

## How to Run Locally
1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies
4. Run Jupyter and open the notebook

Example commands:

```bash
git clone https://github.com/YOUR_USERNAME/coupon-acceptance-analysis.git
cd coupon-acceptance-analysis

python3 -m venv .venv
source .venv/bin/activate

pip install pandas numpy matplotlib seaborn jupyter

jupyter notebook
