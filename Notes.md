 # Alpha Vantage

Alpha Vantage provides realtime equities and forex data. Free registration is required to get an API key.Now we get one.(Alpha Vantage: API key is: OBN8PXVTLNCZ2ULQ)

## Historical Time Series Data

Through the Alpha Vantage Time Series endpoints, it is possible to obtain historical equities and currency rate data for individual symbols. For daily, weekly, and monthly frequencies, 20+ years of historical data is available. The past 3-5 days of intraday data is also available.

The following endpoints are available:

- av-intraday - Intraday Time Series

- av-daily - Daily Time Series

- av-daily-adjusted - Daily Time Series (Adjusted)

- av-weekly - Weekly Time Series

- av-weekly-adjusted - Weekly Time Series (Adjusted)

- av-monthly - Monthly Time Series

- av-monthly-adjusted - Monthly Time Series (Adjusted)

- av-forex-daily - Daily Time Series

## Python environment

We use the python 3.6 version.

- Create an independent Python environment

```bash
mkdir US_Stock
cd US_Stock/
virtualenv --python=python3.6 venv
source venv/bin/activate
deactivate
```

- add the virtual environment into jupyter notebook interpreter

```python
ipython kernel install  --name=US_stack
```

## Requirements Package

pip install -r requirements.txt

virtualenv
pandas-datareader
ipykernel
xlrd

## Excel (Yahoo Ticker Symbol)

This Excel spreadsheet was updated in September 2017.  It is broken down into eight sheets, one each for

- stocks (106332 tickers)
- ETFs (21196tickers)
- futures (9294 tickers)
- indices (80017 tickers)
- mutual funds (24926 tickers)
- currency pairs (4019 tickers)

You get tickers across all international exchanges, including

- Chicago Board of Trade (CBT), Chicago Merctantile -   - - Exchange (CME) and New York Stock Exchange (NYSE)
- Toronto Stock Exchange (TSX)
- Sao Paolo Stock Exchange (BOVESPA)
- London Stock Exchange (LSE)
- Bombay Stock Exchange (BO) and National Stock Exchange of India (NSE)
- Hong Kong Stock Exchange (HKG) and Chinese stock exchanges (SHZ, SHH)
- European exchanges (including Germany, France, Amsterdam etc)
- Melbourne Stock Exchange (ASX)
and many others
