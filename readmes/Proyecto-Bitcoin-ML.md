# Bitcoin Price Prediction — Hybrid ML Models

Research-grade ML project for Bitcoin price prediction. Tests multiple hybrid architectures combining classical time-series features with gradient boosting, benchmarked against paper-reported baselines.

## Live notebook

https://ninocvl.github.io/Proyecto-Bitcoin-ML

## Project Structure

```
├── 01_index.ipynb                              # Project overview and data loading
├── 02_BPP_v5_features_fixed.ipynb             # Feature engineering (v5)
├── 03_modelo_3hibridos_paper_features.ipynb   # Hybrid model experiments
├── myst.yml                                   # Jupyter Book config (GitHub Pages)
└── requirements.txt
```

## Stack

- **ML:** XGBoost, scikit-learn, statsmodels, Optuna (hyperparameter tuning)
- **Data:** pandas, numpy, scipy
- **Visualization:** matplotlib, plotly, seaborn
- **Publishing:** Jupyter Book (MyST), GitHub Actions → GitHub Pages

## Notebooks

| Notebook | Description |
|----------|-------------|
| `01_index.ipynb` | Dataset overview, data sources, project goals |
| `02_BPP_v5_features_fixed.ipynb` | Technical indicators, lag features, rolling statistics |
| `03_modelo_3hibridos_paper_features.ipynb` | Three hybrid model architectures benchmarked against published results |

## Run locally

```bash
git clone https://github.com/ninocvl/Proyecto-Bitcoin-ML
cd Proyecto-Bitcoin-ML

pip install -r requirements.txt

jupyter lab
```

To rebuild the GitHub Pages site:

```bash
pip install jupyter-book
jb build .
```

---

Built by [Nino Cabrera](https://github.com/ninocvl)
