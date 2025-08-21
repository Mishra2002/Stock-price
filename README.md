# Stock Prediction Project (Multi-Model)

**Contents**: An end-to-end, multi-model stock prediction scaffold including:
- LSTM (sequence forecasting)
- XGBoost (feature-based classification/regression)
- Hybrid ensemble
- Backtesting and simple FastAPI + Streamlit interfaces

**How to use (quick)**
1. Create a Python virtual environment and install dependencies:
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```
2. Put your historical OHLCV CSV files into `data/` folder. Example CSV columns:
   `Date,Open,High,Low,Close,Volume`
3. Run a quick demo (train & predict) using:
   ```bash
   python src/main.py --data_path data/sample_ohlcv.csv --mode demo
   ```
4. Run the API:
   ```bash
   uvicorn src.api.app:app --reload --port 8000
   ```
5. Run the Streamlit app:
   ```bash
   streamlit run src/ui/streamlit_app.py
   ```

**Project structure**
- src/: source modules (preprocessing, features, models, backtesting, API, UI)
- data/: place your OHLCV CSV files here (sample included)
- requirements.txt : python deps
- README.md

This scaffold is meant to be a working starting point for the technical round submission. 
Replace/extend models, hyperparameters, and strategy rules as needed.
