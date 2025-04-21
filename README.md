# Unsupervised Clustering of NVDA Trading Days

## Project Overview

This project discovers hidden structure in NVIDIA (NVDA) daily trading data (2018–2025). Using unsupervised methods — K‑Means and DBSCAN — we group days with similar price/volume behaviour and flag unusual “shock” sessions.

Insights include:
-   **Market Regimes:** Identifying distinct periods like calm up‑trends vs. volatile down‑moves.
-   **Anomaly Detection:** Flagging high‑volatility or potentially news‑driven outlier days.
-   **Feature Engineering:** Utilizing percent‑based and trend‑relative metrics for better pattern discovery.

## Features
- **Data Acquisition:**  
  - Pull adjusted NVDA data from Yahoo! Finance via `yfinance`
- **Feature Engineering:**  
  - Daily_Return, Intraday_Range%, Overnight Gap%, 10‑day SMA, Price_vs_SMA10, and Volume_z  
- **Clustering & Evaluation:**  
  - K‑Means with silhouette & Davies‑Bouldin metrics  
  - DBSCAN for anomaly detection  
  - PCA for 2‑D visualization  
- **Analysis & Interpretation:**  
  - Cluster profiles, regime descriptions, and anomaly overlays  
  - Discussion of limitations and future extensions

## Dependencies
All required libraries are listed in `requirements.txt`. To install:

```bash
pip install -r requirements.txt
```

## How to Run the Project

### Option 1: Local Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Alisherg/nvda-unsupervised.git
   ```
2. **Change Directory and Install Dependencies:**
    ```bash
    cd nvda
    pip install -r requirements.txt
    ```
3. **Run the Notebook:**
    ```bash
    jupyter notebook unsupervised_learning_nvda.ipynb
    ```

### Option 2: Google Colab

1. **Upload Notebook to Google Colab:**
   - Open Google Colab.
   - Click on `File > Upload Notebook` and select `unsupervised_learning_nvda.ipynb` from your local machine.

2. **Run the Notebook on Colab:**
   - Once uploaded, run each cell in sequence.
   - Google Colab comes pre-installed with most required libraries, but if any are missing, add a cell with:

3. **Clear All Outputs Before Running (Optional):**
   - To start with a clean notebook, click on `Edit > Clear all outputs` before running the cells.

### Additional Notes

- **Data:** The project uses historical stock data from Yahoo! Finance via the `yfinance` library. No manual download is required.
- **Results:** The notebook includes detailed visualizations and performance metrics. Make sure to run all cells to reproduce the analysis.
