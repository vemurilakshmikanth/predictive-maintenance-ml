# 🛩️ Predictive Maintenance for Aircraft Engines

Machine Learning project to predict Remaining Useful Life (RUL) of turbofan engines using NASA's CMAPSS dataset.

## 📋 Project Overview

This project uses sensor data from aircraft engines to predict when they will fail, enabling **predictive maintenance** instead of reactive repairs. By analyzing 21 sensor readings across engine lifecycles, two ML models were trained to estimate Remaining Useful Life (RUL).

### 🎯 Business Value
- **Cost Reduction**: Schedule maintenance before failures occur
- **Safety Improvement**: Prevent unexpected engine failures
- **Efficiency**: Optimize maintenance schedules based on actual condition

## 📊 Dataset

**Source**: NASA CMAPSS (Commercial Modular Aero-Propulsion System Simulation)
- **Training Samples**: 20,631 sensor readings
- **Engines**: 100 turbofan engines
- **Features**: 14 sensor measurements + 2 operational settings
- **Target**: RUL (Remaining Useful Life) in cycles

## 🔧 Technologies Used

- **Python 3.11**
- **pandas & NumPy**: Data manipulation
- **scikit-learn**: Machine learning algorithms
- **XGBoost**: Gradient boosting
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development

## 🤖 Models Trained

### 1. Random Forest Regressor
- **Test R² Score**: 62.61%
- **Mean Absolute Error**: ±29.5 cycles
- **Training Time**: 2.65 seconds

### 2. XGBoost Regressor
- **Test R² Score**: 62.23%
- **Mean Absolute Error**: ±29.8 cycles
- **Training Time**: 0.31 seconds (8x faster!)

## 📈 Results

Both models achieved ~62% accuracy on unseen test data, predicting engine failure with an average error of ±30 cycles. Random Forest performed slightly better in accuracy, while XGBoost was significantly faster.

## 🚀 Project Structure
```
predictive-maintenance/
├── data/                      # Raw NASA dataset
├── notebooks/                 # Jupyter notebooks
│   └── 01_data_exploration.ipynb
├── models/                    # Trained ML models
│   ├── random_forest_model.pkl
│   ├── xgboost_model.pkl
│   └── scaler.pkl
├── results/                   # Outputs and metrics
│   ├── cleaned_data.csv
│   └── model_performance.json
├── src/                       # Source code (future)
├── requirements.txt           # Python dependencies
└── README.md                  # This file
```

## 💻 Installation & Usage

### Prerequisites
```bash
python --version  # Python 3.11+
```

### Setup
```bash
# Clone repository
git clone <your-repo-url>
cd predictive-maintenance

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Mac/Linux
venv\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt
```

### Run the Analysis
```bash
jupyter notebook notebooks/01_data_exploration.ipynb
```

## 📚 Key Learnings

- **Feature Engineering**: Identified and removed 13 constant sensors
- **Model Comparison**: Evaluated multiple algorithms
- **Overfitting Management**: Balanced train vs test performance
- **Production Pipeline**: Saved models for deployment

## 🎓 Future Improvements

- [ ] Deep Learning models (LSTM for time-series)
- [ ] Hyperparameter tuning (GridSearch)
- [ ] Feature importance analysis
- [ ] Web dashboard for predictions
- [ ] Deploy as REST API

## 👤 Author

**[Your Name]**
- Portfolio: [Your Website]
- LinkedIn: [Your LinkedIn]
- GitHub: [Your GitHub]

## 📄 License

This project is for educational purposes.

## 🙏 Acknowledgments

- NASA for the CMAPSS dataset
- Kaggle community for dataset hosting