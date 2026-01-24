# TDSE_Regression_And_Cloud

**Created by**
Juan Carlos Leal Cruz 

## Laboratory Description
This laboratory focuses on modeling stellar luminosity using linear and polynomial regression implemented from scratch, without relying on machine learning libraries. The main goal is to understand how the hypothesis function, the loss function, and the optimization process are defined, applying all these concepts to a dataset of stellar luminosities.

This project is part of a Machine Learning bootcamp, with an emphasis on learning the fundamentals of models and their execution in cloud and enterprise environments.

### Prerequisites

To run this laboratory you will need:

- Python 3.8 or higher (As a recomendation, the newer versions are better due to the compatibility with the creations of virtual environments in multiple IDEs)
- Jupyter Notebook or JupyterLab
- The following Python libraries:
  - ``numpy``
  - ``matplotlib``
 
### Execution
To run this laboratory, follow the steps below:

1. Clone the repository and navigate to the folder:
   ```
   git clone <Repository_URL>
   cd <Repository_name>
   ```

2. Setup the virtual environment
   ```
   python -m venv venv
   source venv/bin/activate       # On Linux/Mac
   venv\Scripts\activate          # On Windows
   ```
   
3. Start running each block of code so you can see the results
___

### Ejercicio 1
This notebook implements linear regression from scratch to model stellar luminosity as a function of stellar mass. It covers dataset visualization, model definition, MSE loss, gradient computation, and both iterative and vectorized gradient descent.


### Ejercicio 2
This notebook models nonlinear and interaction effects using polynomial features of mass and temperature. It implements vectorized gradient descent, compares models with different feature sets, evaluates the importance of the interaction term, and demonstrates prediction for a new star.


### AWS SageMaker Execution Evidence
