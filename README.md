# 📊 Portfolio Optimization: Minimum Variance & Maximum Sharpe Ratio

This project implements and compares two foundational portfolio optimization strategie using `Python`:

- **Minimum Variance Portfolio (MVP)**
- **Maximum Sharpe Ratio Portfolio (MSRP)**


The data is collected using **[yfinance](https://pypi.org/project/yfinance/)** and the strategies are built and implemented manually from scratch using **[NumPy](https://pypi.org/project/numpy/)**, **[Pandas](https://pypi.org/project/pandas/)**, and **[SciPy](https://pypi.org/project/scipy/)**. Results are then validated against outputs from the **[PyPortfolioOpt](https://pypi.org/project/pyportfolioopt/)** library.

---

## 🎯 Objective

The primary goal of this project is to demonstrates practical applications of quantitative portfolio optimization by:

+ Estimating expected returns and the covariance matrix from historical stock data.
+ Constructing MVP and MSRP portfolios manually by formulating and solving constrained optimization problems for portfolio allocation.
+ Implement both MVP and MSRP using `scipy.optimize`.
+ Validating results with the `PyPortfolioOpt` library.
+ Visualizing weights, volatility, and comparing results.
+ Markdown commentary aboce each code block for transparency and better understanding.

---

## 🧾 Assets & Data

The portfolio includes ten large-cap U.S. stocks from diverse sectors:

| Ticker | Company                     |
|--------|-----------------------------|
| AAPL   | Apple Inc.                  |
| GOOGL  | Alphabet Inc.               |
| JPM    | JPMorgan Chase & Co.        |
| XOM    | Exxon Mobil Corp            |
| NVDA   | NVIDIA Corporation          |
| TSLA   | Tesla Inc.                  |
| PG     | Procter & Gamble Co.        |
| V      | Visa Inc.                   |
| JNJ    | Johnson & Johnson           |
| CAT    | Caterpillar Inc.            |


- **Data Source**: Yahoo Finance via the `yfinance` API
- **Date Range**: January 1, 2020 – January 1, 2025
- **Frequency**: Daily adjusted closing prices

---

## 📈 Methodology

### 🛠 Manual Implementation
- Daily returns and annualized expected returns estimated with `pandas`
- Annualized covariance matrix calculated as `returns.cov() * 252`
- MVP: Objective is to **minimize portfolio variance**
- MSRP: Objective is to **maximize the Sharpe Ratio**, assuming a **risk-free rate of 3%**
- Optimization solved using `scipy.optimize.minimize` (SLSQP)

### 📦 Library-Based Validation (PyPortfolioOpt)
- `PyPortfolioOpt` used to generate MVP and MSRP portfolios using historical return and risk models
- `.min_volatility()` and `.max_sharpe()` methods used for optimization
- `.clean_weights()` used to clean final allocations
- Manual and library results compared using plots

---

## ⚙️ Environment Setup

To run this project on your local machine, you can choose one of the following setup methods:

---

### ✅ Option 1: Clone the Repository & Use Conda Environment (Recommended)

This method ensures that all dependencies are installed with the correct versions.

```bash
# Step 1: Clone the repository
git clone https://github.com/Mahedalii/portfolio-optimization-mvp-msrp.git
cd portfolio-optimization-mvp-msrp

# Step 2: Create the Conda environment
conda env create -f environment.yml

# Step 3: Activate the environment
conda activate portfolio-opt
```

📁 The `environment.yml` file is included in this repo and contains all required packages.

---

### ✅ Option 2: Manual Setup with pip (No Conda Required)

If you're not using Conda, you can manually install the dependencies:

```bash
pip install numpy pandas scipy matplotlib seaborn yfinance PyPortfolioOpt ipykernel
```

---

## 📦 Dependencies

+ `numpy`
+ `pandas`
+ `scipy`
+ `matplotlib`
+ `seaborn`
+ `yfinance`
+ `PyPortfolioOpt`
+ `ipykernel`

---

## 📬 Contact

**Mahed Ali**  
🎓 M.Sc. Quantitative Finance - University of Bologna  
📧 mahed.ali@hotmail.com | 🔗 **[LinkedIn](https://www.linkedin.comin/mahedali)** | 💻 **[GitHub](https://github.com/Mahedalii/portfolio-optimization-mvp-msrp)**

---

## 🧩 License

Distributed under the MIT License. See `LICENSE` for details. This project is shared for educational and learning purposes.
