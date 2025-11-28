
---

## **Modelos implementados**

###  **1. Modelo base (CNN desde cero)**
- Arquitectura simple con tres bloques convolucionales
- Entrada: 150×150
- Aumento de datos básico
- Optimizador: Adam (1e-4)

**Precisión final:** ~0.76  
Servió como punto de partida para el resto del proyecto.

---

###  **2. Modelo ajustado (CNN optimizada)**
- Resolución aumentada a 224×224  
- Capas **Batch Normalization** en todos los bloques  
- Inclusión de un **SE Block (Squeeze-and-Excitation)**  
- Regularización con Dropout del 50%  
- Callbacks: EarlyStopping + ReduceLROnPlateau  

**Precisión final:** ~0.88  
Mejor estabilidad y mejor capacidad de generalización.

---

### **3. Transfer Learning con MobileNetV2 (modelo final)**
- MobileNetV2 preentrenada en ImageNet  
- Fase 1: Feature extraction con la base congelada  
- Fase 2: Fine-tuning de las últimas capas  
- Aumento de datos y preprocesamiento acorde al modelo  
- Clasificador denso de 256 neuronas

**Precisión final:** **0.92**  
Mejor desempeño global y menor tasa de error por clase.

Este modelo es el utilizado en la entrega final.

---

## **Resultados generales**

| Modelo                  | Accuracy |
|-------------------------|----------|
| Modelo base             | 0.76     |
| Modelo ajustado         | 0.88     |
| Transfer Learning (TL)  | **0.92** |

El uso de **Transfer Learning** permitió una mejora significativa en el rendimiento sin necesidad de entrenar millones de parámetros desde cero.

---

## **Modelos entrenados**

Debido a su tamaño, los modelos `.keras` **no se incluyen directamente en el repositorio**.  
Puedes descargarlos desde el siguiente enlace:

🔗 **[Enlace de descarga del modelo final (model_tl2.keras)](URL_AQUÍ)**  
*(https://drive.google.com/drive/folders/1x7pUkJoCLf4zFFfLkQnGt5pLG5oY6562?usp=sharing)*






