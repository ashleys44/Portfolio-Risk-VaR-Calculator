# Portfolio-Risk-VaR-Calculator

**Tech stack:** Python (pandas, numpy, scipy), SQLite/Postgres-compatible workflow, matplotlib

This project demonstrates a portfolio risk analytics pipeline that:
- Ingests historical price data (example uses synthetic data for a stock, crypto, and FX pair)
- Stores price series in a SQL database (SQLite for the demo)
- Computes daily returns, annualized volatility, and the covariance matrix
- Calculates **historical VaR** (percentile-based) and **Monte Carlo VaR** (parametric simulation)
- Produces plots and a short summary report

## How to run (locally)
1. Create a Python virtual environment and install requirements:
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```
2. Run the pipeline (uses SQLite by default):
```bash
python src/run_pipeline.py --db sqlite:///./risk_data.db
```
3. Inspect outputs in `outputs/` and the DB `risk_data.db`.
