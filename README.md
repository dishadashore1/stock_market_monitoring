
```markdown
# 📄 Project Statement of Purpose

## Project Title: Stock Market Monitor and Next-Day Price Predictor

## 1. Goal and Objectives

The primary goal of this project was to demonstrate proficiency in creating a complete, full-stack data application using a **unified Python environment** (Streamlit, Pandas, Scikit-learn).

**Key Objectives Met:**
1.  **Full-Stack Implementation:** Successfully used Python (Streamlit) for dynamic front-end development, eliminating the need for separate HTML/CSS/JavaScript.
2.  **Data Acquisition:** Implemented real-time data fetching from an external API (`yfinance`) based on dynamic user input.
3.  **Machine Learning Integration:** Integrated a machine learning model (Linear Regression) directly into the back-end logic to perform a predictive task.
4.  **Deployment:** Successfully deployed the application from a notebook environment (Google Colab) to a publicly accessible web address (`ngrok`).

## 2. Methodology and Model Selection

### Data Source
Historical OHLCV (Open, High, Low, Close, Volume) data is fetched using the `yfinance` library. The model relies specifically on the **Adjusted Close** price, which is the most accurate reflection of a stock's true value over time.

### Prediction Model: Linear Regression
A **Simple Linear Regression** model was selected for its interpretability and ease of implementation. The model uses the **time index** (sequential days) as the independent variable ($X$) and the next day's price as the dependent variable ($y$).

$$
\text{Price}_{t+1} = \beta_0 + \beta_1 \cdot \text{TimeIndex}_t
$$

This model makes the fundamental assumption that the stock's price trend is linear over the selected historical period.

## 3. Limitations and Future Scope

### Limitations
* **Model Simplicity:** Linear Regression is highly simplistic and does not account for market volatility, non-linear relationships, external news events, or complex trading indicators (RSI, MACD). **The prediction has no actual financial reliability.**
* **Deployment Environment:** The application runs on a temporary server hosted by Colab, requiring periodic restarts and token authentication (`ngrok`).

### Future Scope
* Upgrade the prediction model to a more complex time-series technique, such as **ARIMA** or a **Recurrent Neural Network (LSTM)**, for potentially more accurate forecasting.
* Integrate additional data visualizations, such as candlestick charts and volume bars.
* Add a feature to analyze the latest sentiment from financial news APIs to augment the prediction.
