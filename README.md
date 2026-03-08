# Air-passenger-forecasting-lstm-gru

This project focuses on **time-series forecasting** of international airline passengers using **deep learning models**, specifically **LSTM (Long Short-Term Memory)** and **GRU (Gated Recurrent Unit)**.  
The goal is to predict the **number of passengers for the next 6 and 12 months** based on historical data.

---

## Dataset
The project uses the **AirPassengers dataset**, which contains monthly totals of international airline passengers from **January 1949 to December 1960**.

### Features
- **Month** – Date of observation (monthly)
- **Passengers** – Total number of airline passengers

## Models
Two deep learning models were implemented with the same architecture:

| Model | Epochs |
|-------|--------|
| **LSTM** | 50 | 
| **GRU**  | 40 |

Both models take previous 12 month's data (look_back window) as input to predict future passenger counts.

---

## Conclusion  
- Evaluation using **MAE** and **RMSE** showed that the **GRU model achieved lower error and better prediction results** compared to the LSTM model.  
- This indicates that the GRU model was able to **learn temporal patterns more efficiently** and generalize slightly better for forecasting future passenger counts.

| Model | Train MAE | Train RMSE | Test MAE | Test RMSE | Training Time (seconds) |
|-------|-----------|------------|----------|-----------|------------------------|
| LSTM  | 13.58     | 16.85      | 32.29    | 39.26     | 13.94                  |
| GRU   | 16.03     | 18.72      | 31.19    | 37.98     | 13.90                  |

Overall, both models successfully captured the time-series patterns in the dataset, but **GRU demonstrated superior performance** for forecasting future airline passengers.
