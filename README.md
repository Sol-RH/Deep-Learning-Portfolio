# Intel Image Classification – Deep Learning

Este proyecto implementa una red neuronal convolucional (CNN) en Keras + TensorFlow
para clasificar imágenes naturales del dataset **Intel Image Classification**. Las categorías son:
`buildings`, `forest`, `glacier`, `mountain`, `sea` y `street`.

## Estructura del proyecto
- `intel_image_classification.ipynb`: Notebook principal con entrenamiento, ajuste y evaluación.
- `model_adjusted.keras`: Modelo final entrenado.

## Modelo
Se desarrolló un modelo CNN con aumento de datos y capas de Batch Normalization,
entrenado con optimizador Adam y tasa de aprendizaje de 2e-4.

El modelo alcanzó una **precisión de 81%** en el conjunto de prueba.



