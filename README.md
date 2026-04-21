# Portfolio-Analysis

A simple Streamlit app for uploading an investment portfolio CSV and generating:
- asset allocation
- geographic allocation
- trailing returns

## Files in this repo

- `Stage1.py` — the full Streamlit app
- `requirements.txt` — required Python packages
- `sample_holdings.csv` — example file to test the app

## What the app does

The app allows a user to:
1. Upload a CSV containing a holding identifier, description, and GBP value
2. Confirm the extracted holdings
3. View:
   - % allocation to Equity, Bonds, Alternatives, and Cash
   - geographic allocation across North America, Europe (excluding UK), UK, Japan, and Rest of World
   - estimated 1-year, 3-year, and 5-year returns
4. Download the outputs as CSV files

## Expected CSV format

The app expects columns that are close to:
- `Ticker` or `ISIN` or `SEDOL`
- `Description`
- `GBP Value`

Example:

```csv
Ticker,Description,GBP Value
VUSA.L,Vanguard S&P 500 UCITS ETF,25000
VUKE.L,Vanguard FTSE 100 UCITS ETF,10000
```

## How to run locally

Install the packages:

```bash
pip install -r requirements.txt
```

Then run:

```bash
streamlit run Stage1.py
```

## How to deploy

1. Upload all files in this repo to GitHub
2. Go to Streamlit Community Cloud
3. Create a new app
4. Select this repository
5. Set the main file path to `Stage1.py`
6. Deploy

## Notes

This version is deliberately simple and keeps everything in one Python file to make GitHub and Streamlit deployment easier.

The app currently uses a small built-in mapping dictionary for some example tickers and identifiers. If you use other holdings, you may need to add them into the `MANUAL_MAPPING` section inside `Stage1.py`.
