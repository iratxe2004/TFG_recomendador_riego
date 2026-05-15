# TFG Recomendador de Riego

Este repositorio contiene los notebooks desarrollados para el Trabajo Fin de Grado sobre un sistema de recomendación de riego basado en datos de sensores y meteorología, utilizando técnicas de aprendizaje automático y explicabilidad (SHAP y DiCE).

## Contenido del repositorio

### Notebooks

1. **01_analisis_exploratorio_datos.ipynb** – Exploración inicial de los datos y visualización de patrones.  
2. **02_preprocesamiento_datos.ipynb** – Limpieza, interpolación y preparación de los datos de sensores.  
3. **03_web_scrapping_ivia.ipynb** – Extracción de datos meteorológicos del IVIA.  
4. **04_preprocesado_datos_ivia.ipynb** – Limpieza y estructuración de los datos meteorológicos.  
5. **05_agregacion_diaria.ipynb** – Agregación diaria de variables ambientales y de riego.  
6. **06_agregacion_horaria.ipynb** – Agregación horaria y preparación de datasets para entrenamiento.  
7. **07_entrenamiento_clasificador_simple.ipynb** – Entrenamiento de un clasificador simple para estrés hídrico.  
8. **08_entrenamiento_clasificador_extendido.ipynb** – Entrenamiento de un clasificador extendido con variables adicionales.  
9. **09_dice_modelo_rf_simple_final.ipynb** – Generación de explicaciones contrafactuales con DiCE.  
10. **10_entrenamiento_modelo_pico.ipynb** – Entrenamiento de modelo para estimar el máximo de humedad tras riego.  
11. **11_fase_inferencia_recomendador.ipynb** – Fase de inferencia y generación de recomendaciones finales.

### CSVs incluidos

- `data_daily_agg.csv` – agregación diaria de variables ambientales y de riego.  
- `data_hourly_agg.csv` – agregación horaria, usada en modelos de predicción y entrenamiento.  
- `dataset_learning_24h.csv` – dataset para entrenamiento de clasificador simple y extendido.

> Por limitaciones de espacio, los datos originales (`year_all.csv` y crudos del IVIA) no se incluyen. En su lugar, se proporcionan los CSVs ya interpolados y procesados, con los que es posible ejecutar **todos los notebooks a partir del preprocesamiento**.

### CSVs generados dentro de los notebooks

Algunos CSVs utilizados por notebooks posteriores se generan automáticamente durante la ejecución de los notebooks iniciales. Entre ellos se encuentran archivos de resultados intermedios, métricas y datasets derivados. Por lo tanto, **no es necesario subirlos al repositorio** para reproducir el flujo de análisis y entrenamiento.

## Uso

1. Instalar dependencias: Python 3.9+, `pandas`, `numpy`, `scikit-learn`, `shap`, `dice-ml`, `matplotlib`, `seaborn`.  
2. Ejecutar los notebooks en orden. Con los CSVs incluidos, se puede reproducir todo el flujo de análisis, entrenamiento de modelos y generación de recomendaciones a partir del preprocesamiento.

## Licencia

Este proyecto es parte del Trabajo Fin de Grado de Iratxe Sanjuan Nàcher, 2026.
