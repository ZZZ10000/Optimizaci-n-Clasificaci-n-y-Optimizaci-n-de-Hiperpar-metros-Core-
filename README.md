Proyecto de Clasificación y Optimización de Hiperparámetros
Este proyecto implementa un pipeline completo de machine learning para abordar un problema de clasificación utilizando el Medical Cost Personal Dataset. El objetivo es predecir la categoría de los costos médicos basándose en diversas características del paciente. Se enfoca en el preprocesamiento de datos, la implementación de modelos de clasificación y la optimización de hiperparámetros utilizando GridSearchCV y RandomizedSearchCV.

Contenido del Notebook:
Carga y Exploración Inicial de Datos:

Carga del dataset insurance.csv.
Exploración de la estructura del dataset.
Identificación de valores faltantes (no se encontraron en este dataset).
Generación de estadísticas descriptivas.
Preprocesamiento de Datos:

Identificación de columnas categóricas y numéricas.
Aplicación de StandardScaler a características numéricas.
Aplicación de OneHotEncoder a variables categóricas.
Combinación de las características procesadas.
Creación de una variable objetivo categórica (charges_category) a partir de los costos médicos originales (charges).
Implementación de Modelos de Clasificación:

División de los datos en conjuntos de entrenamiento y prueba.
Entrenamiento y evaluación inicial de tres modelos:
Regresión Logística
K-Nearest Neighbors (KNN)
Árbol de Decisión
Evaluación utilizando validación cruzada.
Optimización de Hiperparámetros:

Implementación de GridSearchCV para optimizar hiperparámetros.
Implementación de RandomizedSearchCV para optimizar hiperparámetros.
Comparación de los mejores resultados de validación cruzada obtenidos por ambos métodos para cada modelo.
Evaluación de Modelos Optimizados:

Evaluación de los modelos optimizados en el conjunto de prueba.
Cálculo de métricas de rendimiento (Exactitud, Precisión, Recall, F1-Score).
Generación y visualización de matrices de confusión.
Generación y visualización de curvas ROC (usando estrategia One-vs-Rest para clasificación multiclase).
Hallazgos Clave:
El dataset inicial no contenía valores faltantes.
La optimización de hiperparámetros, especialmente con RandomizedSearchCV, mejoró el rendimiento de los modelos en comparación con la evaluación inicial.
El Árbol de Decisión optimizado con RandomizedSearchCV demostró ser el modelo con mejor rendimiento para esta tarea de clasificación, obteniendo la mejor precisión de validación cruzada y métricas sólidas en el conjunto de prueba.
Conclusiones:
El pipeline implementado permitió cargar, preprocesar y modelar los datos de costos médicos. La comparación entre GridSearchCV y RandomizedSearchCV mostró que este último fue eficiente para encontrar hiperparámetros competitivos. El Árbol de Decisión optimizado con RandomizedSearchCV se identifica como el modelo más adecuado para predecir la categoría de costos médicos en este dataset.

