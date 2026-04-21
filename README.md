# Proyecto de Telecomunicaciones

## Descripción General
Este proyecto tiene como objetivo desarrollar un modelo predictivo para identificar a clientes en riesgo de cancelación (churn) para Interconnect, un operador de telecomunicaciones. La meta es permitir que Interconnect implemente estrategias de retención proactivas, como ofertas personalizadas y planes especiales, para reducir la tasa de abandono de clientes y mejorar la satisfacción general del cliente.

## Objetivos del Proyecto
1.  **Carga y Consolidación de Datos**: Integrar información de contratos, datos personales, servicios de internet y servicios telefónicos de los clientes.
2.  **Limpieza y Preprocesamiento de Datos**: Manejar valores nulos, duplicados y tipos de datos incorrectos; crear nuevas características como la antigüedad del cliente (`Tenure`) y la variable objetivo `Churn`.
3.  **Análisis Exploratorio de Datos (EDA)**: Comprender la distribución de los datos, identificar patrones y relaciones entre variables.
4.  **Modelado Predictivo**: Desarrollar y evaluar modelos de clasificación para predecir el churn, incluyendo Regresión Logística, Árboles de Decisión, Random Forest y LightGBM.
5.  **Evaluación de Modelos**: Comparar el rendimiento de los modelos utilizando métricas clave como ROC AUC, F1-Score, Recall y Precision.

### Código de Solución
1.  **Unión de DataFrames**: Se fusionaron los cuatro archivos CSV (`contract.csv`, `personal.csv`, `internet.csv`, `phone.csv`) en un único DataFrame utilizando `customerID`.
2.  **Limpieza y Preprocesamiento de Datos**:
    *   Creación de la variable `Churn` a partir de `EndDate`.
    *   Cálculo de `Tenure` (antigüedad del cliente en meses).
    *   Manejo de valores nulos en `TotalCharges` (imputación con 0).
    *   Imputación de `NaN` en columnas de servicios con 'No' o 'No service'.
    *   Codificación de variables categóricas mediante One-Hot Encoding.
    *   Escalado de características numéricas con `StandardScaler`.
3.  **División de Datos**: El conjunto de datos se dividió en entrenamiento y prueba (80/20) con estratificación.
4.  **Modelado Inicial y Evaluación**: Se entrenaron y evaluaron modelos de Regresión Logística, Árbol de Decisión, Random Forest y LightGBM.

## Resultados Clave
Los modelos de **Regresión Logística** y **LightGBM** mostraron el mejor rendimiento inicial, con ROC AUC scores superiores a 0.84, lo que los convierte en los candidatos más prometedores para futuras optimizaciones. Se observó que el Árbol de Decisión tuvo un rendimiento inferior en comparación.

## Estructura del Repositorio
*   `README.md`: Este archivo.
*   `requirements.txt`: Lista de dependencias de Python.
*   `.gitignore`: Archivos y directorios a ignorar por Git.
*   `Proyecto_Telecomunicaciones.ipynb`: El cuaderno de Jupyter/Colab con todo el código y análisis.
*   `data/`: Directorio que contiene los archivos CSV originales.
    *   `contract.csv`
    *   `personal.csv`
    *   `internet.csv`
    *   `phone.csv`

## Cómo Ejecutar el Proyecto
1.  Clona el repositorio:
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    cd <NOMBRE_DEL_REPOSITORIO>
    ```
2.  Crea un entorno virtual (opcional pero recomendado):
    ```bash
    python -m venv venv
    source venv/bin/activate  # En Windows: .venv\Scripts\activate
    ```
3.  Instala las dependencias:
    ```bash
    pip install -r requirements.txt
    ```
4.  Abre el `notebook.ipynb` en un entorno compatible (Jupyter Lab, Jupyter Notebook, Google Colab).

-----

## 👩‍💻 Autora

*Jenifer Gonzalez*

Data Science | QA Engineer | Scrum Master 

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](www.linkedin.com/in/jenifer-paola-gonzalez-peñuela)
[![GitHub](https://img.shields.io/badge/GitHub-black?style=flat&logo=github)](https://github.com/Jenifer-Gonzalez-DS-QA/jenifergon91))

-----
