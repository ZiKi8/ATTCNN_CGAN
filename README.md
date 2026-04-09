# ATTCNN_CGAN

**A deep learning model using Convolutional Neural Networks and conditional Generative Adversarial Networks with multi-head attention for stock prediction**

---

## Description

This repository implements **ATTCNN_CGAN**, a deep learning framework that integrates Convolutional Neural Networks (CNNs), dual-average attention, and conditional Generative Adversarial Networks (cGANs) for stock market time-series forecasting.

Repository: https://github.com/ZiKi8/ATTCNN_CGAN  
DOI: []

---

## Dataset Information

The historical stock datasets are not included in this repository but can be generated using the provided `DataCollect&Preprocess.ipynb` notebook. Run this notebook first before training the model. it can collect and preprocess data for the following stocks and save the CSV files to the `Datasets/` directory:

- AAPL
- META
- NVDA
- AMZN
- MSFT
- GOOG
- EL
- F
- TGT

Each generated dataset includes:

- **Price and volume data:** Open, High, Low, Close, Volume
- **Technical indicators:** SMA, EMA, RSI, ATR, MACD, Bollinger Bands, RSV
- **Frequency-domain features:** Fourier components
- **Attention features:** Derived dual-average attention module

---

## Repository Structure

```
├── DataCollect&Preprocess.ipynb  # Data collection and preprocessing notebook
├── Datasets/                     # Place prepared CSV files here (not included)
├── Model/
│   ├── requirements.txt
│   └── ATTCNN-CGAN/              # Proposed model
│       ├── run_train.py          # Entry point for execution
│       └── backbone/             # Core components
│           ├── __init__.py
│           ├── data.py           # I/O, scaling, sliding windows
│           ├── generator.py      # CNN-based Generator
│           ├── discriminator.py  # CNN-based Discriminator
│           ├── attn.py           # Multi-head attention / Transformer encoder
│           └── train_loop.py     # WGAN-GP training loop, plotting, results
└── tools/
    └── tools.py                  # Technical indicator utilities
```

---

## Requirements

The following Python libraries are required:

```
numpy==1.26.4
pandas==2.2.2
scikit-learn==1.4.2
matplotlib==3.9.0
yfinance==0.2.41
torch==2.2.2
```

Install all dependencies via:

```bash
pip install -r requirements.txt
```

---

## Usage Instructions

1. Generate the datasets by running `DataCollect&Preprocess.ipynb` from the root of the repository. This will save the processed CSV files to the `Datasets/` directory.

2. Navigate to the model directory:

```bash
cd Model/ATTCNN-CGAN
```

3. Run the model:

```bash
python run_train.py
```


