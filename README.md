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
