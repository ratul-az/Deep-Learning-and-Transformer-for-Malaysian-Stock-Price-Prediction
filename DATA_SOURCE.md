# Data Source and Dataset Notes

## Source

The notebook downloads historical market data at runtime using the `yfinance` Python package, which accesses Yahoo Finance data.

## Instruments

| Company | Ticker |
|---|---|
| Maybank | `1155.KL` |
| Petronas Gas | `6033.KL` |
| IHH Healthcare | `5225.KL` |
| Mr. D.I.Y. Group | `5296.KL` |

## Date range

The notebook specifies a start date of `2015-01-01` and an end date of `2026-06-30`. The exact observations returned depend on data availability and the behaviour of the upstream source at execution time.

## No bundled dataset

A separate CSV dataset is not included because the notebook fetches the data when it runs. An internet connection is required for the download step.

## Attribution and terms

Yahoo Finance is the upstream data source. `yfinance` is an open-source Python library and is not affiliated with or endorsed by Yahoo. Review the applicable Yahoo Finance terms and data-use restrictions before redistributing downloaded market data. This repository does not redistribute a downloaded market-data snapshot.
