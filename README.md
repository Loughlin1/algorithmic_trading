# Algorithmic Trading Strategies

This repository contains two algorithmic trading strategies: Mean Reversion Trading Strategy and Black Scholes and Binomial Options Pricing Strategy. Each strategy is implemented and backtested using historical data.

## Mean Reversion Trading Strategy

This strategy uses historical stock prices of S&P 500 ETF (SPY) to identify buy or sell signals based on the stock price deviation from its historical average.

### Steps

1. **Download/Load SP500 stocks prices data**
   - Fetch historical data for a stock (S&P 500 ETF as an example) using `yfinance`.

2. **Define Mean Reversion Strategy**
   - Calculate the moving average and Z-score to identify buy or sell signals based on the stock price deviation from its historical average.

3. **Backtesting Strategy with Backtrader**
   - Implement the strategy in Backtrader where we buy when the Z-score is below -2 (indicating the stock is oversold) and sell when the Z-score is above 2 (indicating the stock is overbought).

4. **Evaluate Strategy Performance**
   - Calculate common performance metrics such as Sharpe ratio, drawdown, and cumulative returns to evaluate the trading strategy.

5. **Summary and Report**
   - Provide a summary of the strategy performance and categorize the Sharpe ratio and drawdown.

### Requirements

- `pandas`
- `numpy`
- `matplotlib`
- `yfinance`
- `backtrader`

## Black Scholes and Binomial Options Pricing Strategy

This strategy uses the Black Scholes and Binomial models to price European and American options, respectively. It also calculates the Greeks to measure the sensitivity of the option's price to various factors.

### Background Information

Options are financial derivatives that give the holder the right (but not the obligation) to buy or sell an asset at a predetermined price before a specified date. The **Black-Scholes** model is a widely used formula for pricing European-style options, while the **Binomial model** is more flexible for American-style options. The **Greeks** (Delta, Gamma, Vega, Theta, and Rho) are key metrics derived from option pricing models that describe the risk sensitivities of the option.

### Steps

1. **Build the Option Pricing Model**
   - Implement the **Black-Scholes** or **Binomial pricing model** in Python to calculate the theoretical price of options.

2. **Calculate the Greeks**
   - Compute the **Greeks** of options, which measure the sensitivity of the option's price to various factors such as changes in the underlying asset price, volatility, and time.

3. **Develop a Trading Strategy**
   - Build a basic **options trading strategy** using the Greeks and market data. Focus on a delta-neutral trading strategy to eliminate directional risk.

4. **Portfolio Optimization and Risk Management**
   - Optimize the portfolio and manage risk using techniques such as position sizing, risk-adjusted returns, and risk metrics like **maximum drawdown** and **Sharpe ratio**.

### Requirements

- `numpy`
- `pandas`
- `yfinance`
- `scipy`
- `matplotlib`
