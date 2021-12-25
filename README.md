# Modelos de aprendizaje automático para el diagnóstico no invasivo de la diabetes mellitus

Este repositorio contiene los notebooks de toda la experimentación desarrollada en el Trabajo Fin de Máster *Modelos de aprendizaje automático para el diagnóstico no invasivo de la diabetes mellitus*.

## Organización del repositorio

En la carpeta [`datos`](./datos) se encuentran los ficheros `Full statistics.xls` (y su transformación a fichero `.csv`) y `For LDA grapgh.xls` obtenidos del [trabajo](https://zenodo.org/record/2525358#.YbFAQNDMLIX) de Dremin et al. (2017). Además, se encuentran los siguientes ficheros:
- [`preprocesamiento_datos.ipynb`](./datos/preprocesamiento_datos.ipynb): notebook con la carga inicial del dataset y su transformación para obtener un conjunto de datos con el que trabajar. Este conjunto de datos se almacena en el fichero `datos.csv` y se crea otra dataset con las clases en _one-hot encoding_, almacenado en el fichero `datos_onehot.csv`.
- [`cargar_datos.ipynb`](./datos/cargar_datos.ipynb) y [`cargar_datos_onehot.ipynb`](./datos/cargar_datos_onehot.ipynb) son dos notebooks de prueba de carga de los dos conjuntos de datos creados anteriormente.
- [`analisis_exploratorio.ipynb`](./datos/analisis_exploratorio.ipynb): notebook en el que se realiza el análisis exploratorio de los datos (_EDA_) del conjunto de datos `datos.csv` para entender cómo están distribuidos y familiarizarse un poco más con ellos. Tras las correcciones oportunas se obtiene el dataset filtrado con el que trabajarán los modelos. Este se almacena en `datos_filtrados.csv`.

En  el directorio raíz se encuentran los notebooks de cada uno de los modelos creados y evaluados. Estos son:

#### Árboles de decisión
- [Separación de datos 80-20%](./arboles_decision_80-20.ipynb)
- [Separación de datos 70-30%](./arboles_decision_70-30.ipynb)
- [Separación de datos 60-40%](./arboles_decision_60-40.ipynb)
- [Separación de datos 80-20% sin filtrar](./arboles_decision_80-20_raw.ipynb)
- [Separación de datos 70-30% sin filtrar](./arboles_decision_70-30_raw.ipynb)
- [Separación de datos 60-40% sin filtrar](./arboles_decision_60-40_raw.ipynb)


#### Random forest
- [Separación de datos 80-20%](./random_forest_80-20.ipynb)
- [Separación de datos 70-30%](./random_forest_70-30.ipynb)
- [Separación de datos 60-40%](./random_forest_60-40.ipynb)
- [Separación de datos 80-20% sin filtrar](./random_forest_80-20_raw.ipynb)
- [Separación de datos 70-30% sin filtrar](./random_forest_70-30_raw.ipynb)
- [Separación de datos 60-40% sin filtrar](./random_forest_60-40_raw.ipynb)


#### kNN
- [Separación de datos 80-20%](./knn_80-20.ipynb)


#### Naive Bayes
- [Separación de datos 80-20%](./naive_bayes_80-20.ipynb)


#### SVM
- [Separación de datos 80-20%](./svm_80-20.ipynb)


#### Red neuronal artificial
- [Separación de datos 80-20%](./red_neuronal_80-20.ipynb)

## Resultados obtenidos
A continuación se muestran las tablas comparativas de los resultados obtenidos en la evaluación de los modelos presentados.

#### Árboles de decisión

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 87.5% | 90.74% | 92.78% | 90.39% |
| 70%-30% (Datos filtrados) | 86.11% | 76.72% | 91.08% | 80.91% |
| 60%-40% (Datos filtrados) | 64.58% | 50.15% | 79.08% | 0% |
| 80%-20% (Datos sin filtrar) | 88% | 90.56% | 93.7% | 87.2% |
| 70%-30% (Datos sin filtrar) | 76.32% | 63.07% | 86.06% | 64.11% |
| 60%-40% (Datos sin filtrar) | 82% | 74.07% | 89.99% | 74.5% |

#### Random forest

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 79.17% | 75.93% | 87.22% | 79.26% |
| 70%-30% (Datos filtrados) | 86.11% | 77.25% | 91.41% | 80.94% |
| 60%-40% (Datos filtrados) | 87.5% | 90.96% | 93.33% | 86.57% |
| 80%-20% (Datos sin filtrar) | 84% | 71.67% | 90.09% | 74.87% |
| 70%-30% (Datos sin filtrar) | 81.58% | 86.32% | 91.12% | 78.57% |
| 60%-40% (Datos sin filtrar) | 84% | 79.2% | 90.48% | 80.03% |

#### kNN

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 70.83% | 52.78% | 81.11% | 0% |
| 70%-30% (Datos filtrados) | 88.89% | 79.1% | 92.93% | 83% |
| 60%-40% (Datos filtrados) | 87.5% | 74.96% | 91.98% | 78.87% |
| 80%-20% (Datos sin filtrar) | 68% | 50.56% | 79.83% | 0% |
| 70%-30% (Datos sin filtrar) | 76.32% | 56.02% | 84.52% | 0% |
| 60%-40% (Datos sin filtrar) | 78% | 66.34% | 86.17% | 69.17% |

#### Naive Bayes

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 83.33% | 79.63% | 90.63% | 79.63% |
| 70%-30% (Datos filtrados) | - | - | - | - |
| 60%-40% (Datos filtrados) | - | - | - | - |
| Datos sin filtrar (80%-20%) | - | - | - | - |

#### SVM

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 87.5% | 82.41% | 92.78% | 85.29% |
| 70%-30% (Datos filtrados) | - | - | - | - |
| 60%-40% (Datos filtrados) | - | - | - | - |
| Datos sin filtrar (80%-20%) | - | - | - | - |

#### Red neuronal artificial

|  | Exactitud | Sensibilidad | Especificidad | F1-score |
| --- |:---:|:---:|:---:|:---:|
| 80%-20% (Datos filtrados) | 91.67% | 93.52% | 95% | 93.52% |
| 70%-30% (Datos filtrados) | - | - | - | - |
| 60%-40% (Datos filtrados) | - | - | - | - |
| Datos sin filtrar (80%-20%) | - | - | - | - |

