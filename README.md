# StockPrice_Prediction using LSTM

This project implements a Long Short-Term Memory (LSTM) neural network model to predict future stock prices based on historical data. The model is trained using time-series data from the **NSE: Tata Global Beverages** stock and demonstrates future forecasting for the next 30 days.

---

## 📌 Project Overview

Stock price prediction is a challenging and highly sought-after task in quantitative finance. This project leverages deep learning (LSTM) to analyze historical stock data and predict upcoming trends. Data visualization, preprocessing, model training, evaluation, and future forecasting are all included.

---

## 🛠️ Technologies Used

* **Python 3.x**
* **Google Colab / Jupyter Notebook**
* **TensorFlow & Keras**
* **NumPy, Pandas, Matplotlib**
* **Scikit-learn**

---

## 📁 Dataset

* Dataset: `NSE-TATAGLOBAL.csv`
* Contains historical stock data including:

  * `Date`, `Open`, `High`, `Low`, `Last`, `Close`, `Total Trade Quantity`, `Turnover (Lacs)`

---

## 📈 Visualizations

The project includes:

* 📊 **Open vs Close Price**
* 📉 **High vs Low vs Last**
* 📦 **Total Trade Quantity**
* 💰 **Turnover (Lacs)**

---

## 🧠 Model Architecture

* **LSTM-based Sequential model**
* Layers:

  * 3 LSTM layers (50 units each)
  * Dropout layers to prevent overfitting
  * Dense layer for final prediction
* Trained for 100 epochs with batch size of 32

---

## 📊 Model Performance

The model is evaluated using:

* **MAE** (Mean Absolute Error)
* **MSE** (Mean Squared Error)
* **RMSE** (Root Mean Squared Error)
* **R² Score**

```text
MAE  = ~191.83
MSE  = ~40513.25
R²   = -605638.79
RMSE = ~201.27
```

> Note: Due to high volatility and dataset limitations, R² was negative, indicating room for improvement.

---

## 🔮 Forecasting

The model forecasts stock prices for the **next 30 days**, and results are plotted against the last 100 days of historical prices.

```python
# Future prediction loop (30 days)
for i in range(1, 31):
    predict next value using LSTM model
```

---

## 🧪 How to Run

1. Upload the dataset `NSE-TATAGLOBAL.csv`
2. Run the notebook in Google Colab or Jupyter
3. The model will train and then predict future prices
4. View training/test predictions and future price forecasts

---

## 📂 Folder Structure (Suggested)

```
stock-price-prediction-lstm/
├── Stock_Prediction_LSTM.ipynb
├── NSE-TATAGLOBAL.csv
├── README.md
└── output_plots/
    └── predictions.png
```

---

## 📌 Future Improvements

* Add more features (volume, moving averages, sentiment)
* Use additional deep learning models (GRU, BiLSTM)
* Incorporate real-time data fetching via APIs
* Deploy as a web dashboard using Streamlit or Flask

---

## 👨‍💻 Author

**D. Lalith Kumar**
*Computer Science & Engineering (AI & ML)*

---

## 📜 License

This project is open-source and available for educational and research use.
