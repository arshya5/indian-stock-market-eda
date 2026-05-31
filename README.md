![Python](https://img.shields.io/badge/Python-3.11-blue)
![Streamlit](https://img.shields.io/badge/Streamlit-Dashboard-red)
![Finance](https://img.shields.io/badge/Domain-Finance-green)
![EDA](https://img.shields.io/badge/EDA-Analytics-purple)
![yFinance](https://img.shields.io/badge/API-yFinance-orange)

[![Live App](https://img.shields.io/badge/Streamlit-Live_App-red)](https://indian-stock-market-eda.streamlit.app/)

# Stock Market Exploratory Data Analysis | Trend and Volatility Insights (India)

### Objective: Help investors understand market behavior, risk patterns, and long-term trends.

---

## Executive Summary

This project explores historical stock price data to understand how the market behaves over time. The analysis focuses on identifying trends, studying volatility patterns, and examining trading behavior through a time-series lens.

Rather than forcing artificial business outcomes or overcomplicating the approach, the work stays grounded in exploratory analysis. A basic forecasting model is included as an extension, while the primary focus remains on uncovering meaningful patterns in the data.

The analysis is also presented through an interactive Streamlit dashboard, allowing users to explore trends and insights visually.

---

## Analytical Objective

The objective of this project is to analyze historical stock data to better understand price behavior, identify recurring patterns, and derive insights that can support more informed financial decision-making.

---

## Stakeholders

* Retail investors
* Financial analysts
* Market researchers

---

## Methodology

The dataset was collected using the yfinance API, providing historical price and volume data.

The data was cleaned and structured for time-series analysis. Relevant time periods were selected, followed by exploratory steps including trend analysis, return calculations, rolling statistics, and volume comparison.

Visualizations were used extensively to support observations and make patterns easier to interpret.

---

## Technical Skills

| Tool / Area   | Techniques Used                      |
| ------------- | ------------------------------------ |
| Python        | Pandas (time-series analysis), NumPy |
| Visualization | Matplotlib, Seaborn, Plotly          |
| Data Source   | yfinance API                         |
| Deployment    | Streamlit                            |

---

## Visual Analysis

### Price Trend Over Time

![Price Trend](eda/visualizations/price_trend.png)

This chart shows a strong long-term upward trend, with the stock price increasing from approximately ₹190 in 2015 to nearly ₹1,300 by 2021. Despite several corrections, the overall trajectory remains positive.

The sharp decline around 2018 represents a structural break in market behavior. This period coincides with the IL&FS financial crisis, which triggered broader concerns around liquidity and credit risk across Indian financial markets. Following this disruption, the market entered a new growth phase and recovered strongly.

---

### Rolling Volatility (10-Day)

![Volatility](eda/visualizations/rolling_volatility.png)

Volatility appears in distinct clusters rather than remaining constant. For most of the analysis period, volatility remained relatively stable before surging sharply during the 2018 market disruption, reaching nearly 9%.

The subsequent decline in volatility supports the concepts of volatility clustering and mean reversion, where periods of instability are followed by calmer market conditions.

---

### Returns Distribution

![Returns](eda/visualizations/returns_distribution.png)

The distribution is centered around zero, indicating that most daily price changes are relatively small. However, extreme observations extend roughly from -13% to +15%, demonstrating that large market movements occur more frequently than would be expected under a normal distribution.

This confirms the presence of fat-tailed behavior and highlights the importance of accounting for tail risk when evaluating investment decisions.

---

### Moving Averages

![Moving Average](eda/visualizations/moving_average.png)

The moving averages closely follow the price trend while smoothing short-term noise. However, they visibly lag behind sudden price movements, reinforcing their role as confirmation indicators rather than predictive tools.

---

### Volume vs Price Relationship

![Volume vs Price](eda/visualizations/volume_vs_price.png)

There is no strong linear relationship between volume and price. Data points are widely scattered, suggesting that price movements are influenced by multiple factors beyond trading volume alone.

---

### Cumulative Returns (Growth of ₹1)

![Cumulative Returns](eda/visualizations/cumulative_returns.png)

Despite short-term fluctuations and significant drawdowns, cumulative returns demonstrate strong long-term wealth creation. A hypothetical ₹1 investment grew to approximately ₹7 during the analysis period.

This reinforces the importance of long-term investing and highlights how sustained growth can outweigh temporary market disruptions.

---

### Daily Returns Over Time

![Returns Over Time](eda/visualizations/returns_over_time.png)

Returns fluctuate around zero with occasional sharp spikes, highlighting periods of market shocks and increased volatility. The most extreme movements occur during periods of market stress, further supporting the presence of tail risk in financial markets.

---

## Key Insights

* The stock appreciated from approximately ₹190 to nearly ₹1,300 during the analysis period
* Market behavior is characterized by distinct regimes rather than smooth linear trends
* Volatility clusters during periods of instability, particularly during the 2018 market disruption
* Daily returns exhibit fat-tail risk, with extreme observations ranging from roughly -13% to +15%
* A hypothetical ₹1 investment grew to approximately ₹7 despite multiple drawdowns and market shocks

---

## Results and Insights

Stock prices do not move in a smooth or predictable manner. Instead, they exhibit structural breaks, where sudden shifts are followed by new phases of behavior. This suggests that markets operate in distinct regimes rather than continuous trends.

Volatility appears in bursts rather than remaining constant. These bursts tend to cluster, indicating that periods of instability persist before stabilizing.

Daily returns are mostly small and centered around zero, but extreme movements occur more frequently than expected. The presence of returns ranging from approximately -13% to +15% highlights the importance of tail-risk awareness in financial decision-making.

Volatility demonstrates mean-reverting characteristics, where periods of elevated uncertainty are often followed by stabilization.

Moving averages help confirm trend direction but lag behind real-time market movements, making them more useful as confirmation indicators than predictive tools.

Trading volume does not exhibit a consistent relationship with price direction, suggesting that price movement is influenced by a combination of factors including sentiment, macroeconomic conditions, and broader market dynamics.

Despite short-term noise, volatility spikes, and temporary drawdowns, long-term performance remains strongly positive, with cumulative returns increasing approximately sevenfold over the analysis period.

---

## Recommendations (Interpretation)

* Focus on long-term trends rather than short-term fluctuations
* Be cautious during high-volatility periods
* Do not rely solely on volume for decision-making
* Use moving averages as confirmation tools rather than predictors

---

## Practical Takeaways

* Avoid making emotional decisions during volatility spikes
* Focus on long-term trend direction rather than daily noise
* Consider tail-risk events when evaluating investments
* Use technical indicators as supporting tools, not standalone predictors

---

## Limitations

* Based only on historical price and volume data
* No inclusion of macroeconomic or sentiment factors
* Forecasting model is basic and experimental

---

## Next Steps

* Integrate real-time stock data
* Add sentiment analysis (news, social media)
* Apply advanced models (LSTM, ARIMA)
* Expand to multiple stocks and sectors

---

## Repository Structure

```text
/data
/notebooks
/visualizations
app.py
requirements.txt
README.md
```

---

## Running the Project

```bash
git clone https://github.com/arshya5/Indian-stock-market-prediction.git
cd Indian-stock-market-prediction
pip install -r requirements.txt
streamlit run app.py
```

---

## Closing Note

This project focuses on understanding financial markets through structured analysis rather than relying solely on complex modeling. It emphasizes clarity, interpretation, and the ability to extract meaningful insights from data.

The goal is not to predict every market movement, but to better understand the patterns, risks, and behaviors that shape long-term market performance.
