# Primer modelo de Machine Learning. :rocket:

En este proyecto se entrena el primer modelo de machine learning realizado por mi.

La tarea es desarrollar un modelo que pueda analizar el comportamiento de los clientes y recomendar uno de los nuevos planes de Megaline: Smart o Ultra. Megaline es una empresa de telefonía móvil que no está satisfecha al ver que muchos de sus clientes utilizan planes heredados.

El dataset tiene los siguientes registros de los clientes:
* сalls — número de llamadas,
* minutes — duración total de la llamada en minutos,
* messages — número de mensajes de texto,
* mb_used — Tráfico de Internet utilizado en MB,
* is_ultra — plan para el mes actual (Ultra - 1, Smart - 0).

## Objetivo
El objetivo es poder predecir si un cliente puede cambiar su plan de smart a ultra (plan más caro). Al ver que se tiene una columna que nos dice el tipo de plan actual del cliente. La tarea se convierte en una tarea de clasificación binaria.

Sabiendo lo anterior, la columna `'is_ultra'` se convierte en el objetivo y las demás columnas serán nuestras características.

Se ha solicitado que el modelo tenga un umbral de exactitud mayor a 0.75.

## Desarrollo del proyecto
Al ser un proyecto educativo para iniciar a prácticar machine learning, los datos ya se encuentran procesados para su manejo. Por lo que no hay un preprocesamiento de datos.

### Segmentación de los datos
Los datos fuente son segmentados en un conjunto de entrenamiento, uno de validación y uno de prueba. Estos a su son segmentados en caracaterísticas y objetivo usando el módulo `train_test_split` de la librería `sklearn.model_selection`.

### Entrenamiento del modelo
Para esto se han entrenado 3 diferentes modelos:
1. Árdol de decisión
2. Bosque aleatorio
3. Regresión logística

Todos de la librería `sklearn`. Y a todos se les modificaron los hiperparámetros. Así se seleccionó el mejor modelo con los mejores hiperparámetros.

## Conclusiones
El modelo de bosque aleatorio fue el que tuvo el umbral más cercano a 0.75. El conjunto de prueba fue evaluado con este modelo obteniendo una exactitud de 0.77.

Finalmente se evaluó una prueba de cordura cuyo resultado de exatitud fue de  0.69, con esto podemos decir que nuestro modelo cumplió con lo esperado.