# Modern Portfolio Theory: Portfolio Optimization with Python

A practical mathematics and Python project exploring **how portfolio allocation affects investment risk and expected return**. The analysis uses four technology stocks: **AAPL, MSFT, GOOG, and AMZN**.

## Methods

- Calculate returns, volatility, covariance, and the Sharpe ratio.
- Simulate **5,000 portfolios** with Monte Carlo sampling.
- Use **SciPy SLSQP** to find the minimum-variance and maximum-Sharpe portfolios.
- Visualize the **efficient frontier** and test allocation constraints.
- Evaluate the portfolios on **32 later weeks** excluded from model fitting.

## Key results

| Portfolio | 32-week test return | Annualized test volatility |
|---|---:|---:|
| Equal-weight benchmark | 25.66% | 13.41% |
| Minimum variance | **30.17%** | 14.17% |
| Maximum Sharpe | 22.47% | 14.39% |

The minimum-variance portfolio had the highest return in this test period, **but not the lowest realized volatility**. Training-sample optimization does not guarantee future performance.

## Run the project

Use **Python 3.10+**, then run from the project directory:

```bash
python -m pip install -r requirements.txt
jupyter notebook portfolio_optimization.ipynb
```

Open the notebook and select **Run All**. The dataset is included, so no API key or internet access is required.

## Project files

- `portfolio_optimization.ipynb` — mathematics, code, charts, and conclusions.
- `data/` — normalized historical stock indices (2018–2019).
- `figures/` — generated visualizations.
- `results/` — experiment results in CSV format.
- `requirements.txt` — Python dependencies.

## References and limitations

Data: [Plotly sample stocks](https://plotly.com/python-api-reference/generated/plotly.data.html). Theory: [Markowitz (1952)](https://doi.org/10.1111/j.1540-6261.1952.tb01525.x). Optimization: [SciPy SLSQP](https://docs.scipy.org/doc/scipy/reference/optimize.minimize-slsqp.html).

The sample is short and concentrated in technology stocks. The analysis assumes frictionless weekly rebalancing and a hypothetical **2% annual risk-free rate** for the main Sharpe calculation. **Historical results are not forecasts or investment advice.**