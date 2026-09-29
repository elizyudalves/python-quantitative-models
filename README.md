# Python Quantitative Models

Exploratory financial time-series research portfolio — Elizângela Alves.

This repository contains two selected studies from a larger research archive. It demonstrates Python workflows, financial data processing, configurable models and reporting. It does not establish a profitable trading strategy or production readiness.

| Study | Methods | Review status |
|---|---|---|
| [GARCH volatility](projects/01-garch-volatility/) | GARCH(1,1), Student-t innovations, multiple forecast horizons | Static review; live execution and forecast validation pending |
| [VWAP backtest](projects/02-vwap-backtest/) | OHLCV validation, lagged daily features, VWAP, moving averages, performance reporting | Static review; live execution and out-of-sample validation pending |

## Setup

Use a separate Python environment:

```bash
python -m venv .venv
# Windows:
.venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
python -m pip install -r requirements.txt
python -m pip install git+https://github.com/rongardF/tvdatafeed.git
python -m jupyter lab
```

The tvDatafeed source URL comes from the original notebook. Installation and current compatibility were not tested here. Dependencies are an inferred starting list, not a validated lockfile. Inspect third-party source before installation. Data access depends on availability, permissions and provider terms.

## Configuration and execution

Open a project notebook and review its symbol, exchange, timeframe and output configuration. Run cells in order. The VWAP notebook includes an execution cell that downloads data and writes reports. The GARCH notebook runs its main routine when its code cell executes.

Keep credentials out of committed files. VWAP reads TV_USER and TV_PASSWORD from environment variables. The GARCH example defaults to anonymous access; do not insert passwords into a public notebook.

## Interpretation

Read each project's limitations. Volatility is not direction or expected profit. Backtest statistics depend on data, execution conventions, costs and sample selection. No historical result is promoted as verified out-of-sample performance.

## Provenance

Prepared from notebooks supplied by the portfolio owner. Formatting and documentation were assisted by AI; analytical code in the selected notebooks was preserved. The owner should complete acknowledgements for course-derived or third-party portions before publishing. No open-source license has been assigned by this preparation step.

## Português

Dois estudos exploratórios selecionados e documentados. Os notebooks tiveram as saídas e metadados locais removidos. A lógica foi preservada; não houve download de dados nem validação de rentabilidade. Consulte `REVISAO_PT.md` para os achados e próximos passos.
