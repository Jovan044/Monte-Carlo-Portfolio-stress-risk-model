# Monte Carlo Portfolio Stress & Risk Model

A 1-year Monte Carlo simulation model in Python (`NumPy`, `Matplotlib`, and `pandas`) built in Google Colab to evaluate expected returns, 95% Value at Risk (VaR), and equity stress-test downside for a multi-asset portfolio.

## Portfolio & Market Assumptions (1-Year Horizon)
* **Starting Capital:** `100,000`
* **Asset Allocation:**
  * **Equity (Nifty 50 TRI benchmark):** `60%` — Expected Return: `12.4%`, Volatility: `18.0%`
  * **Bonds (Indian G-Sec / Fixed Income benchmark):** `30%` — Expected Return: `7.5%`, Volatility: `5.0%`
  * **Gold (Domestic Gold benchmark):** `10%` — Expected Return: `11.5%`, Volatility: `14.0%`
* **Simulation Runs:** `10,000` independent random draws from normal return distributions per asset.

## Stress Test Scenario
To test resilience during an equity downturn, the stress scenario adjusts **Equity** assumptions while keeping Bonds and Gold at baseline inputs:
* **Stressed Equity Expected Return:** `4.0%` (down from `12.4%`)
* **Stressed Equity Volatility:** `30.0%` (up from `18.0%`)

## Key Risk & Return Takeaways
* **Mean vs. Tail Risk:** While average ending capital only moderates during an equity stress test (supported by 30% bonds and 10% gold), **1-Year 95% VaR** rises sharply—showing why tail-risk percentiles matter more than averages alone during market shocks.
* **Visual Comparison:** Includes an overlapping histogram comparing Normal vs. Stress ending capital distributions relative to starting capital.

## Tools Used
* **Python** (`NumPy`, `Matplotlib`, `pandas`)
* **Google Colab**
