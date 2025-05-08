# ESG-Driven Trading Strategy Backtesting

This repository implements an ESG-enhanced trading system that combines traditional technical indicators with real-time ESG news sentiment analysis. It provides modular agents for data collection, indicator computation, strategy development, portfolio management, and backtesting.

## Repository Structure

├── a_580-project 1.py # Data collection and ESG sentiment mapping
├── a_580-project 2.py # Full pipeline: data collection, analysis, strategy development, portfolio management, backtesting
├── run_esg_agent.py # Fetch ESG news and export CSV files
├── backtest.py # Aggregate single-ticker reports and compute cross-ticker performance metrics
├── requirements.txt # Python dependencies
├── LICENSE # MIT open-source license
└── README.md # Project overview and usage instructions
## Environment Setup

We recommend using Conda:

```bash
conda create -n esg-trading python=3.8
conda activate esg-trading
pip install -r requirements.txt

## **Usage**

Run `python run_esg_agent.py --ticker NVDA --start-date 2025-04-05 --end-date 2025-05-02 --output-dir ./data` to fetch ESG news and export `*_esg_news.csv` and `*_esg_sentiment.csv`, then execute `python a_580-project\ 2.py` to run the full pipeline—data collection, technical indicator computation (moving averages, MACD, RSI, Bollinger Bands), ESG signal integration, trading signal generation, portfolio simulation, and backtesting. For basic data collection and signal mapping, use `python a_580-project\ 1.py`, which retrieves market data, maps ESG scores to buy/hold/sell signals, and updates internal state. Finally, run `python backtest.py` to scan all `<TICKER>_report.xlsx` files, build aggregate equity curves, and compute cross-ticker performance metrics (CAGR, volatility, Sharpe ratio, max drawdown, Sortino ratio, win rate, profit factor).  

## Results
Individual ticker reports are output as <TICKER>_report.xlsx.

Cross-ticker performance metrics are printed to the console and can be redirected to a log file.

## License
This project is licensed under the MIT License
