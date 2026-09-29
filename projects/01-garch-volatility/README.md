# GARCH volatility across multiple horizons

Forecasts conditional volatility over 1, 5 and 21 trading days and ranks a configured asset universe.

**Status: exploratory research; not production validated.**

## Limitations
No out-of-sample forecast evaluation is implemented. The ranking measures volatility, not profitability or liquidity. Bands are multiples of volatility, not calibrated confidence intervals. Check optimizer convergence, residual diagnostics, completed bars and data quality before interpretation.

Original source: `Garchsemanal.ipynb`. Outputs cleared for publication. Analytical code preserved.

## Run
From the repository root, install the dependencies described in the main README, launch Jupyter, open `analysis.ipynb`, review the configuration and run cells in order. Network access to TradingView is required. Historical availability and symbol permissions may differ.

No raw market data or old performance outputs are bundled. Successful live execution has not been verified in this review.
