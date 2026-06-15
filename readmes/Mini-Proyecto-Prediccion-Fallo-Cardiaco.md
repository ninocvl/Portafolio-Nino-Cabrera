# Heart Failure Prediction — MLOps with Kubernetes & Monitoring

End-to-end ML system that predicts cardiac failure risk using the [Kaggle Heart Failure Prediction dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction). Covers the full stack from notebook to a live API deployed on Render with data drift monitoring via Evidently.

## Live demo

- **API (Swagger):** https://heart-api-y63c.onrender.com/docs
- **Frontend:** https://ninocvl.github.io/Mini-Proyecto-Prediccion-Fallo-Cardiaco

## Results

| Metric | Value |
|--------|-------|
| Model | Random Forest (scikit-learn Pipeline) |
| Dataset | 918 patients, 12 clinical features |
| Deployment | Render (cloud) + Docker + Kubernetes |

## Project Structure

```
├── heart-disease-mlops/
│   ├── notebooks/               # EDA and model development
│   ├── app/                     # FastAPI service
│   ├── frontend/                # Gradio UI
│   └── monitoring/              # Evidently drift reports
├── .github/workflows/           # CI/CD with GitHub Actions
├── requirements.txt
└── readme.md
```

## Stack

- **ML:** scikit-learn (Random Forest, Pipeline)
- **API:** FastAPI, Pydantic
- **UI:** Gradio
- **Monitoring:** Evidently (data drift detection)
- **Infra:** Docker, Kubernetes, GitHub Actions, Render

## Run locally

```bash
git clone https://github.com/ninocvl/Mini-Proyecto-Prediccion-Fallo-Cardiaco
cd Mini-Proyecto-Prediccion-Fallo-Cardiaco/heart-disease-mlops

pip install -r requirements.txt

# API
uvicorn app.main:app --reload

# UI (separate terminal)
python frontend/app.py
```



---

Built by [Nino Cabrera](https://github.com/ninocvl)
