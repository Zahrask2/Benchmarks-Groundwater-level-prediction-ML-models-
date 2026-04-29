# Benchmarking Time-Series Forecasting Models for Monthly Groundwater Level Prediction

**Module:** IJC319 Final Year Project  
**University of Sheffield** — School of Information, Journalism and Communication  
**Author:** Zahra Sameer Alkhalifah  
**Supervisor:** Dr Abdallah M. Yaghi

---

## Overview

This repository contains the Source code for the final-year project benchmarking three time-series forecasting models — **SARIMAX**, **LSTM**, and **TCN** — for monthly groundwater level (GWL) prediction using a UK observational dataset spanning 1944–2023.

## Data Sources

- **Groundwater Levels:** IGRAC (International Groundwater Resources Assessment Centre) — 27 UK monitoring wells
  https://ggis.un-igrac.org/view/ggmn/
  
- **Meteorological Data:** Temperature, precipitation, wind speed (1944–2023)
  https://open-meteo.com/
  
## Key Results

| Model    | RMSE  | MAE   | R²    | NSE   |
|----------|-------|-------|-------|-------|
| LSTM     | Best  | Best  | Best  | Best  |
| TCN      | Second| Second| Second| Second|
| SARIMAX  | Third | Third | Third | Third |

## Notebooks
| Task             | Notebook Link |
|------------------|--------------|
| Prprocessing     | [preprocessing](https://github.com/Zahrask2/Benchmarks-Groundwater-level-prediction-ML-models-/tree/main/Data%20prepration)|
| SARIMAX          | [SARIMAX](https://github.com/Zahrask2/Benchmarks-Groundwater-level-prediction-ML-models-/tree/main/SARIMAX%20development)|
| Deep Learning    | [Deep learning](https://github.com/Zahrask2/Benchmarks-Groundwater-level-prediction-ML-models-/tree/main/Deep%20learning%20models) |
|Feature Importance| [Feature importance](https://huggingface.co/Kozy9/GWTCN](https://github.com/Zahrask2/Benchmarks-Groundwater-level-prediction-ML-models-#:~:text=GWL_Feature_Importance.ipynb)) |
| ML Benchmark     | [Benchmark](https://github.com/Zahrask2/Benchmarks-Groundwater-level-prediction-ML-models-#:~:text=GWL_Model_comparison.ipynb)|

## Trained models (Hosted on HuggingFace)

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




## Website

The project website is published via GitHub Pages and provides an accessible visualisation of the research findings:

🔗 [https://zahrask2.github.io/ML-GWL-frocaster/](https://zahrask2.github.io/ML-GWL-frocaster/)

## Ethical Approval

This project received ethical approval from the University of Sheffield. The study uses secondary, non-personal environmental data and does not involve human participants.

## License

This project was completed as part of the IJC319 module at the University of Sheffield.
