Bloomberg Stock Scraper
=======================

Stock data can be accessed in JSON format at the following Bloomberg URL:

http://www.bloomberg.com/markets/chart/data/" + frequency + "/" + ticker + ":US"

Bloomberg API
-------------
- Frequency can be either 1D, 1M or 1Y
- Ticker can be any stock symbol on NASDAQ, NYSE or Amex
- Time is returned in UNIX milliseconds.  Use the following function in Excel to convert to Excel seconds:

```
=(((A1/1000/60)/60)/24)+DATE(1970,1,1)+(-5/24)
```

For example, if we want today's prices for Apple, we could send the following request:

http://www.bloomberg.com/markets/chart/data/1D/AAPL:US

Documentation
-------------
To run this program, cd to the right directory and run "python main.py" like so:

```bash
Matthews-MacBook-Pro:stock_data matthewfieger$ python main.py
```
You can scrape data for all stocks listed on a single exchange or you can input a custom list of stocks in "custom.csv".  I haven't encountered any need to throttle requests to this Bloomberg endpoint, so you should be able to scrape to your heart's delight!