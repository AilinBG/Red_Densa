# Red Neuronal Densa para Clasificación de MNIST

## Descripción

Este repositorio contiene el desarrollo de una red neuronal densa secuencial para la clasificación del conjunto de datos MNIST, utilizando TensorFlow/Keras.

Se realizaron experimentos de búsqueda de hiperparámetros mediante Optuna y se registraron los experimentos utilizando MLflow y DagsHub. Posteriormente, se evaluó el efecto de diferentes técnicas de regularización sobre la arquitectura seleccionada.

## Contenido

- `MNIST_Optuna_MLflow_Regularizacion.ipynb`  
  Notebook con el código completo de la práctica, incluyendo:
  - Preprocesamiento del conjunto MNIST.
  - Diseño y entrenamiento de redes neuronales densas.
  - Búsqueda de hiperparámetros con Optuna.
  - Selección de la mejor arquitectura.
  - Evaluación del modelo base.
  - Aplicación de L1, L2, L1-L2, Dropout y Dropout + L1-L2.
  - Registro de experimentos mediante MLflow.

- `Reporte_Optuna_MLflow_Regularizacion.pdf`  
  Reporte final de la práctica con la metodología, resultados y conclusiones.

## Mejor arquitectura encontrada

La búsqueda con Optuna seleccionó una red con:

- 3 capas densas ocultas.
- 448 neuronas en la primera capa.
- 384 neuronas en la segunda capa.
- 192 neuronas en la tercera capa.
- Función de activación ReLU.
- Optimizador RMSprop.
- Learning rate de aproximadamente 0.00118.
- Batch size de 64.

La mejor accuracy de validación obtenida durante la búsqueda fue de aproximadamente **98.43%**.

## Regularización

La arquitectura seleccionada se utilizó posteriormente para comparar diferentes técnicas de regularización:

- L1
- L2
- L1-L2
- Dropout
- Dropout + L1-L2

Los experimentos fueron registrados mediante MLflow y pueden consultarse en DagsHub.

## Registro de experimentos

Los experimentos pueden consultarse en:

[DagsHub - Red_Densa](https://dagshub.com/AilinBG/Red_Densa)

## Tecnologías utilizadas

- Python
- TensorFlow / Keras
- Optuna
- MLflow
- DagsHub
- Google Colab
- MNIST
