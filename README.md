# Benchmarking Time-Series Forecasting Models for Monthly Groundwater Level Prediction

**Module:** IJC319 Final Year Project  
**University of Sheffield** — School of Information, Journalism and Communication  
**Author:** Zahra Sameer Alkhalifah  
**Supervisor:** Dr Abdallah M. Yaghi

---

## Overview

This repository contains the website and digital artefact for a final-year project benchmarking three time-series forecasting models — **SARIMAX**, **LSTM**, and **TCN** — for monthly groundwater level (GWL) prediction using a UK observational dataset spanning 1944–2023.

The project evaluates whether deep learning models outperform traditional statistical approaches for GWL forecasting, and examines the contribution of meteorological variables (temperature, precipitation, wind speed) to each model's predictions using permutation feature importance.

## Research Hypotheses

- **H1:** Deep learning models (LSTM, TCN) outperform SARIMAX in GWL forecasting accuracy.
- **H2:** TCN outperforms LSTM due to its parallelisable architecture and dilated convolutions.
- **H3:** Meteorological variables contribute meaningfully to model predictions.

## Key Results

| Model    | RMSE  | MAE   | R²    | NSE   |
|----------|-------|-------|-------|-------|
| LSTM     | Best  | Best  | Best  | Best  |
| TCN      | Second| Second| Second| Second|
| SARIMAX  | Third | Third | Third | Third |



## Notebooks (Hosted on HuggingFace)

All trained model HuggingFace for reproducibility:

| Model    | Notebook Link |
|----------|--------------|
| SARIMAX  | [Kozy9/GWSarimax](https://huggingface.co/Kozy9/GWSarimax) |
| LSTM     | [Kozy9/GWLSTM](https://huggingface.co/Kozy9/GWLSTM) |
| TCN      | [Kozy9/GWTCN](https://huggingface.co/Kozy9/GWTCN) |

**Gradio App:** [ML-GWL-Forecaster on HuggingFace Spaces](https://huggingface.co/spaces/kozy9/ML-GWL-Forecaster)

## Tools and Technologies

- **Language:** Python
- **Environment:** Google Colab / Jupyter Notebooks
- **Deep Learning:** TensorFlow/Keras, `keras-tcn`
- **Statistical Modelling:** statsmodels (SARIMAX)
- **Hyperparameter Optimisation:** Keras Tuner (Bayesian) for LSTM/TCN, Optuna (TPE) for SARIMAX
- **Preprocessing:** MinMaxScaler, pandas, NumPy
- **Evaluation Metrics:** RMSE, MAE, MAPE, R², NSE
- **Feature Importance:** Permutation-based importance analysis

## Data Sources

- **Groundwater Levels:** IGRAC (International Groundwater Resources Assessment Centre) — 27 UK monitoring wells
- **Meteorological Data:** Temperature, precipitation, wind speed (1944–2023)

## How to Reproduce

1. Open the relevant notebook link from the table above.
2. Run the notebook in Google Colab (recommended) or a local Jupyter environment.
3. Each notebook includes markdown explanation cells paired with code cells, following a numbered step-by-step structure.
4. All preprocessing, training, evaluation, and visualisation steps are contained within the notebooks.

> **Note:** Notebooks have been cleaned of widget metadata for rendering compatibility. Run all cells to reproduce outputs.

## Website

The project website is published via GitHub Pages and provides an accessible visualisation of the research findings:

🔗 [https://zahrask2.github.io/ML-GWL-frocaster/](https://zahrask2.github.io/ML-GWL-frocaster/)

## Ethical Approval

This project received ethical approval from the University of Sheffield. The study uses secondary, non-personal environmental data and does not involve human participants.

## License

This project was completed as part of the IJC319 module at the University of Sheffield.
