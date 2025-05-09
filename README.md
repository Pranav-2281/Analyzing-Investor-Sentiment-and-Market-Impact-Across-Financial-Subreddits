# 📈 Analyzing Investor Sentiment and Market Impact Across Financial Subreddits

**Technologies**: PySpark, AWS (SageMaker, S3), Spark NLP, Matplotlib, DuckDB, GitHub, Quarto  
**Subreddits Analyzed**: r/investing, r/cryptocurrency, r/finance

![Subreddit Banner](/website-source/subreddit_banner.png)
## 🔍 Project Overview

This project explores the relationship between retail investor sentiment on Reddit and market dynamics, focusing on the **r/investing** and **r/cryptocurrency** communities. By analyzing over 3 million Reddit comments and posts, we aimed to understand how social sentiment, trending discussions, and user engagement reflect and potentially predict financial behavior—especially around volatile instruments like Bitcoin.

---

## 🎯 Business Questions

| # | Business Question | Summary |
|---|-------------------|---------|
| 1 | What are the most common words on the CryptoCurrency and Investing subreddits? | Performed frequency analysis to identify dominant themes and discussion points. |
| 2 | Do world events lead to increased discussion volume on r/investing? | Analyzed spikes in comment volume and correlated with financial events. |
| 3 | What are the temporal patterns in investor engagement? | Used heatmaps and time-series plots to detect high-activity periods and their triggers. |
| 4 | Which stocks are most frequently mentioned on Reddit? | Conducted term matching and visualization to highlight popular equities. |
| 5 | Which cryptocurrencies are most frequently mentioned? | Analyzed text data to rank top-mentioned coins like BTC, ETH, and SOL. |
| 6 | How do crypto prices affect the number of posts/comments on r/CryptoCurrency? | Investigated correlation between price fluctuations and subreddit activity. |
| 7 | What are the most frequently discussed financial topics? | Used RegEx to categorize comments into themes like “S&P 500” and “Federal Reserve.” |
| 8 | How do comment lengths vary across subreddits? | Sampled and visualized comment distributions to support NLP strategy. |
| 9 | How does sentiment vary across topics and over time? | Applied sentiment analysis to identify topic-based polarity trends. |
| 10 | Can sentiment and comment volume predict next-day Bitcoin volatility? | Built regression models to evaluate relationships between Reddit chatter and market movement. |
| 11 | Can sentiment and comment volume predict next-day Bitcoin price direction? | Built classification models to forecast binary up/down price movements. |

---

## 📊 EDA Highlights

- Cleaned and validated over **205K posts** and **3.6M comments**.
- Identified **comment spikes** during key financial events.
- Built engagement heatmaps across **hours, days, and weeks**.
- Extracted key terms indicating sentiment and user interest.

---

## 🗣️ NLP Pipeline

- Built using **Spark NLP**, **USE embeddings**, and **PySpark pipelines**.
- Sentiment analysis via **Twitter DL model** for robust polarity detection.
- Identified key topics using **RegEx** for S&P 500, Bitcoin, and the Fed.
- Visualized **sentiment proportions over time** and by topic.

---

## 🧪 Machine Learning Approach

**Models Trained**:
- Logistic Regression & GBTClassifier (for price direction)
- Linear Regression & GBTRegressor (for volatility)

**Process**:
- Aggregated daily sentiment and topic mentions.
- Trained models using PySpark on 70/20/10 train/test/val split.
- Evaluated with ROC, RMSE, and accuracy metrics.

**Findings**:
- No significant predictive power observed.
- Best model (GBTClassifier) showed **marginal improvement** over naive baseline.
- Insights into **which features slightly influenced volatility**.

---

## 📦 Technologies Used

- **PySpark** – distributed ETL and model training  
- **Spark NLP** – lemmatization, sentiment detection  
- **Universal Sentence Encoder** – comment embeddings  
- **AWS S3 / SageMaker Studio** – compute and data storage  
- **Polars, DuckDB** – fast in-memory querying  
- **Matplotlib, Seaborn** – data visualizations  
- **Quarto** – documentation and publishing  
- **GitHub** – version control and collaboration  

---

## 📈 Results & Metrics

- Processed **3M+ Reddit comments** across subreddits  
- Crypto-related Reddit posts increased during downturns, possibly reflecting investor concern
- **Bitcoin, Ethereum, Binance** were most frequently discussed tokens
- Positive sentiment was strongest for crypto content vs. traditional finance
- Identified engagement patterns tied to **financial events**  
- ML models failed to predict price/volatility from Reddit data—supporting the efficient market hypothesis
- Detected **1,500+ fraudulent users** via clustering  

---

## 🔮 Future Work

- Introduce **BERT-based sentiment models** for richer semantic understanding  
- Expand dataset to include **Twitter, Discord, and stock forums**  
- Explore **user-level engagement modeling** for fraud detection  
- Refine time-lag features to **better capture market responses**  

---
