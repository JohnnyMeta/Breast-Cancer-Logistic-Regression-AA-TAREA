# Diagnóstico de Cáncer de Mama con Regresión Logística

Este repositorio contiene el desarrollo práctico de un modelo de clasificación binaria utilizando el algoritmo de **Regresión Logística** sobre el popular dataset *Breast Cancer Wisconsin* de `scikit-learn`. El objetivo principal es evaluar el modelo mediante validación cruzada y optimizar su rendimiento para un entorno de diagnóstico médico real.

## Contenido del Repositorio

*   **`Taller_Clasificacion.ipynb`**: Notebook de Jupyter con todo el código estructurado, celdas ejecutadas, comentarios detallados y la visualización de la matriz de confusión.
*   **`Informe_Final.pdf`**: Reporte formal que contiene el análisis comparativo de métricas, justificación clínica del modelo y las conclusiones analíticas.

## Resumen de Resultados Obtenidos

A continuación se presentan las métricas clave obtenidas tras el entrenamiento del modelo base:

| Métrica | Resultado | Significado Clínico |
| :--- | :---: | :--- |
| **Exactitud (Accuracy)** | 95.61% | Eficiencia global del clasificador. |
| **Precisión (Precision)** | 94.67% | Calidad al predecir tumores benignos. |
| **Sensibilidad (Recall)** | 98.61% | Capacidad crítica para no dejar pacientes enfermos sin detectar. |
| **F1-Score** | 96.60% | Balance óptimo entre falsos positivos y negativos. |
| **AUC-ROC** | 99.40% | Capacidad casi perfecta de separación de clases. |

## Tecnologías y Librerías Utilizadas

*   **Lenguaje:** Python 3
*   **Entorno:** Jupyter Notebook / Google Colab
*   **Librerías Clave:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

## Conclusión del Experimento
El proyecto determinó que la métrica fundamental para este problema de salud pública es el **Recall**, con un umbral de decisión óptimo en `0.5` el cual mantiene la precisión y la sensibilidad del algoritmo sin comprometer vidas humanas.
