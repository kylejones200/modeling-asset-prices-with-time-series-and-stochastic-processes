# Modeling Asset Prices with Time Series and Stochastic Processes How randomness, probability, and the Wiener process shape modern
financial modeling

### Modeling Asset Prices with Time Series and Stochastic Processes 

#### How randomness, probability, and the Wiener process shape modern financial modeling
Financial markets move. A trader, investor, or analyst must work with that motion. Financial analysis begins with a core observation: prices vary over time. That variation --- across equities, bonds, currencies, commodities, and derivatives --- follows no clean path. To understand it, we need time series models. To manage it, we need probability.

Quantitative finance includes several strands of analysis. Cross-sectional analysis compares asset characteristics at a single point in time. Fundamental analysis examines economic and company-specific data to assess valuation. Technical analysis looks for patterns in price and volume data.

Time series analysis stands apart. It focuses on prices across time. It assumes that past values and statistical properties can inform future behavior. This allows for forecasting, risk modeling, option pricing, and strategy design. A chart is not enough. You must model the process that generates the price.

### Time Series and the Randomness of Prices
Price series contain structure, but also noise. This randomness makes financial time series different from temperature, electricity usage, or manufacturing output. Stock prices may trend, but they do not do so cleanly. Prices may revert, but not predictably. Noise dominates signal at short horizons.

This randomness is the core feature of financial markets. Traders act on news. Algorithms compete for millisecond advantage. Information flows are irregular, and reactions vary. Every price is the result of supply and demand under uncertainty. That makes modeling a game of probability.

### Why Probabilistic Models Matter
Deterministic models cannot explain markets. You cannot say what the price of crude oil will be next Thursday. But you can say something about its expected return or volatility. Probabilistic models describe the distribution of future outcomes. That allows analysts to compute risk, simulate paths, and construct hedges.

This is not guesswork. It is formal and structured. It begins with basic assumptions about price behavior, then builds models to match. The most common foundation is a continuous-time stochastic process. For financial applications, that means the Wiener process.

### The Wiener Process
The Wiener process models continuous randomness. It has four properties:

1.  [The process starts at zero.]
2.  [Increments are independent.]
3.  [Increments follow a normal distribution.]
4.  [Increments scale with time.]

Let W(t) be a Wiener process. Then for s\<t, the increment


.

This means that the change in the process over any time interval is normally distributed with zero mean and variance equal to the length of the interval.


<figcaption>The Wiener process represents pure randomness with no drift. It starts at zero and accumulates normally distributed increments.</figcaption>


The Wiener process is the building block of Brownian motion. It underlies nearly every model in continuous-time finance, from the Black-Scholes equation to interest rate models. It captures the idea of market unpredictability while still allowing structured analysis.


<figcaption>The Geometric Brownian Motion (GBM) shows how asset prices evolve when you exponentiate a drifted Wiener process. It avoids negative prices and reflects both growth (drift) and uncertainty (volatility).</figcaption>


### The Lognormal Random Walk
Asset prices cannot follow a normal distribution. A normal distribution allows for negative values. Prices do not. To address this, we model the *returns* of assets as normal, and the *prices* as lognormal.

Let S(t) be the price of an asset at time t. We define its evolution as:


This is the stochastic differential equation for geometric Brownian motion. Here, μ is the expected return, σ is the volatility, and dW(t) is the increment of a Wiener process. Solving this gives:


This expression shows that the logarithm of the price follows a normal distribution. Therefore, the price itself follows a lognormal distribution.

This model is the foundation of modern finance. It powers the Black-Scholes option pricing formula. It underpins most Value-at-Risk calculations. It serves as the base case for equity, currency, and commodity modeling. Despite its limitations --- constant volatility, no jumps, no memory --- it remains the most important model in finance. Financial analysis must work with randomness. Time series models, grounded in probability, offer a path forward. The Wiener process models noise in a mathematically precise way. When used in a lognormal framework, it leads to a workable model of asset prices.

This model predicts distribution (not price). From there, we can estimate risk, simulate returns, price derivatives, and build strategies. Quantitative finance begins not with certainty, but with randomness --- structured, measured, and modeled.
