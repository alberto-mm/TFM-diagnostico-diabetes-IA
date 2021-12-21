# Modelos de aprendizaje automático para el diagnóstico no invasivo de la diabetes mellitus

Este repositorio contiene los notebooks de toda la experimentación desarrollada en el Trabajo Fin de Máster *Modelos de aprendizaje automático para el diagnóstico no invasivo de la diabetes mellitus*.

## Organización del repositorio

- En la carpeta [`datos`](./datos) se encuentran los ficheros `Full statistics.xls` (y su transformación a fichero `.csv`) y `For LDA grapgh.xls` obtenidos del [trabajo](https://zenodo.org/record/2525358#.YbFAQNDMLIX) de Dremin et al. (2017). Además, se encuentran los siguientes ficheros:
	* [`preprocesamiento_datos.ipynb`](./datos/preprocesamiento_datos.ipynb): notebook con la carga inicial del dataset y su transformación para obtener un conjunto de datos con el que trabajar. Este conjunto de datos se almacena en el fichero `datos.csv` y se crea otra dataset con las clases en _one-hot encoding_, almacenado en el fichero `datos_onehot.csv`.
	* [`cargar_datos.ipynb`](./datos/cargar_datos.ipynb) y [`cargar_datos_onehot.ipynb`](./datos/cargar_datos_onehot.ipynb) son dos notebooks de prueba de carga de los dos conjuntos de datos creados anteriormente.
	* [`analisis_exploratorio.ipynb`](./datos/analisis_exploratorio.ipynb): notebook en el que se realiza el análisis exploratorio de los datos (_EDA_) del conjunto de datos `datos.csv` para entender cómo están distribuidos y familiarizarse un poco más con ellos. Tras las correcciones oportunas se obtiene el dataset filtrado con el que trabajarán los modelos. Este se almacena en `datos_filtrados.csv`.
- En  el directorio raíz se encuentran los notebooks de cada uno de los modelos creados y evaluados. Estos son:
	* [Árboles de decisión](./arboles_decision.ipynb)
	* [Random forest](./random_forest.ipynb)
	* [kNN](./knn.ipynb)
	* [Naive Bayes](./naive_bayes.ipynb)
	* [SVM](./svm.ipynb)
	* [Red neuronal artificial](./red_neuronal.ipynb)
