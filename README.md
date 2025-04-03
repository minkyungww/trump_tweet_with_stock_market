# 📊 Analyzing the Influence of Presidential Candidates' Tweets on Stock Market Volatility  
### A Dynamic Topic Modeling Approach

This repository contains the code and analysis for a computational social science project that investigates the relationship between **Donald Trump's tweets** and **stock market volatility** during the 2020 U.S. presidential election period.

---

## 🧠 Abstract

Using **Dynamic Topic Modeling (DTM)** and **high-frequency trading data**, this project explores how political communication via Twitter — particularly from presidential candidate Donald Trump — influences market behavior. Our analysis reveals that while early tweets caused market reactions, repeated tweets on the same topics resulted in **diminishing effects**, suggesting a **desensitization phenomenon** among investors.

---

## 📁 Project Structure

- `trump_tweet_with_stock_market.ipynb`  
  → Analyzes high-frequency stock price & volume data in relation to tweet events.

- `trump_tweet_dynamic_topic_modeling.ipynb`  
  → Implements BERTopic and Dynamic Topic Modeling on Trump’s tweets.

- `Final Report_Team 20.pdf`  
  → Full report documenting background, data, methods, results, and discussion.

---

## 📌 Research Motivation

- Twitter, especially when used by influential figures like Donald Trump, can **introduce new information** that moves financial markets.
- Previous studies lacked **temporal resolution**, using daily price data that masked minute-level reactions.
- Our approach addresses this by combining **minute-by-minute market data** with **time-aware topic modeling**.

---

## 📊 Data Sources

| Dataset | Source | Description |
|--------|--------|-------------|
| **Tweets** | [Twitter Stance Election 2020](https://paperswithcode.com/dataset/twitter-stance-election-2020) | 9,868 tweets from Trump (Feb–Nov 2020), filtered to NASDAQ trading hours. |
| **Market Data** | [Alpha Vantage Stock API](https://www.alphavantage.co/) | S&P 500 and 11 sector ETFs, 1-minute frequency data. |

---

## 🧪 Methodology

### 1. **Dynamic Topic Modeling (DTM)**
- Used **BERTopic** to identify 20 meaningful tweet topics.
- Focused on key topics like *China*, *Covid*, *Economy*, *Fake News*, and *Healthcare*.

### 2. **Macro Analysis**
- Aggregated tweet frequency (14-day intervals) for each topic.
- Compared tweet frequency with **S&P 500 trading volume** and **price movement**.
- Analyzed correlations using gradient changes and Pearson coefficients.

### 3. **Micro Analysis**
- Calculated average trading volume **10 min ~ 3 hours** after tweet events.
- Conducted **linear regression** to determine influence by topic frequency.

---

## 📈 Key Findings

- **Negative correlation** observed between tweet frequency and market volatility.
- New tweets had higher market impact; repeated tweets triggered **smaller reactions**.
- Some sectors (e.g., XLF - Financials) were more sensitive to certain topics (e.g., "Economy").

---

## 💡 Insights

- **Efficient Market Hypothesis (EMH)** holds for new political communication, but **desensitization** occurs over time.
- Investors eventually **ignore repeated political messages**, reducing volatility.
- This behavior can be leveraged in building smarter trading algorithms.

---

## 🚧 Limitations & Future Work

- Analysis limited to tweets during trading hours and only from Twitter.
- Did not include **Joe Biden's tweets** due to insufficient volume.
- Future research could explore:
  - Stock **returns** (not just volume)
  - Other social platforms (e.g., Reddit, Facebook)
  - Off-hour tweet impact on market **opening volatility**



