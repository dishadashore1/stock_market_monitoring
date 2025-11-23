Since you need the content for the `STATEMENT.md` file for your university submission, here is the complete, formatted Markdown content. You can copy and paste this directly into the file editor on GitHub.

---

## 📄 STATEMENT.md: Project Justification and Methodology

# Project Title: Stock Market Monitor and Next-Day Price Predictor

## 1. Goal and Objectives

The primary goal of this project was to demonstrate proficiency in creating a complete, **full-stack data application** using a unified **Python environment**. This approach utilizes Streamlit to eliminate the need for separate front-end languages (HTML/CSS/JavaScript).

**Key Objectives Met:**

* **Full-Stack Implementation:** Successfully implemented both the presentation (front-end) and data processing (back-end) layers entirely in Python (Streamlit and Scikit-learn).
* **Dynamic Data Acquisition:** Implemented code to fetch real-time/historical stock data from a public API (`yfinance`) based on dynamic user input.
* **Machine Learning Integration:** Integrated a simple machine learning model (Linear Regression) directly into the back-end logic to perform a predictive task.
* **Deployment:** Successfully deployed the application from a notebook environment (Google Colab) to a publicly accessible web address (`ngrok`).

---

## 2. Methodology and Model Selection

### Data Source

Historical OHLCV (Open, High, Low, Close, Volume) data is fetched using the `yfinance` library. The model relies specifically on the **Adjusted Close** price, which is the most accurate reflection of a stock's true value over time.

### Prediction Model: Simple Linear Regression

A **Simple Linear Regression** model was selected for this demonstration due to its fundamental nature and ease of integration into the application logic. The model treats the historical stock data as a simple **time series**.

* **Independent Variable ($X$):** The time index (sequential day number).
* **Dependent Variable ($y$):** The stock's closing price on the *next day* (shifted price data).

The model assumes a linear trend over the selected historical period to project the value for the next data point, following the basic linear equation:

$$
\text{Price}_{t+1} = \beta_0 + \beta_1 \cdot \text{TimeIndex}_t
$$

---

## 3. Limitations and Future Scope

### Limitations

* **Model Simplicity:** Linear Regression is highly simplistic for finance. It fails to account for market volatility, non-linear dependencies, sudden news events, or complex trading indicators. **The prediction should not be considered reliable financial advice.**
* **Deployment Dependency:** The application relies on a temporary Colab runtime and a tunneling service (`ngrok`), meaning the public link is transient and requires the Colab notebook to remain active.

### Future Scope

* Upgrade the prediction algorithm to a more advanced time-series model, such as **ARIMA** or a **Recurrent Neural Network (LSTM)**, to capture temporal dependencies and non-linear patterns.
* Integrate additional technical indicators (e.g., RSI, MACD, Bollinger Bands) as input features to enhance model accuracy.
* Implement richer data visualizations, such as interactive candlestick charts and historical volume analysis.
