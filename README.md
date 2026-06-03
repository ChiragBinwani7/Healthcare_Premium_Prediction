# Health Insurance Premium Prediction

An end-to-end Machine Learning web application built with Streamlit that predicts health insurance premium costs based on user demographics and medical history. The project implements a regression model, providing accurate premium estimations to help individuals make informed financial decisions regarding their health insurance.

## 🚀 Features

- **Interactive User Interface:** Easy-to-use web interface built using Streamlit.
- **Personalized Predictions:** Computes insurance premiums considering various factors such as Age, Dependents, Income, BMI, Smoking Status, Medical History, and Insurance Plan type.
- **Dynamic Risk Calculation:** Normalizes risk scores based on pre-existing conditions like Diabetes, Heart Disease, Thyroid, and High Blood Pressure.
- **Age-Specific Modeling:** Utilizes two separate predictive models tailored for young individuals (Age <= 25) and others to improve accuracy.

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **Frontend/UI:** [Streamlit](https://streamlit.io/)
- **Machine Learning:** [Scikit-learn](https://scikit-learn.org/), [XGBoost](https://xgboost.readthedocs.io/)
- **Data Manipulation:** [Pandas](https://pandas.pydata.org/), [NumPy](https://numpy.org/)
- **Model Serialization:** Joblib

## 📁 Project Structure

```text
├── artifacts/                                # Contains trained models and scalers (joblib files)
│   ├── health_insurance_premium_rest.joblib  # Model for age > 25
│   ├── health_insurance_premium_young.joblib # Model for age <= 25
│   ├── scaler_rest.joblib                    # Scaler for age > 25
│   └── scaler_young.joblib                   # Scaler for age <= 25
├── main.py                                   # Streamlit application (Frontend)
├── prediction_helper.py                      # Data preprocessing and prediction logic
├── requirements.txt                          # Python dependencies
├── README.md                                 # Project documentation
└── LICENSE                                   # License file
```

## ⚙️ Installation and Setup

Follow these steps to run the application locally.

1. **Clone the repository:**
   ```bash
   git clone https://github.com/ChiragBinwani7/Healthcare_Premium_Prediction.git
   cd Healthcare_Premium_Prediction
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application:**
   ```bash
   streamlit run main.py
   ```

## 💡 Usage

1. Open the local link provided by Streamlit in your web browser (usually `http://localhost:8501`).
2. Fill in the required details (Age, Income, Dependents, Medical History, etc.).
3. Click the **Predict** button.
4. The estimated health insurance premium will be displayed on the screen.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
