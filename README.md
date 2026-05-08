# Trading Behaviour Analysis using Fear & Greed Index

## Project Overview
This project analyzes whether market sentiment affects trader profitability using real trading data from Hyperliquid and the Bitcoin Fear & Greed Index.

The goal is to understand how traders behave during:
- Extreme Fear
- Fear
- Neutral
- Greed
- Extreme Greed

and identify whether traders earn more profit during certain market emotions.

---

# What is the Fear & Greed Index?

The Fear & Greed Index measures the overall mood of the crypto market on a scale from **0 to 100**.

- **0 → Extreme Fear**
- **100 → Extreme Greed**

It reflects whether traders are:
- scared and panic selling (**Fear**)
- overly confident and aggressively buying (**Greed**)

### Simple Analogy
Imagine the stock market like a crowd during a big sale:

- When everyone is excited and rushing to buy → **Greed**
- When everyone is scared and running away → **Fear**

It works like a “market emotion meter.”

---

# What is Hyperliquid Trader Data?

Hyperliquid is a crypto trading platform.

The dataset contains the complete trading activity of **32 real traders**, including:
- every buy and sell trade
- profit and loss
- traded coin
- trade size
- execution price
- timestamps

### Simple Analogy
Imagine having the complete bank statement of 32 traders for several months.

You can track:
- what they bought
- what they sold
- when they traded
- whether they made profit or loss

---

# Project Goal

The main objective of this project is to answer:

> Does market sentiment affect trader profitability?

This analysis explores:
- Do traders earn more during Extreme Greed?
- Do traders panic during Fear?
- Are traders more aggressive during certain emotions?
- Which coins perform best during Fear or Greed?
- How does buying/selling behavior change with market sentiment?

---

# Datasets Used

## 1. Fear & Greed Dataset

Contains daily Bitcoin market sentiment.

### Columns Description

| Column | Description |
|---|---|
| `timestamp` | Unix timestamp representing the date |
| `value` | Sentiment score from 0–100 |
| `classification` | Sentiment category (Fear, Greed, etc.) |
| `date` | Readable date used for merging datasets |

### Sentiment Categories

| Score Range | Classification |
|---|---|
| 0–24 | Extreme Fear |
| 25–44 | Fear |
| 45–55 | Neutral |
| 56–74 | Greed |
| 75–100 | Extreme Greed |

---

## 2. Historic Trading Dataset

Contains real trader transaction data from Hyperliquid.

### Columns Description

| Column | Description |
|---|---|
| `Account` | Unique wallet/trader ID |
| `Coin` | Cryptocurrency traded |
| `Execution Price` | Actual execution price of trade |
| `Size Tokens` | Quantity of coins traded |
| `Size USD` | Dollar value of the trade |
| `Side` | BUY or SELL |
| `Timestamp IST` | Trade date and time in Indian Standard Time |

---

# Key Analysis Performed

- Data cleaning and preprocessing
- Merging trader data with sentiment data
- Profitability analysis by market sentiment
- Buy vs Sell behavior analysis
- Win rate calculation
- Coin-wise performance analysis
- Crossed order pattern analysis
- Visualization using Matplotlib

---

# Key Insights

- Traders earned higher profits during **Fear** and **Extreme Greed**
- During Fear, traders became more aggressive in buying and selling
- Crowd sentiment significantly affected trader profitability
- Some coins consistently performed better during panic conditions
- Contrarian behavior was visible:
  - traders bought during fear
  - traders sold during greed

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab

---

# Conclusion

This project demonstrates that market psychology strongly influences trading behavior and profitability.

The analysis supports the idea that:
- Fear creates opportunity
- Extreme Greed increases volatility
- Contrarian trading behavior can generate higher returns

By combining trader transaction data with market sentiment, we can better understand how emotions drive financial decisions in crypto markets.
