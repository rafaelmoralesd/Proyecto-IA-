README: Predicción de Supervivencia en Pacientes con COVID-19 

Este repositorio contiene un proyecto de Inteligencia Artificial desarrollado para predecir la supervivencia de pacientes con COVID-19 basándose en un conjunto de datos médicos. El proyecto utiliza un modelo de Árbol de Decisión y técnicas de preprocesamiento de datos para lograr una predicción precisa.

Estructura del Repositorio
Covid Data.csv: El conjunto de datos original utilizado para el entrenamiento y la evaluación del modelo.

notebook.ipynb: El cuaderno de Colab que contiene todo el código del proyecto, desde la limpieza de datos hasta el entrenamiento del modelo.

Integrantes del Grupo
Andrea Estefanía Andrade Alvarenga (20142003006)

Carlos Eduardo Argueta Rivera (20172001120)

Rafael Ernesto Morales Díaz (20202001873)

Análisis y Preprocesamiento de Datos
El notebook.ipynb realiza una serie de pasos esenciales para preparar los datos antes del entrenamiento del modelo:

Carga del Dataset: El archivo Covid Data.csv se carga directamente en un DataFrame de pandas.

Limpieza y Transformación:

La columna DATE_DIED se usa para crear la variable objetivo alive_patients (1 para vivo, 0 para muerto).

Se eliminan valores nulos y atípicos (como 97 y 99) en columnas clave como PNEUMONIA y AGE.

Se eliminan columnas irrelevantes para el modelo final, como DATE_DIED, INTUBED, ICU y PREGNANT.

Manejo de Desbalance de Clases:

Se aplica la técnica de sobremuestreo SMOTE (Synthetic Minority Over-sampling Technique) para equilibrar las clases de alive_patients, asegurando que el modelo no se sesgue hacia la clase mayoritaria.

Modelo de Machine Learning
Se utiliza un Árbol de Decisión como modelo principal de clasificación.

Entrenamiento: El modelo se entrena con los datos procesados, ajustando sus parámetros para aprender los patrones que diferencian a los pacientes que sobreviven de los que no.

Evaluación: Se utilizan métricas clave como la matriz de confusión y el reporte de clasificación para evaluar la precisión y el rendimiento del modelo en datos de prueba.

Resultados y Visualización
El proyecto incluye visualizaciones para interpretar el modelo:

Matriz de Confusión: Muestra el rendimiento del modelo, indicando el número de predicciones correctas e incorrectas.

Árbol de Decisiones: Se genera un gráfico que visualiza la estructura del árbol, permitiendo entender las decisiones que toma el modelo para llegar a sus predicciones.
