# Asset Price Modeling

This project demonstrates asset price modeling using Wiener processes and Geometric Brownian Motion.

## Business context

Financial markets move. A trader, investor, or analyst must work with that motion. Financial analysis begins with a core observation: prices vary over time. That variation --- across equities, bonds, currencies, commodities, and derivatives --- follows no clean path. To understand it, we need time series models. To manage it, we need probability.

Quantitative finance includes several strands of analysis. Cross-sectional analysis compares asset characteristics at a single point in time. Fundamental analysis examines economic and company-specific data to assess valuation. Technical analysis looks for patterns in price and volume data.

Time series analysis stands apart. It focuses on prices across time. It assumes that past values and statistical properties can inform future behavior. This allows for forecasting, risk modeling, option pricing, and strategy design. A chart is not enough. You must model the process that generates the price.

## Project Structure

```
.
├── README.md           # This file
├── main.py            # Main entry point
├── config.yaml        # Configuration file
├── requirements.txt   # Python dependencies
├── src/               # Core functions
│   ├── core.py        # Asset modeling functions
│   └── plotting.py    # Tufte-style plotting utilities
├── tests/             # Unit tests
├── data/              # Data files
└── images/            # Generated plots and figures
```

## Configuration

Edit `config.yaml` to customize:
- Wiener process parameters (n_steps, T)
- GBM parameters (S0, mu, sigma, T, n_steps)
- Output settings

## Models

### Wiener Process (Brownian Motion)
- Continuous-time stochastic process
- Independent increments
- Normal distribution

### Geometric Brownian Motion (GBM)
- Standard model for stock prices
- S(t) = S₀ exp((μ - 0.5σ²)t + σW(t))
- Parameters: drift (μ) and volatility (σ)

## Caveats

- Simulations use random number generation. Set seed in config for reproducibility.
- GBM assumes constant drift and volatility.
- Step size affects simulation accuracy.

## Disclaimer

Educational/demo code only. Not financial, safety, or engineering advice. Use at your own risk. Verify results independently before any production or operational use.

## License

MIT — see [LICENSE](LICENSE).