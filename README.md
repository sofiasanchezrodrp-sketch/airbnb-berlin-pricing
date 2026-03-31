# Airbnb Berlín — Predicción de precios

Pipeline completo de machine learning para predecir el precio de alojamientos en Airbnb Berlín, desde la limpieza de datos hasta un dashboard interactivo en Power BI.

## Resultados

| Modelo | RMSE | MAE | R² |
|---|---|---|---|
| XGBoost + log_price | 46.67€ | 31.18€ | 0.61 |
| XGBoost | 46.94€ | 32.69€ | 0.61 |
| Random Forest | 47.15€ | 32.96€ | 0.61 |
| Regresión Lineal | 53.26€ | 35.79€ | 0.50 |

**Mejor modelo:** XGBoost con transformación logarítmica del target — RMSE de 46.67€ y R² de 0.61.

## Estructura del proyecto
```
├── notebooks/
│   ├── 01_eda_cleaning.ipynb
│   ├── 02_eda_visualization.ipynb  
│   ├── 03_feature_engineering.ipynb
│   └── 04_modeling.ipynb
└── dashboard/
    └── airbnb_berlin.pbix
```

## Pipeline

1. **EDA y limpieza** — selección de variables, tratamiento de nulos y análisis de outliers
2. **Visualización** — distribución de precios, correlaciones y análisis por barrios
3. **Feature engineering** — creación de variables derivadas: `log_price`, `price_per_person`, `neighbourhood_median_price`, `amenities_count`, `days_since_last_review`, `is_entire_home`
4. **Modelado** — comparativa de 5 modelos con optimización de hiperparámetros mediante GridSearchCV

## Tecnologías

- Python, Pandas, Scikit-learn, XGBoost
- Power BI Desktop
- Dataset: [Inside Airbnb — Berlin](http://insideairbnb.com/berlin)
