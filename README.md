# crypto-arbitrage-screener
Crypto arbitrage screener built in a Jupyter notebook. This tool scans Binance spot vs futures markets for opportunities where you can profit from price discrepancies beyond a transaction cost threshold.

🚀 Features
📡 Live price feeds using Binance WebSocket API (via websocket-client)

💹 Detects and logs arbitrage opportunities between spot and futures

⚙️ Customizable cost threshold, supports multiple crypto symbols

📁 Logs opportunities in timestamped CSV files

🧵 Multi-threaded price tracking per symbol

📊 Console output for both opportunity alerts and periodic updates

📓 Notebook: screener.ipynb
The notebook provides:

📌 A clean, structured view of the ArbitrageMonitor class

🧪 Example: Monitor ETH, BTC, SOL, and ADA

📤 Auto-logs to arbitrage_<symbol>.csv (e.g., arbitrage_eth.csv)

💡 Can be adapted to backtest or extend for strategy development

⚙️ Requirements
Install dependencies:

bash
Copier
Modifier
pip install websocket-client
Standard libraries used: json, threading, csv, os, datetime, time.

🧪 How to Use
Open the screener.ipynb notebook in Jupyter Lab or Jupyter Notebook.

Run all cells.

Sit back and let the screener monitor your selected symbols.

⚙️ Customization
You can change symbols and cost threshold in the notebook’s main section:
symbols = ['eth', 'btc', 'sol', 'ada']
monitor_multiple_symbols(symbols, cost_threshold=0.005)
Change the list or threshold to fit your arbitrage strategy.

📊 Output Example
ETH Arbitrage detected: Buy SPOT at $1872.25, Sell FUTURE at $1873.31 | Profit: $0.06
CSV: arbitrage_eth.csv

timestamp,symbol,spot_price,future_price,spread,profit,arbitrage_opportunity
2025-05-09T12:03:45,ETH,1872.2500,1873.3100,1.0600,0.5550,YES

📂 Project Structure
├── screener.ipynb           # Jupyter Notebook with full arbitrage logic
├── arbitrage_eth.csv        # Auto-generated logs (example)
├── arbitrage_btc.csv
├── ...
└── README.md

📜 License
MIT License — free for personal or commercial use. Attribution appreciated!
