# Entrega-Final
# 🍷 Wine Classification & ML Pipeline

## 1. Descripción del Proyecto
Este proyecto implementa un pipeline integral de datos y Machine Learning para la clasificación y análisis de perfiles de vinos a partir de descripciones sensoriales. 

El flujo automatiza:
- La ingesta desde una API externa mediante autenticación segura.
- El procesamiento analítico y tipado en memoria con **Polars** y **DuckDB**.
- La persistencia estructurada en base de datos local SQLite utilizando **SQLAlchemy 2.0**.
- El entrenamiento, búsqueda de hiperparámetros (**GridSearchCV**) y evaluación de un pipeline de clasificación con **Scikit-Learn**.

---

## 2. Estructura del Repositorio
```text
├── config/
│   └── .env.example
├── docs/
│   └── metricas.json
├── src/
│   ├── ingesta.py
│   ├── procesamiento.py
│   └── train.py
├── .gitignore
├── requirements.txt
└── README.md
