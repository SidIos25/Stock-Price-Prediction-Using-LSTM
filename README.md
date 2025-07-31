# Stock-Price-Prediction-Using-LSTM


This project is a real-time stock price prediction system built using an LSTM (Long Short-Term Memory) deep learning model. It fetches historical stock data, applies technical indicators, trains an LSTM model, and predicts future stock prices. The project also visualizes actual vs predicted prices and can fetch recent stock-related news headlines.

---

##  Features

-  **Real-time stock price fetching** from Yahoo Finance, Google Finance, MarketWatch, or Investing.com.
-  **LSTM model** to predict next-day stock prices.
-  **Interactive visualizations** using Plotly and Matplotlib.
-  **Technical indicators** like RSI, MACD, Bollinger Bands, and EMA.
-  **Latest news headlines** related to the stock ticker.
-  **Fallback sample data generator** when no stock data is available.

---

##  Project Structure

```
 StockPricePredictor/
│
├── stock_predictor.py      # Main script with StockPredictor class
├── README.md               # Project documentation
└── requirements.txt        # Required libraries
```

> If you're running this on Google Colab, simply copy-paste the class and call methods as shown below.

---

##  How It Works

### 1. Fetch Stock Data
The script uses multiple sources (Yahoo, Google, MarketWatch) to retrieve real-time and historical stock data.

### 2. Feature Engineering
Calculates technical indicators:
- EMA (Exponential Moving Average)
- RSI (Relative Strength Index)
- MACD (Moving Average Convergence Divergence)
- Bollinger Bands

### 3. Model Training
The LSTM model is trained on past stock prices (scaled with MinMaxScaler) to learn patterns and trends.

### 4. Prediction & Visualization
- Predicts the next day’s stock price.
- Plots actual vs predicted prices using both Matplotlib and Plotly.

### 5. News Fetching
Scrapes latest headlines related to the company from Google News.

---

##  Example Usage

```python
predictor = StockPredictor('AAPL')
predictor.predict()
predictor.display_actual_vs_predicted()
predictor.display_plotly_graph()
predictor.fetch_news()
```

---

##  Dependencies

Install the following packages if not using Colab:

```bash
pip install yfinance beautifulsoup4 lxml plotly tensorflow scikit-learn
```

If you're using **Google Colab**, most libraries are pre-installed.

---

##  Notes

- Works best with stock symbols from **NASDAQ**, **NYSE**, etc.
- If all sources fail (e.g., ticker is invalid or internet is down), synthetic data is generated.
- Modify sequence length, model structure, or add new indicators for improved accuracy.

---

##  Author

**Sidharth Kumar Reddy**  
Hyderabad, India  
sidkr725@gmail.com  
[GitHub](https://github.com/SidIos25)

---

## License

This project is open-source and free to use under the [MIT License](https://opensource.org/licenses/MIT).
