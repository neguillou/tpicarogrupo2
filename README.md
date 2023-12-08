# Trabajo Práctico ICARO: Desarrollo de un Modelo de Recomendación

Este repositorio contiene el código y los recursos utilizados para desarrollar un modelo de recomendación utilizando la biblioteca LightFM y medir varias métricas de evaluación.

## Objetivo

El objetivo principal de este trabajo práctico es implementar LightFM para desarrollar un sistema de recomendación. Se busca evaluar la efectividad del modelo en la tarea de recomendar 20 animes a usuarios de la plataforma myanimelist.net

## Contenido del Repositorio

### Archivos Principales

- 'TP\_Recommender\_System\_EDA\_.ipynb': Notebook de Jupyter que contiene una exploración de los datasets que utilizamos para el sistema de recomendación.

- 'Recommender\_System\_LightFM.ipynb': Notebook que contiene el código de implementación del modelo de recomendación utilizando LightFM.

- 'Gridsearch\_LightFM.ipynb': Notebook que contiene la búsqueda de los mejores hiperparámetros para nuestro modelo de recomendación.

- 'Matrices\_Train\_Test\_pickle.ipynb': Notebook que contiene la división en conjuntos de entrenamiento y prueba, su factorización de matrices, y la serialización de estos objetos a través de pickle.

- 'Recomendaciones.csv': Dataset que contiene las recomendaciones de 20 animes (anime\_id) para cada usuario (user\_id).

### Recursos (agregar carpeta de drive donde se encuentren los recursos)

- 'rating\_complete\_filtrado.csv': Dataset obtenido a partir del filtrado del dataset original 'rating\_complete.csv', considerando solo los casos de usuarios que hayan puesto puntaje a más de 150 animes. Esto se hizo con el objetivo de reducir la dimensionalidad.

- 'matriz\_interacciones.pickle': Archivo que contiene la serialización de la matriz de interacciones para el conjunto de entrenamiento.

- 'matriz\_interacciones\_test': Archivo que contiene la serialización de la matriz de interacciones para el conjunto de prueba.

## Descripción del Proyecto

### Pasos Principales

1. **Preprocesamiento de Datos:** Se filtraron los datos para reducir su dimensionalidad, posteriormente se dividieron en un conjunto de entrenamiento y uno de prueba, para ajustar y evaluar el rendimiento del modelo de recomendación. Se serializaron las matrices para poder trabajar de forma segmentada.

1. **Entrenamiento del Modelo:** Se implementó y entrenó el modelo de recomendación utilizando LightFM, ajustando los hiperparámetros utilizando GridSearchCV, para obtener un buen rendimiento.

1. **Evaluación del Modelo:** Se midieron dos métricas, Precision at K y MAP, para evaluar la efectividad del modelo en la tarea de recomendación.

### Métricas de Evaluación

- **Precision at K:** Mide la proporción de elementos relevantes en las primeras K recomendaciones.

- **MAP(Mean Average Precision):** Promedia la precisión en la lista de recomendaciones para todos los usuarios, ofreciendo una visión general de la efectividad del sistema.

## Instrucciones de Uso

1. Clonar este repositorio:

\```bash

git clone https://github.com/neguillou/tpicarogrupo2.git
