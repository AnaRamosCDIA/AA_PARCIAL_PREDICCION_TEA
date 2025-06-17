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
- [📁 Notebooks del Proyecto](#notebooks-del-proyecto)
- [📝 Informes Técnicos del Proyecto](#informes-técnicos-del-proyecto)

---

## 1. Descripción del Proyecto

Este proyecto investiga la viabilidad de aplicar técnicas de Aprendizaje Automático para predecir indicadores del Trastorno del Espectro Autista (TEA) en niños, basándose en datos de tamizaje y variables sociodemográficas. El objetivo es construir modelos que permitan identificar casos compatibles con el TEA de forma temprana, especialmente en contextos con acceso limitado a diagnóstico especializado como Tierra del Fuego.

## 2. Objetivos

### General
Desarrollar un modelo de clasificación binaria que prediga la presencia de indicios de TEA en niños.

### Específicos
- Realizar EDA y limpieza del dataset.
- Entrenar Regresión Logística, Árbol de Decisión y Random Forest.
- Comparar métricas de desempeño.
- Evaluar aplicabilidad real del modelo en contextos como Tierra del Fuego.

## 3. Relevancia del Problema

El diagnóstico temprano del TEA mejora significativamente la intervención en salud y educación. Este proyecto ofrece una herramienta de apoyo que puede servir para priorizar derivaciones clínicas en zonas con dificultades de acceso al diagnóstico.

### 3.1. Preguntas e Hipótesis

- ¿Puede predecirse el TEA con datos de tamizaje?
- ¿Qué variables son más relevantes?
- ¿Qué modelo tiene mejor rendimiento?
- ¿Puede aportar valor en contextos de acceso limitado?

Hipótesis:
- H1: Se puede predecir TEA con buena precisión.
- H2: Variables sociodemográficas influyen.
- H3: Random Forest tendrá mejor F1-score.
- H4: El modelo puede ayudar a mejorar la derivación en Tierra del Fuego.

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
- AUC-ROC y Curva PR (solo en RF optimizado)

## 6. Conclusiones Generales

- La Regresión Logística logró mayor precisión global (98%).
- Random Forest alcanzó mejor balance entre precisión y recall (F1 = 0.91).
- Árbol de Decisión fue útil para interpretabilidad.
- Este modelo puede servir como apoyo a decisiones clínicas y educativas en Tierra del Fuego.

---

## 📁 Notebooks del Proyecto

- 📘 [`EDA_TEA_INFANCIA.ipynb`](notebooks/EDA_TEA_INFANCIA.ipynb)
- 🤖 [`Modelos_Predictivos_TEA.ipynb`](notebooks/Modelos_Predictivos_TEA.ipynb)
- 🧪 [`Notebook_Validacion_Optimizacion_Metricas_TEA.ipynb`](notebooks/Notebook_Validacion_Optimizacion_Metricas_TEA.ipynb)

## 📝 Informes Técnicos del Proyecto

- 📄 [`Descripcion_Dataset_Original.pdf`](reports/Descripcion_Dataset_Original.pdf)
- 📄 [`Descripcion_Dataset_Procesado.pdf`](reports/Descripcion_Dataset_Procesado.pdf)
