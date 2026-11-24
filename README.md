# Entrega-Final
# 🍷 Clasificación de vino y Pipeline de ML(Wine Classification & ML Pipeline)

## 1. Descripción del Proyecto
Este proyecto implementa un pipeline integral de datos y Machine Learning para la clasificación y análisis de perfiles de vinos a partir de descripciones sensoriales. 

El flujo automatiza:
- La ingesta desde una API externa mediante autenticación segura.
- El procesamiento analítico y tipado en memoria con **Polars** y **DuckDB**.
- La persistencia estructurada en base de datos local SQLite utilizando **SQLAlchemy 2.0**.
- El entrenamiento, búsqueda de hiperparámetros (**GridSearchCV**) y evaluación de un pipeline de clasificación con **Scikit-Learn**.

---
# Pipeline Completo de Ciencia de Datos: Calidad de Vinos

## Descripción del Proyecto
Este proyecto implementa un pipeline de datos integral de extremo a extremo:
1. **Ingesta:** Extracción automatizada de datasets desde fuentes externas consumiendo variables de entorno.
2. **Procesamiento y Normalización:** Limpieza analítica de alto rendimiento integrando **Polars** y transformaciones SQL avanzadas en memoria con **DuckDB**.
3. **Persistencia:** Almacenamiento relacional estructurado en SQLite utilizando **SQLAlchemy 2.0**.
4. **Machine Learning:** Pipeline de **Scikit-Learn** con escalado, clasificación (Random Forest) y optimización de hiperparámetros mediante `GridSearchCV`.

---

## Estructura del Repositorio
```text
├── config/
│   └── .env.example
├── data/
│   └── vinos.db          # Creado automáticamente por el pipeline
├── src/
│   ├── ingesta.py        # Descarga y lectura de datos crudos
│   ├── processing.py     # Transformaciones con Polars y DuckDB
│   ├── database.py       # Modelado ORM y persistencia en SQLite
│   └── train.py          # Pipeline de ML, GridSearchCV y métricas
├── .gitignore
├── requirements.txt
└── README.md
```

---

## Instalación y Configuración

1. **Clonar el repositorio:**
   ```bash
   git clone <https://github.com/gabimazzo-coder/Entrega-Final.git>
   cd <Entrega-Final>
   ```

2. **Crear y activar un entorno virtual (Python 3.12):**
   ```bash
   python -m venv venv
   # En Windows:
   venv\Scripts\activate


3. **Instalar dependencias:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Variables de entorno:**

   ```bash
   cp config/.env.example .env
   ```

---

## Ejecución del Pipeline

Para reproducir el flujo completo de datos y modelado, ejecuta los scripts en orden:

```bash
# 1. Ingesta y almacenamiento intermedio
python src/ingesta.py

# 2. Transformaciones y persistencia relacional
python src/database.py

# 3. Entrenamiento y evaluación del modelo de ML
python src/train.py
```

---

## Resultados y Métricas del Modelo

- **Objetivo:** Clasificación binaria (`es_buena_calidad` >= 7).
- **Algoritmo:** Random Forest Classifier optimizado con validación cruzada (5 folds).
- **Métricas obtenidas en conjunto de test:**
  - **F1-Score (macro/ponderado):** *[0.94]*
  - **ROC-AUC:** *[0,9279]*
  - **Accuracy:** *[0,89]*

