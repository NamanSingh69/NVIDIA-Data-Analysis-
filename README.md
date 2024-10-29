# NVIDIA Share Analysis

Welcome to the **NVIDIA Share Analysis** project! This comprehensive analysis aims to evaluate NVIDIA's stock performance, financial health, market position, and future prospects by leveraging various data sources and analytical techniques. The project encompasses data collection, cleaning, exploratory data analysis (EDA), technical and financial analysis, competitor benchmarking, sentiment analysis, forecasting, and risk/opportunity identification.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Data Files](#data-files)
- [Images](#images)
- [Installation](#installation)
- [Usage](#usage)
- [Analysis Overview](#analysis-overview)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The **NVIDIA Share Analysis** project is designed to provide an in-depth understanding of NVIDIA's market performance and financial standing. By integrating data from various sources, including stock prices, financial statements, macroeconomic indicators, and news sentiment, the project offers a holistic view of NVIDIA's position in the technology sector. Advanced analytical methods such as time series forecasting, technical indicator computation, and sentiment analysis are employed to derive actionable insights.

## Features

- **Data Collection and Caching:** Efficiently gathers historical stock data, financial statements, options data, and macroeconomic indicators with caching mechanisms to optimize performance and reduce redundant API calls.
- **Data Cleaning and Validation:** Ensures data integrity by handling missing values, removing duplicates, and eliminating outliers.
- **Exploratory Data Analysis (EDA):** Provides descriptive statistics, correlation analysis, and visualizations to uncover underlying patterns and relationships.
- **Technical Analysis:** Computes key technical indicators like MACD, Bollinger Bands, RSI, and identifies support/resistance levels to assess stock performance.
- **Financial Metrics Analysis:** Calculates essential financial ratios and metrics to evaluate NVIDIA's financial health and operational efficiency.
- **Competitor Benchmarking:** Compares NVIDIA's performance with major competitors (AMD, Intel, Micron, TSMC) and relevant market indices (S&P 500, NASDAQ, SOX).
- **Sentiment Analysis:** Analyzes news headlines using VADER and TextBlob to gauge market sentiment towards NVIDIA.
- **Forecasting:** Utilizes Prophet for time series forecasting to predict future stock prices.
- **Risk and Opportunity Identification:** Identifies potential risks and opportunities based on financial metrics, market sentiment, and macroeconomic factors.

## Data Files

The project utilizes several CSV files to store and process data. Below is a summary of each file and its columns:

### **1. NVIDIA Financials**

- **File:** `nvidia_financials_pivoted.csv`
- **Columns:**
  ```
  Date,Tax Effect Of Unusual Items,Tax Rate For Calcs,Normalized EBITDA,Total Unusual Items,
  Total Unusual Items Excluding Goodwill,Net Income From Continuing Operation Net Minority Interest,
  Reconciled Depreciation,Reconciled Cost Of Revenue,EBITDA,EBIT,Net Interest Income,
  Interest Expense,Interest Income,Normalized Income,Net Income From Continuing And Discontinued Operation,
  Total Expenses,Total Operating Income As Reported,Diluted Average Shares,Basic Average Shares,
  Diluted EPS,Basic EPS,Diluted NI Availto Com Stockholders,Net Income Common Stockholders,
  Net Income,Net Income Including Noncontrolling Interests,Net Income Continuous Operations,Tax Provision,
  Pretax Income,Other Income Expense,Other Non Operating Income Expenses,Special Income Charges,
  Restructuring And Mergern Acquisition,Net Non Operating Interest Income Expense,
  Interest Expense Non Operating,Interest Income Non Operating,Operating Income,Operating Expense,
  Research And Development,Selling General And Administration,Gross Profit,Cost Of Revenue,Total Revenue,
  Operating Revenue,Treasury Shares Number,Ordinary Shares Number,Share Issued,Net Debt,Total Debt,
  Tangible Book Value,Invested Capital,Working Capital,Net Tangible Assets,Capital Lease Obligations,
  Common Stock Equity,Total Capitalization,Total Equity Gross Minority Interest,Stockholders Equity,
  Gains Losses Not Affecting Retained Earnings,Other Equity Adjustments,Treasury Stock,
  Retained Earnings,Additional Paid In Capital,Capital Stock,Common Stock,Preferred Stock,
  Total Liabilities Net Minority Interest,Total Non Current Liabilities Net Minority Interest,
  Other Non Current Liabilities,Employee Benefits,Tradeand Other Payables Non Current,
  Non Current Deferred Liabilities,Non Current Deferred Revenue,Non Current Deferred Taxes Liabilities,
  Long Term Debt And Capital Lease Obligation,Long Term Capital Lease Obligation,Long Term Debt,
  Current Liabilities,Other Current Liabilities,Current Deferred Liabilities,Current Deferred Revenue,
  Current Debt And Capital Lease Obligation,Current Capital Lease Obligation,Current Debt,
  Other Current Borrowings,Current Provisions,Payables And Accrued Expenses,Change In Prepaid Assets,
  Change In Inventory,Change In Receivables,Changes In Account Receivables,Other Non Cash Items,
  Stock Based Compensation,Deferred Tax,Deferred Income Tax,Depreciation Amortization Depletion,
  Depreciation And Amortization,Operating Gains Losses,Gain Loss On Investment Securities,
  Net Income From Continuing Operations
  ```

### **2. Stock Data**

- **Files:**
  - `AMD_stock_data.csv`
  - `INTC_stock_data.csv`
  - `MU_stock_data.csv`
  - `nvidia_stock_data.csv`
  - `TSM_stock_data.csv`
- **Columns:**
  ```
  Date,Open,High,Low,Close,Adj Close,Volume
  ```

- **Cleaned Versions:**
  - `AMD_stock_data_cleaned.csv`
  - `INTC_stock_data_cleaned.csv`
  - `MU_stock_data_cleaned.csv`
  - `nvidia_stock_data_cleaned.csv`
  - `TSM_stock_data_cleaned.csv`
- **Columns:**
  ```
  Date,Open,High,Low,Close,Adj Close,Volume
  ```

### **3. Macroeconomic Data**

- **Files:**
  - `macroeconomic_data.csv`
  - `macroeconomic_data_cleaned.csv`
- **Columns:**
  ```
  Date,GDP,Unemployment_Rate,Inflation_Rate,Interest_Rate
  ```

### **4. Market Capitalization Data**

- **File:** `market_caps.csv`
- **Columns:**
  ```
  Company,Market Cap (in billion USD),Market share %
  ```

### **5. NVIDIA Options Data**

- **Files:**
  - `nvidia_options_calls.csv`
  - `nvidia_options_puts.csv`
- **Columns:**
  ```
  contractSymbol,lastTradeDate,strike,lastPrice,bid,ask,change,percentChange,
  volume,openInterest,impliedVolatility,inTheMoney,contractSize,currency
  ```

### **6. Forecasting Data**

- **File:** `nvidia_price_forecast.csv`
- **Columns:**
  ```
  ds,trend,yhat_lower,yhat_upper,trend_lower,trend_upper,additive_terms,
  additive_terms_lower,additive_terms_upper,daily,daily_lower,daily_upper,
  weekly,weekly_lower,weekly_upper,yearly,yearly_lower,yearly_upper,
  multiplicative_terms,multiplicative_terms_lower,multiplicative_terms_upper,yhat
  ```

### **7. Sentiment Analysis Data**

- **File:** `nvidia_sentiment_data.csv`
- **Columns:**
  ```
  Headline,VADER_Sentiment,TextBlob_Sentiment
  ```

### **8. Technical Indicators Data**

- **File:** `nvidia_stock_data_with_indicators.csv`
- **Columns:**
  ```
  Date,Open,High,Low,Close,Adj Close,Volume,MACD,Signal_Line,Upper_BB,Lower_BB,RSI
  ```

### **9. Market Indices Data**

- **Files:**
  - `sox_data.csv`
  - `sp500_data.csv`
- **Columns:**
  ```
  Date,Open,High,Low,Close,Adj Close,Volume,Daily_Return,Log_Return,
  Volatility,SMA_50,SMA_200,RSI
  ```

## Images

The project generates various visualizations to illustrate the analysis findings. All images are stored in the `images/` directory and include:

- **nvidia_vs_indices_performance.png:** Comparative cumulative returns of NVIDIA vs. market indices.
- **nvidia_financial_metrics.png:** Trends of NVIDIA's key financial metrics over time.
- **nvidia_competitor_correlation.png:** Correlation heatmap between NVIDIA and its competitors.
- **nvidia_technical_indicators_with_support_resistance.png:** Technical indicators plotted alongside support and resistance levels.
- **nvidia_sentiment_analysis.png:** Sentiment scores from news headlines.
- **nvidia_risks_opportunities.png:** Bar chart depicting identified risks and opportunities.
- **market_share_and_stock_price.png:** NVIDIA's market share evolution and stock price trends.
- **market_share_vs_stock_price_scatter.png:** Scatter plots showing correlations between market share and stock price.
- **nvidia_stock_product_launches.png:** Stock price movements around product launch dates.
- **nvidia_stock_global_events.png:** Stock price movements around significant global events.
- **nvidia_price_forecast.png:** Forecasted stock prices on linear and logarithmic scales.
- **nvidia_call_option_prices_refined.png:** Refined call option prices across different expiration dates.
- **nvidia_stock_split_YYYY-MM-DD.png:** Analysis of stock splits on specified dates.

## Installation

To set up and run the **NVIDIA Share Analysis** project, follow these steps:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/nvidia-share-analysis.git
   cd nvidia-share-analysis
   ```

2. **Create a Virtual Environment (Optional but Recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Required Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

   **Note:** Ensure you have `pip` installed and updated. The `requirements.txt` file should include all necessary libraries such as `pandas`, `numpy`, `yfinance`, `matplotlib`, `seaborn`, `scikit-learn`, `prophet`, `nltk`, `textblob`, `BeautifulSoup`, `requests`, `statsmodels`, `pmdarima`, and others as used in the project.

4. **Download NLTK Data (For Sentiment Analysis):**
   ```python
   import nltk
   nltk.download('vader_lexicon')
   ```

5. **Set Up FRED API Key:**
   - Obtain a free API key from [FRED](https://fred.stlouisfed.org/docs/api/fred/) by creating an account.
   - Update the `FRED_API_KEY` variable in the script with your API key.

## Usage

The project consists of multiple scripts that perform different stages of the analysis. Below is a guide on how to execute each part:

1. **Data Collection and Preparation:**
   - **Script:** `data_collection.py`
   - **Description:** Fetches historical stock data, financial statements, options data, and macroeconomic indicators. Implements caching to optimize data retrieval.
   - **Run:**
     ```bash
     python data_collection.py
     ```

2. **Data Cleaning:**
   - **Script:** `data_cleaning.py`
   - **Description:** Cleans the collected data by handling missing values, removing duplicates, and eliminating outliers.
   - **Run:**
     ```bash
     python data_cleaning.py
     ```

3. **Exploratory Data Analysis (EDA):**
   - **Script:** `eda_analysis.py`
   - **Description:** Performs descriptive statistics, correlation analysis, and visualizations for all datasets.
   - **Run:**
     ```bash
     python eda_analysis.py
     ```

4. **Performance Comparison with Indices:**
   - **Script:** `performance_comparison.py`
   - **Description:** Compares NVIDIA's stock performance against major market indices like S&P 500, NASDAQ, and SOX.
   - **Run:**
     ```bash
     python performance_comparison.py
     ```

5. **Financial Metrics Analysis:**
   - **Script:** `financial_metrics_analysis.py`
   - **Description:** Analyzes NVIDIA's financial health by calculating and visualizing key financial ratios and metrics.
   - **Run:**
     ```bash
     python financial_metrics_analysis.py
     ```

6. **Competitor Analysis:**
   - **Script:** `competitor_analysis.py`
   - **Description:** Benchmarks NVIDIA against its main competitors (AMD, Intel, Micron, TSMC) in terms of beta, annual returns, and volatility.
   - **Run:**
     ```bash
     python competitor_analysis.py
     ```

7. **Technical Analysis:**
   - **Script:** `technical_analysis.py`
   - **Description:** Computes and visualizes technical indicators such as MACD, Bollinger Bands, RSI, and support/resistance levels.
   - **Run:**
     ```bash
     python technical_analysis.py
     ```

8. **Options Analysis:**
   - **Script:** `options_analysis.py`
   - **Description:** Analyzes NVIDIA's call and put options, filtering based on strike prices and expiration dates.
   - **Run:**
     ```bash
     python options_analysis.py
     ```

9. **Sentiment Analysis:**
   - **Script:** `sentiment_analysis.py`
   - **Description:** Scrapes news headlines related to NVIDIA and analyzes their sentiment using VADER and TextBlob.
   - **Run:**
     ```bash
     python sentiment_analysis.py
     ```

10. **External Factors Analysis:**
    - **Script:** `external_factors_analysis.py`
    - **Description:** Evaluates the impact of macroeconomic indicators and significant events on NVIDIA's stock price.
    - **Run:**
      ```bash
      python external_factors_analysis.py
      ```

11. **Stock Split Analysis:**
    - **Script:** `stock_split_analysis.py`
    - **Description:** Examines the effects of historical stock splits on NVIDIA's stock price and trading volume.
    - **Run:**
      ```bash
      python stock_split_analysis.py
      ```

12. **Time Series Forecasting:**
    - **Script:** `time_series_forecasting.py`
    - **Description:** Utilizes Prophet to forecast NVIDIA's future stock prices and visualizes the predictions.
    - **Run:**
      ```bash
      python time_series_forecasting.py
      ```

13. **Risk and Opportunity Identification:**
    - **Script:** `risk_opportunity_identification.py`
    - **Description:** Identifies potential risks and opportunities for NVIDIA based on financial metrics, market sentiment, and external factors.
    - **Run:**
      ```bash
      python risk_opportunity_identification.py
      ```

## Analysis Overview

The project follows a systematic approach to analyze NVIDIA's stock and financial data:

1. **Data Collection:** Gathers historical stock prices, financial statements, options data, and macroeconomic indicators using APIs like Yahoo Finance and FRED. Implements caching to store retrieved data locally, reducing API call frequency and enhancing performance.

2. **Data Cleaning:** Ensures data quality by handling missing values through imputation, removing duplicate records, and filtering outliers to maintain dataset integrity.

3. **Exploratory Data Analysis (EDA):** Provides a foundational understanding of the data through statistical summaries, data distributions, and correlation matrices. Visualizations help in identifying trends and relationships.

4. **Technical Analysis:** Computes technical indicators such as MACD, Bollinger Bands, and RSI to assess stock momentum and potential price movements. Identifies support and resistance levels using clustering techniques like K-Means.

5. **Financial Metrics Analysis:** Calculates key financial ratios (e.g., P/E ratio, revenue growth, profit margins) to evaluate NVIDIA's financial health and operational efficiency.

6. **Competitor Benchmarking:** Compares NVIDIA's performance with major competitors and market indices to contextualize its market position and volatility.

7. **Sentiment Analysis:** Analyzes news headlines to gauge market sentiment towards NVIDIA, utilizing natural language processing tools like VADER and TextBlob.

8. **Forecasting:** Employs Prophet for time series forecasting to predict future stock prices, aiding in investment decision-making.

9. **Risk and Opportunity Identification:** Synthesizes insights from financial metrics, sentiment analysis, and external factors to outline potential risks and opportunities for NVIDIA.

## Results

The analysis yields several insightful findings:

- **Stock Performance:** NVIDIA's stock has demonstrated robust growth compared to major indices like S&P 500 and NASDAQ, with significant cumulative returns over the analyzed period.

- **Financial Health:** Strong revenue growth and high profit margins indicate a healthy and expanding business model. However, a high P/E ratio suggests potential overvaluation, warranting cautious investment.

- **Technical Indicators:** Indicators like MACD and RSI provide signals on potential buy or sell opportunities. Bollinger Bands and support/resistance levels help in understanding price volatility and trend reversals.

- **Competitor Benchmarking:** NVIDIA exhibits higher beta compared to some competitors, indicating greater volatility. Correlation analysis reveals the degree to which NVIDIA's stock movements align with its peers and market indices.

- **Sentiment Analysis:** Positive sentiment in news headlines correlates with stock price increases, while negative sentiment may signal potential downturns.

- **Forecasting:** Prophet-based forecasts project continued growth in NVIDIA's stock price, though subject to market dynamics and external factors.

- **Risk and Opportunity:** Identified risks include high valuation metrics and potential market slowdowns, while opportunities lie in expanding AI and data center markets, strong financial metrics, and favorable market sentiment.

## Contributing

Contributions are welcome! If you'd like to enhance this project, please follow these steps:

1. **Fork the Repository**
2. **Create a New Branch**
   ```bash
   git checkout -b feature/YourFeature
   ```
3. **Commit Your Changes**
   ```bash
   git commit -m "Add your feature"
   ```
4. **Push to the Branch**
   ```bash
   git push origin feature/YourFeature
   ```
5. **Open a Pull Request**

Please ensure your contributions adhere to the project's coding standards and include relevant documentation.

---

**Disclaimer:** This analysis is for educational and informational purposes only. It does not constitute financial advice. Always consult with a professional financial advisor before making investment decisions.
