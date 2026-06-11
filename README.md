# Diagnóstico de Cáncer de Mama con Regresión Logística

Este repositorio contiene el desarrollo práctico de un modelo de clasificación binaria utilizando el dataset *Breast Cancer Wisconsin* de `scikit-learn`. 
El objetivo principal es evaluar el modelo mediante validación cruzada y optimizar su rendimiento para un entorno de diagnóstico médico real.

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

## Eficiencia en la Optimización (Grid vs Random)

Ambos métodos de búsqueda encontraron la misma combinación óptima de hiperparámetros (`{'C': 10, 'penalty': 'l2'}`) alcanzando un F1-Score idéntico de **0.9596**, pero con una notable diferencia en recursos computacionales:

*   **GridSearchCV:** 4.7364 segundos (Búsqueda exhaustiva completa).
*   **RandomizedSearchCV:** 2.1909 segundos (**Ahorro del 53.7% en tiempo de cómputo**).

## Tecnologías y Librerías Utilizadas

*   **Lenguaje:** Python 3
*   **Entorno:** Jupyter Notebook / Google Colab
*   **Librerías Clave:** `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`

## Conclusión del Experimento
El proyecto determinó de forma empírica que el modelo posee una estabilidad diagnóstica sobresaliente. Al evaluar los umbrales de decisión, la sensibilidad (*Recall*) se mantuvo estricta en su nivel máximo de **98.61%** a través de todos los escenarios, permitiendo que un ajuste de umbral exigente en **0.7** elevara la precisión al **95.95%** y consolidara el punto de equilibrio óptimo del experimento (F1-Score de **0.9726**). Esto demuestra que el algoritmo es capaz de mitigar falsos positivos sin comprometer de ninguna manera la detección de pacientes enfermos.
