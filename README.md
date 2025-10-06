# Ethereum-ETH--Strategy
Backtestable ETH/USDT Trading Strategy using Bollinger Bands &amp; EMA in Pine Script v6 with train/test date segmentation.

# BB EMA ETH/USDT 4h Strategy (Pine Script v6)

This repository contains a TradingView Pine Script v6 strategy for **Ethereum (ETH/USDT)** on the **4-hour timeframe**.  
It combines **Bollinger Bands (BB)** and an **Exponential Moving Average (EMA)** to generate long signals and manage exits.  
The script also includes **train/test date segmentation**, making it easier to validate performance on historical data.

---

## ✨ Features
- **Indicators Used**:
  - Bollinger Bands (configurable length & multiplier)
  - Exponential Moving Average (configurable length)
- **Signals**:
  - Long entry when price crosses above the upper Bollinger Band and is above EMA
  - Exit when price crosses under the Bollinger Band middle line or EMA
- **Train/Test Split**:
  - Select a time segment (Training, Testing, or All) for your backtest
  - Adjustable start & end dates for each segment
- **Strategy Parameters**:
  - Initial capital: 1000 USDT (can be adjusted)
  - Position size: 100% of equity per trade (can be adjusted)

---

## 🛠 How to Use
1. Open [TradingView](https://www.tradingview.com/).
2. Go to **Pine Editor** and paste the contents of `BB_EMA_ETHUSDT_4h.pine`.
3. Save and add it to your chart.
4. Select the **4H timeframe** and **ETH/USDT** pair.
5. Adjust the input parameters (EMA length, BB length, multiplier, train/test dates) as needed.
6. Choose the segment to backtest: `Training`, `Testing`, or `All`.

---

## 📈 Strategy Logic
- **Long Entry**:  
  `ta.crossover(close, bb_upper) and close > ema`
- **Exit**:  
  `ta.crossunder(close, bb_middle) or ta.crossunder(close, ema)`

---

## 📝 Inputs
| Parameter | Description |
|-----------|-------------|
| EMA Length | Period for the Exponential Moving Average |
| BB Length | Period for Bollinger Bands |
| BB Multiplier | Standard deviation multiplier for Bollinger Bands |
| Training Start/End Date | Date range for training backtest |
| Testing Start/End Date | Date range for testing backtest |
| Segment | Choose Training, Testing, or All |

---

## 📊 Example Chart
(Add a screenshot of your TradingView chart with the strategy applied here)

---

## ⚠️ Disclaimer
This script is for **educational purposes only**.  
It is not financial advice. Past performance does not guarantee future results.

---

## 📄 License
MIT License – feel free to modify and improve.

---


