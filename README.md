# Credit Risk Prediction

An exploratory machine-learning project that compares classification models for predicting loan default from applicant and loan attributes.

## Project Contents

- `credit_risk_prediction.ipynb` - data exploration, preprocessing, model comparison, and tuning.
- `credit_risk_dataset.csv` - dataset used by the notebook.
- `correlation heatmap.png` and `PCA graph.png` - exported analysis figures.

Assignment PDFs and local development files are intentionally excluded from version control.

## Getting Started

Run these commands from the repository root:

```bash
python -m venv .venv
```

Activate the environment, then install the dependencies and start Jupyter:

```bash
python -m pip install -r requirements.txt
jupyter notebook credit_risk_prediction.ipynb
```

On Windows PowerShell, activate the environment with `.venv\Scripts\Activate.ps1`. On macOS or Linux, use `source .venv/bin/activate`.

The notebook reads `credit_risk_dataset.csv` using a relative path, so launch Jupyter from the repository root.

## Analysis

The notebook explores the target distribution, feature relationships, missing values, and outliers. It then prepares the data, uses a stratified 80/20 train/test split, scales numeric features, and evaluates both scaled features and PCA-transformed features.

The classifiers compared are:

- Logistic regression
- k-nearest neighbors
- Decision tree

Each is evaluated with accuracy, precision, recall, and F1 score. A grid search tunes the decision tree using cross-validation and F1 scoring.

## Dataset

The target is `loan_status` (`0` for no default and `1` for default). The remaining columns describe applicant age, income, home ownership, employment length, loan intent, grade, amount, interest rate, loan-to-income ratio, prior default status, and credit-history length.

The dataset is included as supplied with this project. Its original source and redistribution terms were not included; verify them and add attribution before making the repository public or redistributing the data.

## Responsible Use

This is an educational analysis, not a validated credit decision system. It does not establish fairness, calibration, legal compliance, or suitability for real lending decisions. Credit decisions require careful validation, documented data provenance, bias assessment, and human oversight.

## License

No license is currently specified. Unless a license is added, standard copyright applies to the project files; dataset rights remain subject to the original source's terms.