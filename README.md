# TFG: Comparación de modelos de ML para la predicción e interpretación de la adherencia
Este cuaderno desarrolla el análisis completo del problema de la adherencia a tratamientos farmacológicos mediante técnicas de ciencia de datos y aprendizaje automático. El objetivo principal es comparar distintos modelos supervisados para predecir la adherencia de los pacientes, así como complementar el análisis con técnicas de interpretabilidad y segmentación.

El flujo de trabajo se estructura en las siguientes fases:

1. **Carga y comprensión del conjunto de datos**

Se importa el dataset para realizar una primera exploración con el objetivo de comprender su estructura y estudiar las variables disponibles.

2. **Análisis exploratorio de datos (EDA)**

Se analizan las distribuciones de las variables, posibles relaciones entre ellas y patrones relevantes que puedan influir en la adherencia al tratamiento.

3. **Preprocesamiento de datos**

Se preparan los datos para el modelado:

- Separación en variables predictoras y variable objetivo
- División en conjuntos de entrenamiento, validación y test
- Definición del pipeline para la transformación de variables numéricas y categóricas
- Aprendizaje supervisado: predicción de adherencia

4.1. **Ajuste y comparación inicial de modelos supervisados**

Se entrenan y comparan distintos modelos de clasificación:

- Regresión Logística
- Random Forest
- Red neuronal (MLP)
- XGBoost
  
La comparación se realiza utilizando métricas como accuracy, precision, recall, F1-score y ROC-AUC.

4.2. **Ajuste del modelo seleccionado****

Se selecciona el modelo con mejor rendimiento (XGBoost) y se optimizan sus hiperparámetros mediante búsqueda aleatoria (RandomizedSearchCV).

4.3. **Optimización del umbral de decisión**

Se ajusta el threshold de clasificación utilizando el conjunto de validación, con el objetivo de mejorar el equilibrio entre precisión y recall, especialmente en la detección de pacientes no adherentes.

4.4. **Evaluación final sobre el conjunto de test**

Se evalúa el modelo final sobre el conjunto de test, obteniendo una estimación realista de su capacidad de generalización.

4.5. **Análisis del sobreajuste**

Se analiza el comportamiento del modelo mediante curvas de aprendizaje, comparando el rendimiento en entrenamiento y validación, con el objetivo de identificar posibles problemas de sobreajuste o infraajuste.

4.6. **Resumen de los modelos supervisados**

Se realiza una comparación global de los modelos evaluados, analizando sus resultados en términos de las métricas consideradas. Este análisis permite evaluar el rendimiento relativo de cada modelo y comprender sus diferencias en función de las métricas utilizadas.

5. **Aprendizaje No supervisado: segmentación de pacientes**

Se aplican técnicas de clustering para identificar perfiles de pacientes con comportamientos similares, complementando así el análisis predictivo con un enfoque descriptivo.

6. **Técnicas de interpretabilidad**

Se analizan las variables más relevantes que influyen en la predicción, con el objetivo de aportar interpretabilidad al modelo y facilitar la comprensión de los factores asociados a la adherencia.
