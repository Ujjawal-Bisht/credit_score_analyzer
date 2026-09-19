# Credit Score Analyzer

A machine learning project for predicting credit risk using the German Credit dataset. The project includes data exploration, preprocessing, model training, and a Streamlit web application for making predictions.

## Project Overview

This project analyzes customer credit data and predicts whether a loan application is likely to be:

- Good risk
- Bad risk

The final selected model is a Random Forest classifier. For this project, the model was chosen because Random Forest delivered the strongest balance of recall and F1 score while staying very close to Extra Trees in ROC-AUC. This makes it the most suitable choice for identifying risky loan applicants more reliably.

## Project Structure

```text
credit_score_analyzer/
├── .venv/
├── data/
│   └── german_credit_data.csv
├── models/
│   ├── random_forest_credit_model.pkl
│   ├── target_encoder.pkl
│   └── label_encoders/
│       ├── Sex_encoder.pkl
│       ├── Housing_encoder.pkl
│       ├── Saving accounts_encoder.pkl
│       ├── Checking account_encoder.pkl
│       └── Purpose_encoder.pkl
├── notebooks/
│   └── pre_processing.ipynb
├── reports/
│   └── MODEL_EVALUATION_SUMMARY.md
├── main.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Features Used

- Age
- Sex
- Job
- Housing
- Saving accounts
- Checking account
- Credit amount
- Duration
- Risk (target)

## Setup

1. Clone the repository.
2. Create and activate a virtual environment.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Run the Notebook

Open the notebook in Jupyter or VS Code:

```text
notebooks/pre_processing.ipynb
```

It contains:

- dataset loading
- missing value checks
- cleaning steps
- exploratory data analysis
- encoding
- model training and comparison
- model export

## Run the Streamlit App

From the project root, run:

```bash
streamlit run main.py
```

This launches the web interface where you can input applicant information and get a credit risk prediction.

## Model Details

The project compares several classifiers:

- Decision Tree
- Random Forest
- Extra Trees
- XGBoost

The Random Forest model was selected as the best-performing model for this project because it achieved the best recall and F1 score among the evaluated models, while remaining competitive on ROC-AUC.

## Important Notes

- The encoded categorical features are saved in the `models/label_encoders` folder.
- The trained model is stored in `models/random_forest_credit_model.pkl`.
- The final selected model is Random Forest because the project prioritizes recall and F1 score for credit-risk detection.
- The model expects the same feature names and preprocessing logic used during training.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Streamlit

## License

This project is for educational and demonstration purposes.
