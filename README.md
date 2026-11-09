# Gold Trading Analysis

Analysis of my own real-money gold trading (XAU/USD) on MetaTrader 5, January to May 2026. I logged every trade, measured performance and tested whether the result was skill or luck.

## Results

| Metric | Value |
| --- | --- |
| Trades | 74 |
| Win rate | 40.5% (30 of 74) |
| Average win / average loss | €13.90 / €8.36 |
| Win/loss ratio | 1.66:1 (break-even at this win rate: 1.47:1) |
| Net result | +€49 |
| Max drawdown | €134 |
| Longest losing streak | 16 trades |

P/L is in euros and excludes spreads and commissions.

## Key findings

- **Profitable on paper.** A 1.66:1 win/loss ratio beat the 1.47:1 needed to break even at a 40.5% win rate.
- **Position size hurt returns.** 0.01-lot trades made +€144; all 3 trades at 0.05 lots lost (−€95), cutting the overall result by two-thirds.
- **Not statistically significant.** A one-sample t-test gives p ≈ 0.32, and a bootstrap puts the 95% range for the net result at roughly −€158 to +€251. 74 trades is not enough to tell skill from luck.
- **Late drawdown.** Performance peaked at +€183 after trade 58, followed by 16 consecutive losses.

## Files

| File | What it contains |
| --- | --- |
| `Gold_Trading_Performance_Sriya_Sambaturu.xlsx` | Full trade log (result, lot size, gold move, P/L) and a summary sheet with formulas, breakdowns by lot size and phase, and an equity curve |
| `gold_trading_significance.ipynb` | Python notebook: t-test and bootstrap on per-trade P/L |

## How to run the notebook

Open it in [Google Colab](https://colab.research.google.com) (File → Upload notebook) or Jupyter, then run all cells. Requires `numpy` and `scipy`.

## Tools

MetaTrader 5 · Excel · Python (NumPy, SciPy)
