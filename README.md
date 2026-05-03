# Coupon Acceptance Analysis — Consumer Behavior EDA

Exploratory data analysis of driving coupon acceptance behavior using survey data from Amazon Mechanical Turk. Identifies the demographic and contextual factors that predict whether a driver will accept a coupon delivered to their mobile device.

## Business Problem

Targeted coupon delivery is only valuable if the coupon is actually used. Understanding which customer segments accept coupons — and under what circumstances — allows businesses to:
- Reduce wasted coupon distribution to unlikely acceptors
- Personalize offers based on customer profile and context
- Increase redemption rates and ROI on promotional spend

## Dataset

| Attribute | Value |
|---|---|
| Source | UCI Machine Learning Repository (via Amazon Mechanical Turk) |
| Records | 12,684 survey responses |
| Features | 25 (demographic, behavioral, contextual) |
| Target | Binary — accepted coupon (Y/N) |
| Overall acceptance rate | ~56.8% |

Features include: destination, passenger type, weather, temperature, time of day, coupon type, expiration, age, income, marital status, children, education, occupation, visit frequency.

## Key Findings

### Who Accepts Coupons?

| Segment | Acceptance Rate | vs. Average |
|---|---|---|
| Age under 30 | ~65% | +8 pts |
| Frequent bar visitors (3+ times/month) | ~77% | +20 pts |
| Coffee house regulars | ~67% | +10 pts |
| Drivers without children | ~59% | +2 pts |
| Drivers with passengers (friends/partner) | ~61% | +4 pts |

### When Are Coupons Accepted?

- **Time of day:** Midday (10am–2pm) shows highest acceptance rates
- **Weather:** Sunny conditions correlate with higher acceptance vs. rainy/snowy
- **Destination:** No urgent destination → significantly higher acceptance
- **Expiration:** 1-day coupons outperform 2-hour coupons in most segments

### Coupon Type Breakdown

- **Coffee House:** Highest volume + moderate acceptance (~50%)
- **Carry Away / Cheap Restaurants:** Highest acceptance rates (~70%+)
- **Bars:** High acceptance among frequent visitors, low among infrequent ones
- **Expensive Restaurants:** Lowest overall acceptance (~45%)

## Analytical Approach

1. **Data Quality** — Identified and handled missing values (car column: 99% missing → dropped; Bar/CoffeeHouse/etc.: imputed with mode)
2. **Univariate Analysis** — Distribution of each feature, acceptance rate by category
3. **Bivariate Analysis** — Cross-tabulation of demographics vs. acceptance
4. **Segmentation** — Behavioral segmentation (bar frequency, coffee house frequency) crossed with demographics
5. **Visualization** — Heatmaps, bar charts, proportion plots for all key comparisons

## Project Structure

```
coupon-acceptance-eda/
├── Coupon_Acceptance.ipynb    # Full analysis notebook
└── data/
    └── coupons.csv            # Survey dataset
```

## Quick Start

```bash
git clone https://github.com/BedirhanUlas/coupon-acceptance-eda.git
cd coupon-acceptance-eda
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Coupon_Acceptance.ipynb
```

## Tech Stack

`Python` · `pandas` · `NumPy` · `Matplotlib` · `Seaborn`

## Business Recommendations

1. **Bar coupons:** Target drivers who visit bars 3+ times/month and are over 25 — acceptance rate nearly doubles vs. infrequent visitors
2. **Coffee house coupons:** High potential for young professionals (under 30) traveling alone to work
3. **Avoid:** Sending expensive restaurant coupons to families with children — lowest acceptance segment
4. **Timing:** Schedule delivery for midday rather than morning rush or late evening

## License

MIT
