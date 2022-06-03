# ProyectoFinalIA_Agro
Este repositorio contiene los archivos necesarios para implementar en JupyterNotebook o Collab, Spyder o Python IDE la estimación de la variable pH usando un conjunto de datos de espectroscopía VIS/NIR mediante métodos de aprendizaje de máquina.
# Introducción
Julián Oviedo (yo) y Andrés Camilo Ángel, realizamos la implementación de los modelos de inteligencia artificial para la estimación de la variable pH. Empleando el conjunto de Datos NIRSdata que contiene caracteristicas de entrada dadas por la abosrbancia del espectro VIS/NIR de muestras de suelo analizadas en el laboratorio de análisis de suelo de Agrosavia obtenemos: 
 - 19 Caracteristicas que comprenden el rango de 451 a 604 nm con espaciado de 8,5 nm  entre muestra y muestra.
 -  La etiqueta a predecir será pH, la que previamente se ha validado mediante pruebas quimiometricas en laboratorio.

# ¿Qúe hicimos?

Usando Python y sus librerias como ScikitLearn, Matplotlib y Pandas, realizamos el preprocesamiento del conjunto de datos pasando de 6178 a 3285 muestras, puesto que se contaban con 2893 muestras con valores NAN en el etiquetado, esto por trazabilidad (comentado por Agrosavia). Posterior, se realiza una regularización de los datos con el objetivo de mejorar el procesamiento usando técnicas como: 
Regresión Lineal Múltiple
Regresión de Soporte Vectorial
Perceptrón Multicapa

# ¿Qué se obtuvo?

Una vez se implementan los modelos con las técnicas nombradas obtenemos las siguientes métricas y gráficas:

![image](https://user-images.githubusercontent.com/47205790/171812137-0fd0c5e8-f3d9-491e-8455-8ee8b106bc74.png)

