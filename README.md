# ProyectoFinalIA_Agro ![image](https://user-images.githubusercontent.com/47205790/171818497-97b03c0f-3a4e-40bc-b5eb-5fe30736b395.png)

Este repositorio contiene los archivos necesarios para implementar en JupyterNotebook o Collab, Spyder o Python IDE la estimación de la variable pH usando un conjunto de datos de espectroscopía VIS/NIR mediante métodos de aprendizaje de máquina.

![image](https://user-images.githubusercontent.com/47205790/171818519-2ab76fb4-1712-407c-8df6-96bc4580ea84.png)

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
<p align="center">

![image](https://user-images.githubusercontent.com/47205790/171812137-0fd0c5e8-f3d9-491e-8455-8ee8b106bc74.png)

 
![image](https://user-images.githubusercontent.com/47205790/171816392-97e37a11-f227-4618-91d6-74808a97cbc1.png)
 </p>
# Conclusion

Los métodos implementados por las métricas obtenidas nos permiten concluir que a pesar de que para SVR se aplicó una optimización de hiperparámetros por GridSearchCV no se obtuvieron buenos resultados con estos regresores. Se analizó el sobre entrenamiento que sufre el modelo al repetirlo, sin embargo, las funciones de pérdida nos indican con un valor significativo que el modelo no se comporta de manera correcta, en ninguna de las técnica aplicadas, en especial en el perceptrón multicapa, asi que como continuidad a este proyecto recomendamos hacer una optimización de los parámetros, usar una red neuronal más robusta y además usar validación cruzada en este método para obtener un mejor análisis. 
Cabe resaltar y anotar que los parámetros y base de análisis parte del uso de la herramienta Regression Learner APP de Matlab en su paquete de Aprendizaje Autómatico, que nos permitió de manera automática determinar algunos de los parámetros y obtener una visión del problema, tanto visual como con las métricas, además basados en el estado del arte [1] se decide probar con estas tres técnicas.

# Referencia
1]	D. A. Delgadillo-Duran, C. A. Vargas-García, V. M. Varón-Ramírez, F. Calderón, A. C. Montenegro, and P. H. Reyes-Herrera, “Using vis-NIRS and Machine Learning methods to diagnose sugarcane soil chemical properties,” Dec. 2020, Accessed: Feb. 23, 2022. [Online]. Available: https://arxiv.org/abs/2012.12995v3
![image](https://user-images.githubusercontent.com/47205790/171818435-9d026a0b-b80e-4605-976c-6727aeba9ef5.png)





