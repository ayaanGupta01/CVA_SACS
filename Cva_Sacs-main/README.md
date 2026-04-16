# CVA-SACS v6 — Market Intelligence Terminal
A professional-grade stock market risk analysis dashboard powered by 
Machine Learning, FinBERT sentiment analysis, and advanced quantitative methods.

## What This Project Does
- Scans stocks and ranks them by **Composite Risk Index (CRI)**
- Uses **XGBoost + LightGBM + CatBoost ensemble** ML models
- Performs **FinBERT NLP sentiment analysis** on market news
- Runs **Monte Carlo simulations** for forward price prediction
- Provides **SHAP explainability** — understand *why* a signal was generated
- Supports both **US stocks** (AAPL, MSFT, NVDA...) and **Indian stocks** (RELIANCE.NS, TCS.NS...)

## Quick Start

### Option 1 — One Click Setup
```bash
python setup_and_run.py
```

### Option 2 — Manual Setup
```bash
pip install -r requirements.txt
streamlit run cva_sacs_v6.py
```

### Option 3 — Docker
```bash
docker build -t cva-sacs-v6 .
docker run -p 8501:8501 cva-sacs-v6
```



## Architecture
- `cva_sacs_v6.py` — Streamlit dashboard (9 pages)
- `cva_sacs_v6_ml.py` — ML engine (130 features, XGB+LGB+CAT ensemble)
- `cva_sacs_v6_sentiment.py` — FinBERT NLP sentiment
- `cva_sacs_v6_data.py` — Data expansion (S&P 500 + Nifty 100)
- `cva_sacs_v6_advanced.py` — SHAP, Monte Carlo, Conformal Prediction
- `config.py` — Centralised configuration
- `tests/` — Unit tests (pytest)
# CVA_SACS



## Dashboard Pages
1. **Market Overview** — Live watchlist scan
2. **Stock Screener** — Any tickers, ranked by CRI
3. **Deep Analysis** — Full ML pipeline + FinBERT sentiment
4. **Backtest** — Equity curve, Sharpe ratio, Kelly sizing
5. **Comparison** — CRI vs CRI, correlation matrix
6. **Portfolio Risk** — Weighted CRI, bubble chart
7. **Explainability** — SHAP waterfall, what-if analysis
8. **Monte Carlo** — Forward price simulation
9. **Conformal** — Prediction sets with statistical guarantees


## Requirements
- Python 3.9+
- See `requirements.txt` for full list

## Tech Stack
- **Dashboard:** Streamlit + Plotly
- **ML Models:** XGBoost, LightGBM, CatBoost
- **NLP:** FinBERT (HuggingFace Transformers)
- **Data:** yfinance (Yahoo Finance)
- **Explainability:** SHAP
- **Forecasting:** Prophet

---
