
## Clasificación de Imágenes con PyTorch

### Descripción del Problema

Este proyecto de inteligencia artificial implementa un modelo de aprendizaje profundo para **clasificar imágenes**. Las imágenes son convertidas a escala de grises, redimensionadas y normalizadas antes de ser alimentadas a una red neuronal. El objetivo es construir un clasificador robusto utilizando PyTorch y un flujo de trabajo reproducible.

Este tipo de solución es útil en contextos como:

* Diagnóstico médico por imágenes (radiografías, escáneres, etc.).
* Reconocimiento visual en sistemas industriales.
* Clasificación automática de contenido visual.

---

### Estructura del Proyecto

* **Carga de bibliotecas**: Se importan librerías como `torch`, `torchvision`, `sklearn`, `numpy`, y `PIL`.
* **Preprocesamiento de imágenes**:

  * Conversión a escala de grises.
  * Redimensionamiento a 150x150 píxeles.
  * Normalización.
* **Carga del dataset**:

  * Uso de `ImageFolder` para organizar las imágenes.
  * División estratificada en entrenamiento, validación y test.
* **Construcción del modelo**:

  * Red neuronal convolucional personalizada.
* **Entrenamiento del modelo**:

  * Uso de `CrossEntropyLoss` y optimizador `Adam`.
  * Entrenamiento por múltiples épocas con evaluación en validación.
* **Evaluación**:

  * Se mide la precisión en el conjunto de prueba.
* **Visualización de métricas**:

  * Pérdida (loss) y precisión (accuracy) por época.

---

### Consideraciones Importantes

* El archivo `ai-competition01-jerom` incluido en este repositorio **debe ser utilizado como benchmark oficial** para evaluar el rendimiento del modelo implementado.
* Los datos utilizados para entrenar la red fueron y **deben ser obtenidos directamente desde la Competición 1 alojada en Kaggle**. Asegúrate de descargarlos desde la fuente original para mantener la coherencia con la evaluación y los resultados esperados.

---

### Cómo Ejecutar el Proyecto

#### 1. Pre-requisitos

Asegúrate de tener instalado:

```bash
pip install torch torchvision matplotlib numpy scikit-learn
```

#### 2. Organización de Archivos

Estructura esperada:

```
proyecto_IA.ipynb
ai-competition01-jerom
/dataset/
    ├── clase1/
    │   ├── img1.jpg
    │   └── img2.jpg
    └── clase2/
        ├── img3.jpg
        └── img4.jpg
```

#### 3. Ejecutar el notebook

Puedes ejecutar el proyecto desde Jupyter o VSCode:

```bash
jupyter notebook proyecto_IA.ipynb
```

Luego corre las celdas secuencialmente.

---

### Resultados Esperados

* Precisión del modelo en test.
* Visualización de la pérdida y precisión por época.
* Clasificación de imágenes nuevas.

---

### Tecnologías Usadas

* Python 3
* PyTorch
* torchvision
* scikit-learn
* PIL
* matplotlib

---

### Mejora Potenciales

* Implementación de **data augmentation** para mejorar la robustez del modelo.
* Inclusión de **técnicas de regularización** (dropout, batch normalization).
* Experimentación con **transfer learning** usando modelos preentrenados.
* Uso de métricas adicionales: F1-score, matriz de confusión, ROC-AUC.
* Exportación del modelo entrenado con `torch.save()` para uso en producción o inferencia por lotes.

---

### Reproducibilidad

Para asegurar la reproducibilidad:

* Se establecen semillas aleatorias (`torch.manual_seed`) en el notebook.
* La división de los datos es estratificada.
* Los hiperparámetros usados (como tamaño del lote, tasa de aprendizaje y número de épocas) están documentados y configurados explícitamente.

---

### Autor

Desarrollado por Jerónimo Osorio Muñoz, Valentina Ortega Vargas, Sofia Castaño Pulgarin, Sebastian Tapias Gomez, como parte del proyecto final de inteligencia artificial.

