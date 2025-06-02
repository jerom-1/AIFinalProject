

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
