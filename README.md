<div align="center">
  <h1>Hi, I'm Terry </h1>
  <h3>Medicinal Chemistry Student @ The University of Edinburgh | Lead Operations Analyst at SFI Partners</h3>

  <p>Building clean models, analyzing complex data, and actively bridging between sports and finance.</p>

  <a href="https://www.linkedin.com/in/scoterry"><img src="https://img.shields.io/badge/LinkedIn-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:s2209113@ed.ac.uk"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
</div>

---

### 👨‍💻 About Me

I am a driven Medicinal Chemistry student with a strong foundation in mathematics and programming. I specialize in turning raw data into actionable insights and am passionate about writing clean, reproducible code.

* 🎓 **Education:** B.Sc. in Medicinal Chemistry, The University of Edinburgh (Expected Graduation: May 2028)
* 🌱 **Currently learning:** Model Deployment, Time-Series Forecasting, Machine Learning
* 💼 **Looking for:** Data Science or Machine Learning Internships
* ⚡ **Fun fact:** I served as a tank driver at the Korean army for 18 months

---

### 🛠️ Tech Stack & Tools

* **Languages:** Python, SQL
* **Data & modelling:** pandas, NumPy, SciPy, statsmodels, scikit-learn, LightGBM, XGBoost, PyMC, ArviZ, Matplotlib, pytest
* **Quant methods:** backtesting with full cost models, Monte Carlo simulation, extreme-value tail risk, structural-break tests, event studies, option pricing (Black-76), small-sample exact tests
* **Finance:** three-statement forecasting, DCF and trading multiples, fund share-class design, currency hedging, counterparty stress tests
* **Market data:** Binance, Bybit, Hyperliquid, Deribit, Upbit, Bithumb, Coinbase, DefiLlama, FRED, Yahoo Finance, StatsBomb, Transfermarkt
* **Tools:** Git, GitHub, Jupyter, Docker, Claude Code

---

### 📈 Quantitative Finance Projects

Every repo runs end to end with one command, keeps all assumptions in `config.yaml`, and ships tests plus a mutation check that confirms the tests catch deliberate bugs.

#### 1. **[One stock, three prices: Korean equity perpetuals](https://github.com/scotankboi/korea-equity-perp-carry)**
* **Tech Stack:** pandas, NumPy, SciPy, statsmodels, pyarrow, yfinance
* **What I Did:** Built a hedged-carry backtest for SK hynix and Samsung that buys the KRX shares and shorts the perpetual on Hyperliquid and Binance. It covers funding, Korea's 0.20% sell tax, margin risk and market-impact capacity. A second chapter tests whether pre-IPO perps predicted the first trade better than the offer price.
* **Impact/Results:** Found a structural break in the carry: SK hynix funding fell from 66% a year to 18% after mid-July 2026. Capacity at post-break carry is about $14–16m on Hyperliquid. In the pre-IPO chapter, the perp was closer to the first trade than the offer in 5 of 7 listings, but shorts at maximum leverage would have been liquidated in 4 of them.

#### 2. **[One carry, five investors: share classes for a bitcoin basis strategy](https://github.com/scotankboi/crypto-carry-share-classes)**
* **Tech Stack:** pandas, NumPy, SciPy, pyarrow, Matplotlib
* **What I Did:** Took one market-neutral BTC carry book and modelled what it delivers as USDT, USD, yen-hedged, won-hedged and bitcoin share classes. This includes daily-marked FX forwards, fees with a high-water mark, a replay of the FTX bankruptcy using its actual repayment schedule, and a covered-call overlay for the BTC class priced with Black-76.
* **Impact/Results:** The master earned 7.7% a year with a monthly, autocorrelation-adjusted Sharpe of 0.54 (the naive daily figure is 4.3). After fees the USD class earns 4.9% while the BTC class loses 7.1% in BTC. In the FTX replay the USD class loses 3.0% of NAV and the BTC class 37%.

#### 3. **[Kimchi premium: why arbitrage does not close it](https://github.com/scotankboi/kimchi-premium)**
* **Tech Stack:** pandas, NumPy, Requests, Matplotlib
* **What I Did:** Built an hourly pipeline of Upbit, Bithumb, Binance and FRED data back to 2017. I split Korea's BTC premium into a USDT part and a crypto-specific part, then backtested hedged arbitrage under the US$100k annual remittance cap.
* **Impact/Results:** About 99% of the premium is the won price of USDT. Under the cap, arbitrage earns one person about $1.4k in a median year, so the cap, not a lack of opportunity, keeps the premium alive.

#### 4. **[Stablecoin depegs under stress](https://github.com/scotankboi/stablecoin-peg-monitor)**
* **Tech Stack:** pandas, NumPy, Requests, Matplotlib
* **What I Did:** Measured depeg depth, recovery time and redemptions for USDT, USDC, DAI, UST, BUSD and USDe across five stress events, using hourly USD quotes from several venues.
* **Impact/Results:** In the SVB event, hourly data shows USDC at $0.86, against $0.96 in daily data. It took 53 hours to return within 1% and lost 25% of supply in 30 days. In October 2025, USDe hit $0.65 on Binance but $0.93 on Bybit in the same hour, so its depeg was venue-local.

---

### ⚽ Sports Finance Projects (SFI Partners)

#### 5. **Premier League Club Financial Forecasting Engine**
* **Tech Stack:** Python, pandas, NumPy, Monte Carlo simulation
* **What I Did:** Led a five-person team building an engine that forecasts all three financial statements for every Premier League club to FY2029. It uses 303 club-years of filed accounts, simulates seasons from betting odds, and tests clubs against the League's cost-control rules.
* **Impact/Results:** Across 194 rolling out-of-sample forecasts it beat a no-change benchmark on key lines, with a Premier League revenue error (WAPE) of 11% against 14%.

#### 6. **Player Valuation Model**
* **Tech Stack:** LightGBM, pandas, StatsBomb event data, Transfermarkt
* **What I Did:** Built position-specific LightGBM models that value 2,898 players on real 2025/26 market values. Features include Expected Threat computed from 234,637 StatsBomb World Cup 2022 events, plus a Heckman correction for selection bias.
* **Impact/Results:** 5-fold cross-validation gives R² 0.83 on log value and a rank correlation of 0.92.

#### 7. **World Cup 2026 Advanced Simulator**
* **Tech Stack:** Pandas, NumPy, PyMC, ArviZ, Matplotlib, Scikit-Learn
* **What I Did:** Built a Bayesian match model for the 2026 World Cup, fitted with MCMC on historical results and standardised attacking efficiency, and ran the tournament through a Monte Carlo engine.
* **Impact/Results:** Produces match outcome and progression probabilities for every team.

---

### 🧪 Other Projects

* **Alpha-Hunter Paper Trading Bot (Mock Mode):** an autonomous KOSPI paper-trading bot with a vectorized simulation engine, an XGBoost signal model and KIS VTS API execution (pandas, XGBoost, scikit-learn, TA, yfinance).
