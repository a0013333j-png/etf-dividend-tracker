# ETF Dividend Tracker

🇹🇼 A Python-based tool to track Taiwan ETF dividends (currently supports 0050, 0056, 00878).  
此專案用 Python 建立台灣 ETF 股利追蹤工具，支援 0050 / 0056 / 00878。

---

## ✨ Features 功能特色
- Auto-fetch ETF dividends and prices (from TWSE / Yahoo Finance APIs, with fallback to web scraping).  
  自動抓取台灣 ETF 的歷史配息與股價（優先使用官方/金融 API，必要時用爬蟲備援）。  
- Track personal trades and holdings.  
  依據交易紀錄追蹤持股與均價。  
- Calculate TTM (Trailing Twelve Months) dividend yield.  
  計算近 12 個月配息殖利率。  
- Generate monthly cash flow timeline from dividends received.  
  根據實際持股生成「每月現金股利」時間序列。  
- Simple forward projection of future 12 months cash dividends.  
  以歷史配息簡單預測未來 12 個月現金流。  
- Export results with charts.  
  產出圖表，方便視覺化觀察。

---

## 📂 Project Structure 專案結構
```
etf-dividend-tracker/
│
├── README.md ← 專案說明
├── requirements.txt ← 需求套件 (pandas, matplotlib, yfinance, requests, bs4)
│
├── data/ ← 數據存放
│ ├── dividends.csv ← 歷史配息 (ticker, date, dividend_per_share)
│ ├── trades.csv ← 個人交易 (date, ticker, shares, price, fee, notes)
│ └── prices/ ← (選擇性) 股價快照
│
├── notebooks/
│ └── etf_dividend_tracker.ipynb ← Jupyter notebook 主程式
│
├── scripts/
│ ├── fetch_dividends.py ← 抓配息
│ ├── fetch_prices.py ← 抓股價
│ └── update_tracker.py ← 整合更新
│
└── output/
├── figures/ ← 圖表輸出
└── reports/ ← (選擇性) PDF 報告
```

## 🚀 Quick Start 快速開始
1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/etf-dividend-tracker.git
   cd etf-dividend-tracker

2. Install dependencies:
```
   pip install -r requirements.txt
```
3. Update data/trades.csv with your own trades.
   在 data/trades.csv 填入你的實際交易紀錄。

4. Run the notebook:
   打開 notebooks/etf_dividend_tracker.ipynb，依序執行。

## 📊 Example Data 範例資料
   data/dividends.csv
   ```
  ticker,date,dividend_per_share
   0050,2024-07-15,7.10
   0056,2024-12-18,1.20
   00878,2024-10-20,0.30
```

data/trades.csv
```
   date,ticker,shares,price,fee,notes
   2024-06-10,0050,5,150.0,10,首次投入
   2024-07-25,0056,20,30.5,10,逢低加碼
   2024-09-02,00878,30,17.8,10,定期定額
```


## ⚠️ Disclaimer 免責聲明
   This tool is for educational purposes only and not financial advice.
   本工具僅供學習與研究，非投資建議。請自行確認數據來源與投資風險。


---

