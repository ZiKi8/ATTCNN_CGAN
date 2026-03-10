# ATTCNN_CGAN
A deep learning model using CNNs and deterministic GANs with multi-head attention for stock prediction
<br>
<br>
Description<br>
This repository (https://github.com/ZiKi8/ATTCNN_CGAN) implements ATTCNN_CGAN, a deep learning framework that integrates Convolutional Neural Networks (CNNs), dual-average attention, and Generative Adversarial Networks (GANs) for stock market time-series forecasting. 
<br><br>
Dataset Information<br>
This repository contains multiple daily historical stock datasets, including:<br>
• AAPL<br>
• META<br>
• NVDA<br>
• AMZN<br>
• MSFT<br>
• GOOG<br>
• EL<br>
• F<br>
• TGT<br>
<br>
<br>
Each dataset includes:<br>
• Price and volume data: Open, High, Low, Close, Volume<br>
• Technical indicators: SMA, EMA, RSI, ATR, MACD, Bollinger Bands, RSV<br>
• Frequency-domain features: Fourier components<br>
• Attention features: Derived through temporal attention modules<br>
This repository contains the proposed model shown in the following structure<br>
├─ model/<br>
│ ├─ ATTCNN_CGAN/ # Proposed model<br>
│ │ ├─ backbone/ # Core components<br>
│ │ │ ├─ init.py<br>
│ │ │ ├─ data.py # I/O, scaling, sliding windows<br>
│ │ │ ├─ generator.py # CNN-based Generator<br>
│ │ │ ├─ discriminator.py # CNN-based Discriminator<br>
│ │ │ ├─ attn.py # (Optional) Attention feature extractor<br>
│ │ │ ├─ train_loop.py # Training process, plotting, results<br>
│ │ ├─ run_train.py # Entry point for execution<br>
<br>
Requirements<br> 
Please ensure the following Python libraries are installed before running the code:<br>
tensorflow==2.15.0<br>
numpy==1.26.4<br>
pandas==2.2.2<br>
scikit-learn==1.4.2<br>
scipy==1.11.4<br>
matplotlib==3.9.0<br>
yfinance==0.2.41<br>
torch==2.2.2<br>
<br>
Install all dependencies via: pip install -r requirements.txt<br>
<br>
Usage Instructions<br>
1.	Navigate to the project directory: cd models/ATTCNN_CGAN<br>
2.	Run the model: python run_train.py<br>

