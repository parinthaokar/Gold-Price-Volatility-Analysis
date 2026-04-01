# Gold Price Volatility Analysis During Economic Crises

## Project Overview
This project investigates **how major economic crises and periods of high inflation impact the volatility of gold prices** in the US. Gold is often considered a "safe-haven" asset during times of market instability, but this analysis explores whether gold prices are truly stable or if they experience significant fluctuations during periods of economic stress.

The research focuses on comparing gold price behavior across three economic periods from 2016 to 2026:

- **Stable Periods** – Years with minimal market disruptions.
- **COVID-19 Period** – The global market disruptions caused by the pandemic.
- **Inflation Periods** – Periods of elevated inflation and economic pressure.

The findings have implications for **investors, portfolio managers, financial institutions, and policymakers**, providing insights into how gold responds to uncertainty.

---

## Research Question
**How do major economic crises or periods of high inflation impact the volatility of gold prices compared to stable market periods?**

Understanding this helps:

- Determine if gold acts as a true safe-haven asset.
- Inform portfolio diversification and risk management strategies.
- Provide insights for policymakers observing gold as a market signal.

---

## Dataset Description
The dataset consists of **daily historical gold prices in USD** from 2016 to 2026, pulled from Yahoo Finance. It includes 2,530 rows and 7 columns.

**Key columns:**

| Column | Description |
|--------|-------------|
| Date | The trading day for each observation |
| Gold Price (USD) | Daily gold price in USD |
| Daily Return | Percentage change in gold price from the previous day |
| Rolling Volatility | 30-day rolling standard deviation of daily returns |
| Period Label | Categorical variable indicating the economic period (Stable, COVID, Inflation) |

**Notes:**
- The dataset does not include external economic factors such as interest rates or inflation.
- Missing values occur at the start due to the rolling volatility calculation.
- Non-trading days (weekends, holidays) are excluded and assumed to not impact results.

---

## Data Cleaning & Preparation
Key preprocessing steps included:

1. **Data Type Conversion:** Converted `Date` to datetime format and numeric columns to float/int.
2. **Daily Returns Calculation:** Computed percentage changes in gold prices to measure day-to-day volatility.
3. **Rolling Volatility:** Calculated 30-day rolling standard deviation to quantify market stability.
4. **Period Labeling:** Divided the dataset into Stable, COVID, and Inflation periods based on defined date ranges.
5. **Handling Missing Values:** Removed initial rows with missing rolling volatility values.

---

## Analysis & Visualization
Several visualizations were created to explore gold price behavior:

1. **Time Series Plot:** Displays rolling volatility from 2016–2026, showing spikes during COVID-19 and low volatility during stable periods.
2. **Boxplots of Volatility by Period:** Compare median and spread of volatility across economic periods; COVID period shows the largest range, while stable periods have the lowest.
3. **Histograms of Daily Returns:** Show distribution of daily returns for each period; COVID period has heavier tails, indicating larger price swings.

---

## Key Findings
- **Stable Periods:** Low and consistent volatility, predictable gold price behavior.
- **COVID-19 Period:** Highest volatility and widest distribution of returns, indicating rapid market adjustments and uncertainty.
- **Inflation Periods:** Moderate volatility, higher than stable periods but lower than crisis periods, reflecting persistent economic pressure.

**Interpretation:**  
Gold is reactive during economic stress but does not guarantee price stability. It remains a safe-haven in the long term, but short-term fluctuations are significant during crises.

---

## Limitations
- Analysis does not include broader economic variables such as interest rates, stock market trends, or macroeconomic indicators.
- Economic periods are simplified into fixed date ranges, while real-world conditions change gradually.
- Rolling volatility is used as the sole measure of stability, excluding other potential risk metrics.

---

## Future Work
- Include additional economic indicators like interest rates, inflation, and stock indices for a more complete understanding.
- Compare gold with other safe-haven assets (e.g., silver, bonds) to evaluate relative stability.
- Explore different volatility measures or machine learning models to predict gold price fluctuations during crises.

---

## Conclusion
This analysis shows that while gold is often considered a safe-haven asset, its short-term volatility **increases significantly during crises**, moderately rises during inflation, and remains stable in calm periods. Investors and policymakers can use these insights to better understand and manage risk in portfolios containing gold.
