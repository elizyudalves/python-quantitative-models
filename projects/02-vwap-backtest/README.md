# VWAP and five-condition backtest

Compares 2–5 confirmations using previous close, daily volatility, VWAP and moving averages.

**Status: exploratory research; not production validated.**

## Limitations
Default transaction costs and slippage are zero. Position sizing uses fractional 1x notional exposure; it does not model actual WIN/WDO contract multipliers, margin or integer contracts. There is no fixed stop/target. Session completeness filters can exclude observations. Results are exploratory, without an untouched out-of-sample evaluation.

Original source: `backtest5variaveis.ipynb`. Outputs cleared for publication. Analytical code preserved.

## Run
From the repository root, install the dependencies described in the main README, launch Jupyter, open `analysis.ipynb`, review the configuration and run cells in order. Network access to TradingView is required. Historical availability and symbol permissions may differ.

No raw market data or old performance outputs are bundled. Successful live execution has not been verified in this review.
