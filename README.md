# BTC-gold-levels
Python script for analyzing Bitcoin's historical support levels: comparing the stability of Gold-pegged levels versus traditional USD price levels.

**Although the script generates images at selected levels, this indicator on TradingView allows you to "touch" the chart more closely and identify correlations.** https://ru.tradingview.com/script/jFB0u0CT-structural-gold-levels/


**Сomparing the stability of Bitcoin support levels denominated in Gold (grams) versus US Dollars.**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)
[![Status](https://img.shields.io/badge/status-active-success)]()

## Overview
This repository contains a Python analytical engine designed to test a key hypothesis in crypto-economics: 
**"Are Bitcoin structural levels more stable when measured in Gold rather than fiat currency (USD)?"**

The script analyzes 7 historical structural levels (2017–2021) and performs a comparative backtest to determine which unit of account—Gold or USD—provides a more reliable "memory" for the market.

## Key Features
- **Automated Data Fetching:** Downloads historical BTC/USD and Gold (XAU/USD) data via `yfinance`.
- **Dual-Unit Analysis:** Simultaneously tracks support/resistance behavior in both Fiat and Gold terms.
- **Smart "Respect" Algorithm:** Detects level interactions using a volatility-adjusted tolerance zone (±5%).
- **Visual Reporting:** Generates 7 comparative charts (USD vs Gold) for visual inspection.
- **Econometric Testing:** Calculates **Paired T-test** statistics to prove statistical significance of the results (P-value analysis).

## How It Works
The script evaluates "Level Quality" based on two metrics:
1.  **Respect Days:** How long the price stays within the level's zone (Stability).
2.  **Crossovers:** How often the price breaks the level (Instability).

It assigns a **Quality Score** for each level:
Score = Days_{Respect} - (Crossovers \times 5)

Finally, it runs a statistical test to reject the Null Hypothesis ($H_0$) that both methods are equal.

## 🛠️ Installation & Usage
You can run this code directly in **Google Colab** or locally.


### Running the Analysis
Simply run the main script:

The script will:
1.  Download necessary market data.
2.  Process all 7 levels.
3.  Save comparative charts as PNG files.
4.  Print a detailed ASCII report with P-value statistics.

## Example Results
*> Sample output from the statistical engine:*


