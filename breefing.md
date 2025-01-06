# eTB - Diagnost

---

## Briefing para Proyecto Personal

---

## Automatización del Diagnóstico Precoz de Tuberculosis con Redes Neuronales Convolucionales

---

### Descripción General

#### Problema a Resolver

En Ucrania, la tuberculosis (TB) sigue siendo un desafío de salud pública significativo. Según datos de la Organización Mundial de la Salud (OMS), en 2022, Ucrania registró aproximadamente 27,000 nuevos casos de tuberculosis, con una incidencia de 63 casos por cada 100,000 habitantes. El sistema de salud realiza cribados anuales masivos mediante radiografías de tórax para la detección temprana, lo que genera una carga considerable para los radiólogos. Este retraso en el diagnóstico puede impactar negativamente en la tasa de detección y tratamiento oportuno.

#### Relevancia

La implementación de herramientas de inteligencia artificial puede aliviar la carga de trabajo de los radiólogos, acelerar el diagnóstico y mejorar los resultados de salud. Automatizar el análisis de radiografías mediante redes neuronales convolucionales (CNN) permite identificar casos sospechosos de tuberculosis con mayor rapidez y precisión.

#### Público Objetivo

- Instituciones de salud pública y privada en Ucrania.
- Radiólogos y técnicos de diagnóstico por imágenes.
- Pacientes adultos sometidos a cribados anuales de TB.

#### Objetivo principal

Diseñar e implementar un modelo basado en redes neuronales convolucionales que automatice la detección de tuberculosis en radiografías de tórax, mejorando la eficiencia y precisión del diagnóstico.

---

### Entregables

- Un artículo en Medium explicando el proyecto, metodología y resultados.
- Repositorio en GitHub.
- Opcional: Una interfaz web demostrativa para subir imágenes y obtener resultados preliminares.

---

### Funcionalidades Propuestas

#### Nivel Esencial

- **Clasificación binaria de imágenes de tórax:** El modelo inicial será capaz de clasificar imágenes como "normal" o "positivo para TB" basándose en un dataset público de radiografías.
- **Entrenamiento de una Red Neuronal Convolucional (CNN):**  Se entrenará un modelo básico CNN utilizando un dataset público de imágenes de radiografías.
- **Métricas Avanzadas:** Implementar métricas de evaluación como sensibilidad, especificidad y precisión para medir el desempeño del modelo, asegurando una correcta identificación de casos positivos y negativos.

#### Nivel Medio

- **Visualización de Activaciones de la CNN (Heatmaps):** Utilizar técnicas como Grad-CAM para visualizar las activaciones de la red neuronal y generar mapas de calor que expliquen cómo el modelo toma decisiones en las imágenes, ayudando a los radiólogos a interpretar los resultados de manera más confiable.
- **Pipeline de Preprocesamiento Automatizado:** Desarrollar un pipeline para la detección y corrección de artefactos comunes en las radiografías (por ejemplo, ruido o malas calidades de imagen), mejorando la calidad de las imágenes antes de ser procesadas por el modelo.
- **Aumento de Datos para Mejorar el Modelo:** Implementar técnicas de aumento de datos (como rotación, zoom, recorte o cambio de iluminación) para aumentar la diversidad del dataset, mejorando así la capacidad del modelo para generalizar y ser más robusto ante variaciones en los datos de entrada.

#### Nivel Avanzado

- **Diagnóstico multi-clase:** Utilización del dataset NIH Chest X-rays para clasificar múltiples enfermedades pulmonares y no solo tuberculosis. Las clases incluyen atelectasia, consolidación, infiltración, neumotórax, entre otras.

#### Nivel Experto

- **Generación de informes en lenguaje natural:** Utilización de un modelo LLM para generar informes detallados y de alta calidad en lenguaje humano, basados en las etiquetas y hallazgos del modelo CNN.
- **Implementación de explicabilidad en el modelo:** Utilización de mapas de saliencia o técnicas de interpretación para mostrar cómo el modelo llega a sus conclusiones y asegurar que los radiólogos puedan confiar en las predicciones.

---

### Tecnologías 

- **Python**
- **TensorFlow / Keras / PyTorch** para el desarrollo del modelo CNN.
- **OpenCV** para el preprocesamiento de imágenes.
- **Hugging Face Transformers** para integrar el modelo de lenguaje natural (LLM) para la generación de informes.
- **Pandas, NumPy, Matplotlib, Seaborn**
- **Google Colab, Jupyter Notebooks**
- **VS Code, GitHub**
- **Gradio/Streamlit**
- **Docker**
- **Google Cloud**

---

### Datos a Utilizar

1. **Dataset de Radiografías de Tórax para la detección de Tuberculosis**: [Tuberculosis TB Chest X-ray Dataset en Kaggle](https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset)
   
2. **Dataset de Radiografías de Tórax (NIH Chest X-rays)**: [NIH Chest X-ray Dataset en Kaggle](https://www.kaggle.com/datasets/nih-chest-xrays/data)

---

### Consideraciones Éticas y de Privacidad


#### Limitaciones

Es importante destacar que este modelo **no debe ser utilizado como un diagnóstico definitivo**. Aunque proporciona una herramienta útil para la detección temprana de la tuberculosis, el modelo debe ser considerado como un apoyo a los radiólogos y médicos especialistas, no como un reemplazo de la interpretación clínica profesional. El uso indebido del modelo podría llevar a errores de diagnóstico, lo que resalta la necesidad de confirmación clínica adicional.

#### Citación

**Tawsifur Rahman, Amith Khandakar, Muhammad A. Kadir, Khandaker R. Islam, Khandaker F. Islam, Zaid B. Mahbub, Mohamed Arselene Ayari, Muhammad E. H. Chowdhury. (2020) "Reliable Tuberculosis Detection using Chest X-ray with Deep Learning, Segmentation and Visualization". IEEE Access, Vol. 8, pp 191586 - 191601. DOI. [10.1109/ACCESS.2020.3031384](https://doi.org/10.1109/ACCESS.2020.3031384).**

#### Otras Citaciones

1. **Wang X, Peng Y, Lu L, Lu Z, Bagheri M, Summers RM.** ChestX-ray8: Hospital-scale Chest X-ray Database and Benchmarks on Weakly-Supervised Classification and Localization of Common Thorax Diseases. *IEEE CVPR 2017*. [ChestX-ray8_Hospital-Scale_Chest_CVPR_2017_paper.pdf](https://arxiv.org/pdf/1705.02315.pdf).

2. **NIH News release**: NIH Clinical Center provides one of the largest publicly available chest x-ray datasets to the scientific community. [Enlace al sitio oficial](https://nihcc.app.box.com/v/ChestXray-NIHCC/folder/36938765345).

#### Nota

Este proyecto refleja un **interés personal** en la aplicación de inteligencia artificial en el campo médico y está alineado con los **objetivos de aprendizaje y desarrollo profesional**. La idea es explorar cómo la inteligencia artificial puede mejorar los procesos de diagnóstico y contribuir al campo de la salud, con un enfoque en la tuberculosis, que es un problema de salud pública relevante en diversas regiones del mundo.

---

#### Alcance

Este proyecto prioriza un modelo **funcional básico**, con el objetivo de implementar una solución escalable en etapas posteriores. Inicialmente, el enfoque será en la creación de un modelo que pueda identificar imágenes de tórax normales y positivas para tuberculosis, utilizando redes neuronales convolucionales (CNN). En el futuro, se pueden agregar más características, como la clasificación de otros tipos de enfermedades pulmonares, y mejorar la precisión y robustez del modelo.

---
