Práctica 1 – Perceptrón Multicapa (MLP) para Predicción de Satisfacción Laboral

Este proyecto implementa un Perceptrón Multicapa (MLP) para predecir el nivel de satisfacción de empleados utilizando un dataset de desempeño y productividad.
La práctica está dividida en varias actividades que abarcan:

Análisis exploratorio

Procesamiento de datos

Construcción de modelos MLP

Entrenamiento y evaluación

Visualización de resultados

📊 Descripción del Proyecto

El área de Recursos Humanos recolectó múltiples métricas de desempeño, productividad y comportamiento de los empleados.
El objetivo es estimar el Employee Satisfaction Score, que originalmente es una variable numérica, pero se transforma a 5 categorías (0 a 4) para tratarlo como un problema de clasificación multiclase.

Este proyecto entrena tres arquitecturas diferentes de redes neuronales tipo MLP y evalúa cuál generaliza mejor sobre los datos.

 Contenido de la Práctica
🔹 Actividad 1 – Preparación de Datos

Se realizan las siguientes tareas:

Carga del archivo CSV

Selección de columnas numéricas

Visualización de distribuciones

Estandarización con StandardScaler

División en entrenamiento/prueba (67% / 33%)

Conversión del target a categorías 0–4

One-hot encoding para el entrenamiento con softmax

🔹 Actividad 2 – Implementación de 3 Arquitecturas MLP

Se construyen tres modelos distintos usando TensorFlow/Keras:

🔵 MLP Simple

1 capa densa oculta

Pocas neuronas

Baseline rápido
Ideal para comparar contra modelos más complejos.

🟢 MLP Deep

Arquitectura profunda

Varias capas densas

Aprende patrones más complejos
Adecuado para datasets con relaciones no lineales.

🔴 MLP Regularized

Uso de BatchNormalization

Uso de Dropout

Reduce el riesgo de sobreajuste
Especialmente útil en datasets pequeños o ruidosos.

Cada modelo tiene su propio nombre dentro de Keras.

🔹 Actividad 3 – Compilación y Entrenamiento

Cada modelo se compila con:
optimizer='adam'
loss='categorical_crossentropy'
metrics=['accuracy']

Y se entrena con diferentes cantidades de epochs según su complejidad:

MLP_simple → 50 epochs

MLP_deep → 70 epochs

MLP_regularized → 100 epochs

Además, se entrena con los datos estandarizados y etiquetas one-hot.

🔹 Actividad 4 – Evaluación y Visualización

Se generan:

✔ Gráficas de aprendizaje:

Accuracy vs Epoch

Loss vs Epoch

Comparación entre los tres modelos

✔ Matriz de confusión

Para identificar qué clases se confunden entre sí.

✔ Classification report

Incluye:

Precision

Recall

F1-score

Esto permite determinar qué modelo generaliza mejor y cuál tiene mejor rendimiento global.
