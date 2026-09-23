# econ3916-lab02-deflation
# Deflating Economic Data — Nominal vs. Real

## Objective
This project demonstrates how to isolate real (inflation-adjusted) economic
trends from nominal dollar figures, using CPI-based deflation applied to
U.S. wage and Big Mac price data.

## Methodology
- Pulled CPI (CPIAUCSL) and average hourly earnings series from FRED via a
  public, no-API-key data path
- Implemented a reusable `deflate_series(nominal, cpi, base_year)` function
  to convert nominal series into constant-dollar terms for any base year
- Applied `.asof()` alignment to match semi-annual Big Mac price data against
  monthly CPI readings
- Converted average hourly earnings to constant 2020 dollars and compared
  against the nominal series
- Computed compounded (multiplicative) percentage change across nominal,
  real, and CPI series to verify internal consistency of the deflation
- Built an interactive explorer (ipywidgets + matplotlib) with a series
  selector, base-year slider, and nominal/real toggle for exploratory
  analysis

## Key Findings
- Nominal hourly earnings rose from $2.50 to $32.53
- Real hourly earnings (2020 $) moved from $20.92 to $25.20
- Big Mac price: nominal + 178 %, real + 43%, with CPI
  rising + 95 % over the same period
- Big mac prices move faster once inflation was removed. Big mac prices grew at a faster rate compared to real hourly earnings. 
