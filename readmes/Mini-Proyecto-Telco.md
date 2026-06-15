# Telco Churn Prediction — End-to-End MLOps

Predicts customer churn for a telecom company using the [Kaggle Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (~7,000 records). The project covers the full ML lifecycle: exploratory analysis, model training, interpretability, REST API, and containerized deployment.

## Results

| Metric | Value |
|--------|-------|
| Dataset | 7,043 customers |
| Best model | Logistic Regression / Random Forest (GridSearchCV) |
| Deployment | FastAPI + Gradio + Docker |

## Project Structure

```
├── data/                          # Raw and processed datasets
├── notebooks/
│   ├── 1_eda_preprocessing.ipynb  # Exploratory analysis and feature engineering
│   ├── 2_model_training.ipynb     # Model selection and hyperparameter tuning
│   └── 3_interpretability.ipynb   # LIME explanations
├── app/
│   ├── api.py                     # FastAPI prediction endpoint
│   ├── schemas.py                 # Pydantic request/response models
│   └── model.joblib               # Trained scikit-learn pipeline
├── frontend/
│   ├── app.py                     # Gradio interactive UI
│   └── Dockerfile
├── tests/
│   ├── test_api.py
│   └── test_model.py
├── Dockerfile
└── requirements.txt
```

## Stack

- **ML:** scikit-learn (Pipeline, GridSearchCV), LIME
- **API:** FastAPI, Pydantic
- **UI:** Gradio
- **Infra:** Docker, GitHub Actions (CI/CD)

## Run locally

```bash
# Clone
git clone https://github.com/ninocvl/Mini-Proyecto-Telco
cd Mini-Proyecto-Telco

# Install dependencies
pip install -r requirements.txt

# Start API
uvicorn app.api:app --reload

# Start Gradio UI (separate terminal)
python frontend/app.py
```

## Notebooks

| Notebook | Description |
|----------|-------------|
| `1_eda_preprocessing.ipynb` | Data quality, class imbalance, feature correlation |
| `2_model_training.ipynb` | Model comparison, cross-validation, final pipeline |
| `3_interpretability.ipynb` | LIME explanations for individual predictions |

---

Built by [Nino Cabrera](https://github.com/ninocvl)
