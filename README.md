# A10 — Time‑Series Analysis of U.S. Treasury Yields and Equity Markets for Improved Forecasting

> _Exploratory analysis of FRB H.15 yields, S&P 500, and VIX with correlations, signal studies, and classic time‑series diagnostics_

<p align="center">
  <img alt="Yield curve & equities" src="https://img.shields.io/badge/Notebook-Analysis-blue?logo=jupyter">&nbsp;
  <img alt="Focus" src="https://img.shields.io/badge/Focus-Treasuries%20%26%20Equities-8A2BE2">&nbsp;
  <img alt="Language" src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python">
</p>

---

## 🧭 Executive Summary

This repository contains a single Jupyter notebook that analyzes relationships between U.S. Treasury yields and U.S. equity markets. 
Using daily data (e.g., FRB H.15 Treasury yields, S&P 500 index levels, and the VIX), the notebook explores:
- Yield‑curve behavior (spreads, inversions, curvature) and how often inversions occur across maturities.
- Equity–rate interactions via daily and rolling correlations, cross‑correlations, and drawdown overlays.
- Signal studies including forward‑return buckets by inversion depth and rate‑shock “jump day” behavior versus VIX.
- Time‑series diagnostics such as stationarity checks (ADF), ACF/PACF inspection, and rolling OLS betas/R² for return attribution.

The goal is to build intuition for how rate regimes map to equity risk and to outline features and checks that can feed future forecasting work.

---

## 👥 Team

- **Team Number:** 10  
- **Team Name:** **The Exponents**  
- **Team Members:** Akbar, Daaksha, Dongfang, Jaisy, Purnima, Vishesh  
- **Project Manager:** Vishesh

---

## 📁 Repository Contents

This repo intentionally contains **one notebook** (the project itself):

```
A10-TIME-SERIES-ANALYSIS-OF-U-S-TREASURY-YIELDS-AND-EQUITY-MARKETS-FOR-IMPROVED-FORECASTING.ipynb
```

---

## 🧪 What’s Inside (Highlights)

- 99th‑percentile 2‑year yield shocks vs VIX (“jump days”)
- Classic 10Y–3M spread tracking
- Daily and rolling (60‑day/12‑month) bond‑equity correlations
- Drawdown vs 2s10s slope, cross‑correlation of slope vs VIX
- Forward 12‑month S&P returns by inversion depth
- Rolling S&P betas to 2‑yr/10‑yr rate changes and rolling R²
- S&P 500 vs inverted 10‑year yield index overlay
- Stationarity check (ADF) + ACF/PACF visuals for key series
- Treasury curve butterfly curvature vs forward equity returns
- Yield‑curve spreads heatmap (2014–2024) and 10‑year yield stats

> Each section pairs a guiding **Question → Interpretation → Answer** pattern with visuals to support plain‑English takeaways.

---

## ⚙️ Requirements

Install the following Python libraries (as used in the notebook):

- `matplotlib`
- `numpy`
- `pandas`
- `re`
- `seaborn`
- `statsmodels`

You can use a simple environment:

```bash
pip install matplotlib numpy pandas re seaborn statsmodels
```

---

## 📊 Data Inputs (expected locally)

The notebook reads the following CSV files from the working directory:

- `FRB_H15.csv`
- `VIXCLS.csv`
- `sp500_index.csv`
- `us_treasury_yields_daily_Kaggle.csv`

> If you do not have these CSVs, update the relevant cells to point to your data sources or equivalent series.

---

## ▶️ How to Run

1. **Clone** or download this repo (it contains only the notebook and the datasets).  
2. Place the input CSVs (listed above) next to the notebook or adjust paths in the loading cells.  
3. Open the notebook with Jupyter/Colab and **run cells top‑to‑bottom**.

---

## 🧠 Methods & Checks (as implemented)

- Descriptive statistics and trend visuals for rates and equities.  
- Stationarity tests: **Augmented Dickey–Fuller (ADF)**.  
- Autocorrelation/partial autocorrelation: **ACF/PACF** plots.  
- Rolling windows for correlations, betas, and fit quality (**R²**) via OLS.  
- Cross‑correlation to explore lead/lag dynamics (e.g., slope vs VIX).

---

## ✅ Outputs

- Plots illustrating yield‑curve regimes and equity relationships.  
- Tables/snippets summarizing rate shocks, forward returns, and diagnostics.  
- Narrative blocks with **Question → Interpretation → Answer** for each figure.

---

## 🚧 Limitations (from the notebook’s scope)

- Focused on a select set of daily series and time windows.  
- Correlations/regimes can be **time‑varying**; out‑of‑sample stability is not guaranteed.  
- Forecasting is **not** the primary contribution here; the notebook builds ingredients and intuition for downstream models.

---

## 🗺️ Future Work (suggested next steps)

- Expand the data panel (macro factors, term‑structure features, equity factor returns).  
- Robust feature engineering and **walk‑forward** validation for forecasting.  
- Compare model families (e.g., ARIMA/VAR baselines, rolling OLS, tree/boosted models) using consistent evaluation.  
- Stress‑scenario dashboards with real‑time refresh.

---

## 📎 Citation/Attribution

Please cite the notebook by repository name and commit if used in reports or coursework.

---
