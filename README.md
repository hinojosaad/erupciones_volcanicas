# Clasificación de erupciones volcánicas

Mi solución al reto propuesto por Nuwe en la página web https://nuwe.io/dev/challenges/jornada-talento-clasificacion-de-erupciones-volcanicas.

## Descripción del reto
El reto consiste en construir un modelo predictivo  de tipo __Random Forest__ a partir del conjunto de datos _jm_train_ que contiene las mediciones de las vibraciones de sensores detectadas en dias previos a una erupción volcánica. Dichas mediciones son clasificadas en las siguientes categorías de acuerdo al tipo de erupción:

* 0 Pliniana
* 1 Peleana
* 2 Vulcaniana
* 3 Hawaiana
* 4 Estromboliana

Adicionalente se proporciona el archivo _jm_test_ el con mediciones de vibraciones cuyo posible tipo de erupción desconoce. El objetivo del reto es predecir cuales son los valores de dicho archivo, utilizando como base el _jm_train_. El desempeño del modelo se evalua a través de la métrica __f1_macro__, es decir se considerará que un modelo es mejor si logró hacer una predicción con un __f1_macro__ mayor.


## Archivos del repositorio

* Erupciones_volcanicos.ipynb: Notebook describiendo el código en python con el cual se construyó la solución propuesta al reto
* space_X_pred.csv: Archivo que contiene las predicciones del modelo de __Random Forest__ con parametros ajustados para los valores contenidos en _jm_test_X


## Resultados
Se utilizó el modelo __RandomForestClassifier__ de la librería _sklearn_ combinado con un reescalado _RobustScaler_ obteniendo el siguiente desempeño antes y después de afinar parámetros

| **f1_macro** | **tuned f1_macro** |
|--------------|--------------------|
|    .7682     |       .7774        |


## Requisitos

matplotlib==3.5.2
numpy==1.21.5
pandas==1.4.4
seaborn==0.11.2
sklearn==1.1.1
