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
