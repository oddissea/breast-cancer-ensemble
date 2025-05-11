# Análisis predictivo de cáncer de mama con algoritmos ensemble

Este repositorio contiene la implementación de un análisis completo de minería de datos aplicado al conjunto "Breast Cancer Wisconsin (Diagnostic)" utilizando algoritmos ensemble con énfasis en Random Forest.

## Descripción del proyecto

El proyecto aborda la clasificación de tumores mamarios (benignos o malignos) mediante técnicas avanzadas de preprocesamiento, selección de variables y algoritmos ensemble. Se desarrollaron y optimizaron múltiples modelos, evaluando su rendimiento y aplicando técnicas de explicabilidad para proporcionar interpretaciones clínicamente relevantes.

## Características principales

- **Análisis exploratorio**: Evaluación estadística exhaustiva de 30 variables morfológicas de núcleos celulares, identificando patrones discriminativos entre clases.
  
- **Preprocesamiento adaptativo**: Transformaciones específicas basadas en el nivel de asimetría de cada variable (logarítmica, Yeo-Johnson, normalización robusta por clase).
  
- **Selección híbrida de variables**: Combinación de métodos basados en Random Forest, Extra Trees, ANOVA F-value e información mutua, complementada con análisis de redundancia mediante clustering jerárquico.
  
- **Modelado ensemble**: Implementación de múltiples algoritmos (Random Forest, Extra Trees, Bagging) con diferentes clasificadores base, evaluados contra modelos de referencia.
  
- **Optimización de hiperparámetros**: Búsqueda exhaustiva y validación cruzada para determinar configuraciones óptimas, logrando reducciones de complejidad del 75-90% sin comprometer el rendimiento.
  
- **Explicabilidad con SHAP**: Análisis de importancia global e interpretación de predicciones individuales para facilitar la comprensión clínica.

## Estructura del repositorio

- `notebooks/`
  - `a_analisis.ipynb`: Análisis exploratorio de datos
  - `b_preprocesado.ipynb`: Preprocesamiento y tratamiento de datos
  - `c_seleccion_variables.ipynb`: Métodos de selección de variables
  - `d_modelado.ipynb`: Implementación de modelos base y ensemble
  - `e_optimizacion.ipynb`: Optimización de hiperparámetros
  - `f_explicabilidad.ipynb`: Técnicas de explicabilidad e interpretabilidad

- `data/`: Directorios con datos en diferentes etapas de procesamiento
  - `raw/`: Datos originales
  - `preprocessed/`: Datos transformados
  - `processed/`: Datos con variables seleccionadas
  - `models/`: Modelos entrenados
  - `optimizados/`: Modelos con hiperparámetros optimizados

- `results/`: Visualizaciones y resultados de los diferentes análisis
  - `preprocesamiento/`: Gráficos de transformaciones y normalización
  - `seleccion_variables/`: Visualizaciones de importancia de variables
  - `model/`: Matrices de confusión y métricas de evaluación
  - `explicabilidad/`: Gráficos SHAP y análisis de interpretabilidad

## Resultados principales

- Identificación de "worst concave points", "mean concave points" y "mean radius" como las variables más discriminativas para detectar malignidad.
  
- Reducción de dimensionalidad del 40% (de 30 a 18 variables) preservando la capacidad predictiva.
  
- Modelos optimizados con exactitud del 100% (Extra Trees y Bagging-LR) y 99,42% (Random Forest) utilizando configuraciones significativamente simplificadas.
  
- Validación mediante técnicas de explicabilidad (SHAP) de los patrones morfológicos asociados a malignidad, proporcionando transparencia a las predicciones.

## Requisitos

```
numpy==1.24.3
pandas==2.0.3
scikit-learn==1.3.0
matplotlib==3.7.2
seaborn==0.12.2
scipy==1.11.1
shap==0.42.1
```

## Uso

1. Clonar el repositorio:
```
git clone https://github.com/oddissea/breast-cancer-ensemble.git
cd breast-cancer-ensemble
```

2. Instalar dependencias:
```
pip install -r requirements.txt
```

3. Ejecutar los notebooks en orden (a-f) para reproducir el análisis completo.


## Licencia

Este proyecto está bajo la licencia MIT.
