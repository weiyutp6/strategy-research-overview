# Strategy Research Overview

A description of the research directions behind my quantitative work. This repository contains **no code, parameters, thresholds, position sizes or data**: those are kept private. It states the ideas and how each was tested.

## Statistical arbitrage and mean reversion

- **Same-issuer share-class spread.** Model the log price ratio of two share classes, standardise it with rolling statistics, estimate mean-reversion speed with an AR(1) fit, and test entry and exit rules by backtest, including scaling into a position as the spread widens.
- **Gold ETF against gold-miner equity.** A spread signal combined with a volatility regime filter: reversal-confirmed entries, exits when the spread normalises, and trading switched off in high-volatility regimes. Evaluated with a vectorised backtest.

## Volatility

- **Volatility-spike studies.** Define a spike relative to a short moving average of the VIX and compare option structures (outright, vertical and calendar spreads) over spike episodes with a Black-Scholes backtest. Related volatility-of-volatility work.
- **Premium selling on index ETFs.** Short-dated call selling conditioned on the volatility level and recent drawdown behaviour, with the cut-off between taking and skipping a day studied as a function of past moves.
- **Neuroevolution (NEAT).** Evolved networks that map volatility-index and index-ETF features to positions, with GARCH-based features.

## Credit and rates

- **Credit-cycle signal.** The high-yield to investment-grade spread as a rolling z-score, compared with the price of a listed credit vehicle and with the convexity of the short-rate futures curve.
- **Treasury-yield binary contracts.** Pricing from a calibrated short-rate model, screening of contracts by model fair value, and quoting rules. The pricing and quoting framework is public in [cir-treasury-pricing](https://github.com/weiyutp6/cir-treasury-pricing) and [kalshi-autoquoter-framework](https://github.com/weiyutp6/kalshi-autoquoter-framework).

## Prediction markets

- Fair-probability models against live order books, fractional-Kelly sizing and a paper-trading execution layer: [mlb-prediction-market-framework](https://github.com/weiyutp6/mlb-prediction-market-framework).

For research and education only. Not investment advice.
