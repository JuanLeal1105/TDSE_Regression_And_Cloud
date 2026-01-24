# TDSE_Regression_And_Cloud

**Elaborado por**
  
Juan Carlos Leal Cruz 

## Descripción del Laboratorio
El presente laboratorio modela la luminosidad estelar usando regresión lineal y polinómica implementada desde cero, sin liberías de machiene learning. El objetivo principal es entender cómo se definen la función de hipótesis, la función de pérdida y el proceso de optimización, aplicando todos estos conceptos a un conjunto de datos de luminosidad estelar.

El proyecto forma parte de un bootcamp de Machine Learning con énfasis en el aprendizaje de los fundamentos de los modelos y su ejecución en entornos cloud y empresariales.

### Prerrequisitos

Para la ejecuión de este laboratorio es nececesario contar con:

- Python 3.8 o superior
- Jupyter Notebook o JupyterLab
- Las siguientes librerías de Python:
  - ``numpy``
  - ``matplotlib``
 
### Ejecución
Para la ejecución del presente laboratorio se plantea el siguiente orden de ejecución para:

1. Clonar el repositorio e ingresar a la carpeta
   ```
   git clone <URL_del_repositorio>
   cd <nombre_del_repositorio>
   ```

2. Preparar el entorno virtual

___

### Ejercicio 1
En este ejercicio se implementa la regresión lineal desde cero para poder modelar la luminosidad estelar en función de la masa. Se define de forma explícita el modelo junto con la función de pérdida (MSE) y los gradientes. El objetivo es entrear el modelo mediante el descenso por gradiente tanto de forma iterativa como vectorizada; por otro lado se anliza la superficia de costo, la convergencia del algoritmo y las limitaciones de un modelo lineal para el conjunto de datos dado.


### Ejercicio 2
En este ejercicio se extiende el modelo anterior incorporando ingeniería de caracteríasticas polinómicas e interacciones entre variables. Se contruyen distintos modelos con combinaciones tanto de masa como de temperatura y se entrenan mediante descenso por gradiente vectorizado, comparando en términos de pérdida y capacidad predictiva. También se analiza la importancia del término de interacción y se realiza una predicción para un nuevo dato de entrada.


### AWS SageMaker Execution Evidence
