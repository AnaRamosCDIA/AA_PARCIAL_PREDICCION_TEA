# Predicción del Trastorno del Espectro Autista en Niños mediante Aprendizaje Automático

![Imagen de portada](reports/portada_proyecto_autismo.jpg)

## 📚 Índice

- [1. Descripción del Proyecto](#1-descripción-del-proyecto)
- [2. Objetivos](#2-objetivos)
- [3. Relevancia del Problema](#3-relevancia-del-problema)
  - [3.1. Preguntas de Investigación e Hipótesis](#31-preguntas-de-investigación-e-hipótesis)
- [4. Tipo de Problema](#4-tipo-de-problema)
- [5. Modelos y Evaluación](#5-modelos-y-evaluación)
- [6. Conclusiones Generales](#6-conclusiones-generales)
- [7. Mejor modelo seleccionado](#7-Mejor-Modelo-Seleccionado)
- [8. Aporte a Tierra del Fuego](#8-Aporte-a-Tierra-del-Fuego)
- 📘 [9. Notebooks del Proyecto](#9-notebooks-del-proyecto)
- 📄 [10. Informes Tecnicos del Proyecto](#10-informes-tecnicos-del-proyecto)
- 🎥 [11. Video Presentacion del Proyecto](#11-video-presentacion-del-proyecto)
---

## 1. Descripción del Proyecto

Este proyecto investiga la viabilidad de aplicar técnicas de Aprendizaje Automático para predecir indicadores del Trastorno del Espectro Autista (TEA) en niños, basándose en datos de tamizaje y variables sociodemográficas, entre otras. El objetivo es construir modelos que permitan identificar casos compatibles con el TEA de forma temprana, especialmente en contextos con acceso limitado a diagnóstico especializado como Tierra del Fuego.

## 2. Objetivos

### General
Desarrollar un modelo de clasificación binaria que prediga la presencia de indicios de TEA en niños.

### Específicos
- Realizar EDA y limpieza del dataset.
- Entrenar Regresión Logística, Árbol de Decisión y Random Forest.
- Comparar métricas de desempeño.
- Evaluar aplicabilidad real del modelo en contextos como Tierra del Fuego.

## 3. Relevancia del Problema

EEl diagnóstico temprano del TEA es fundamental para implementar intervenciones que favorezcan el desarrollo integral del niño. Sin embargo, en regiones con escasos recursos diagnósticos y limitaciones geográficas —como Tierra del Fuego—, los tiempos de espera para una evaluación clínica especializada pueden ser prolongados.
En este contexto, contar con herramientas tecnológicas basadas en aprendizaje automático podría facilitar la detección preliminar, sirviendo de apoyo para profesionales de la salud, la educación y las familias. Este proyecto no busca reemplazar el diagnóstico clínico, sino proponer una herramienta que complemente y oriente la derivación oportuna, con una mirada ética y responsable sobre el uso de la inteligencia artificial en salud.

### 3.1. Preguntas e Hipótesis

- ¿Puede predecirse el TEA con datos de tamizaje y variables sociodemográficas?
- ¿Qué variables son más relevantes?
- ¿Qué modelo tiene mejor rendimiento?
- ¿Puede aportar valor en contextos de acceso limitado?

Hipótesis:
- H1: Se puede predecir TEA con buena precisión.
- H2: Variables sociodemográficas influyen.
- H3: Random Forest tendrá mejor F1-score.
- H4: La implementación de modelos predictivos en nuestra provincia puede contribuir a la detección temprana y a la derivación más eficiente de niños para su evaluación clínica.
## 4. Tipo de Problema

Clasificación binaria supervisada. Variable objetivo: `Clase_TEA` (0 = no indicios, 1 = indicios de TEA).

## 5. Modelos y Evaluación

Modelos implementados:
- Regresión Logística
- Árbol de Decisión
- Random Forest

Métricas utilizadas:
- Accuracy
- Precision
- Recall
- F1-score
- Matriz de Confusión
- AUC-ROC
- Curva Precisión-Recall
- Validación cruzada
- Optimización de hiperparámetros

## 6. Conclusiones Generales

- Regresión Logística demostró un desempeño sobresaliente en el conjunto de test, alcanzando una precisión global del 98% y sin falsos negativos, lo que la hace una opción confiable para tareas de cribado preliminar.

- Random Forest, especialmente en su versión optimizada con GridSearchCV (n_estimators=200, max_depth=10, min_samples_split=5), fue el modelo más robusto y generalizable. Alcanzó un F1-score de 0.90, junto con métricas avanzadas sobresalientes: AUC-ROC = 0.99 y Curva PR = 0.99, además de una precisión promedio del 94.8% en validación cruzada, lo que indica una excelente capacidad para generalizar a nuevos datos.

- Árbol de Decisión aportó interpretabilidad al revelar reglas claras y variables clave para la clasificación, aunque su rendimiento fue más limitado (accuracy del 78%).

- Las variables más predictivas fueron las preguntas del cuestionario AQ-10-Child, que demostraron una mayor capacidad discriminante que las variables sociodemográficas.

- **Conclusión:** El modelo **Random Forest optimizado** fue seleccionado como **el mejor modelo del proyecto por su excelente equilibrio entre rendimiento, estabilidad y capacidad de generalización.

## 7. Mejor Modelo Seleccionado
De acuerdo con la validación cruzada (accuracy promedio de 94.8%), la optimización de hiperparámetros y las curvas de evaluación (AUC-ROC y PR = 0.99), el modelo más robusto y confiable fue el Random Forest optimizado. Si bien la Regresión Logística mostró un desempeño excelente en el conjunto de test (F1 = 0.98), el Random Forest demostró una mejor capacidad de generalización, siendo el más recomendable para implementación práctica en entornos reales.

## 8. Aporte a Tierra del Fuego

Este trabajo propone un modelo funcional que podría utilizarse como herramienta de apoyo en centros educativos o instituciones de salud primaria en Tierra del Fuego, donde el acceso a diagnóstico especializado es limitado. Su aplicación permitiría priorizar derivaciones y reducir los tiempos de espera, favoreciendo la detección e intervención temprana, con un enfoque ético y adaptado al contexto local.

## 9. Notebooks del Proyecto

- 📘 [`EDA_TEA_INFANCIA.ipynb`](notebooks/EDA_TEA_INFANCIA.ipynb)
- 📘 [`Modelos_Predictivos_TEA.ipynb`](notebooks/Modelos_Predictivos_TEA.ipynb)
- 📘 [`Validacion_Optimizacion_Metricas_TEA.ipynb`](notebooks/Validacion_Optimizacion_Metricas_TEA.ipynb)

## 10. Informes Tecnicos del Proyecto

- 📄 [`Descripcion_Dataset_Original.pdf`](reports/Descripcion_Dataset_Original.pdf)
- 📄 [`Descripcion_Dataset_Procesado.pdf`](reports/Descripcion_Dataset_Procesado.pdf)
- 📄 [`Conclusiones.pdf`](reports/Conclusiones.pdf)

## 11. Video Presentacion del Proyecto

Podés acceder al video de presentación en el siguiente enlace de Google Drive:

[🎥 Ver video en Google Drive](https://drive.google.com/file/d/19OvDQnVg9FBSFvwIkMHrG7MivOcxXeO2/view?usp=sharing)

> Este video resume el objetivo, metodología y resultados clave del proyecto de predicción de TEA en niños mediante Aprendizaje Automático.



