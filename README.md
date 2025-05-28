# RSI & EMA Stock Trading Bot
Beginner-friendly Python trading bot which uses two common technical indicators, Relative Strength Index (RSI) and Exponential Moving Averages (EMA)

## Features
- Calculates RSI to detect overbought/oversold market conditions
- Computes short term and long term EMAs to catch shifts in momentum
- Simulates BUY, SELL, HOLD decisions based on combined indicator logic
- Supports near real-time data using 1-minute interval trading logic
- Logs trades into a CSV file for rewiew
- Uses OOP (Object-Oriented Programming) with a distinct parent/child class structure
- Includes several matplotlib visualizations for RSI strategy review


## Strategies Logic
### Buy Signal
- Short EMA crosses above Long EMA (bullish momentum)
- RSI < 70 (not overbought)
- No open position

### Sell Signal
- Short EMA crosses below Long EMA (bearish momentum)
- RSI > 30 (not oversold)
- User currently holds the stock

### Hold Signal
- No strong buy/sell signal OR advises to hold the next remaining times, even if conditions remain favorable
- Maintain current position

## Modules
- yfinance: fetches stock market data
- pandas: data handling
- numpy: numerical calculations
- matplotlib: visualizations
- time: loop in near real-time

## Structure
├── rsi_ema_bot.py        # Main trading logic with RSI + EMA strategy
├── combined_log.csv      # Output log of simulated trades
├── README.md             # Project documentation

## Disclaimer
This bot is for educational and simulation purposes only. It does not place real trades. Please do your own research and consult financial professionals before investing.
