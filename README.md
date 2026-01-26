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

### Exercise 1
For this specific part of the lab, a simple linear regression model was implemented to model the relationship between stellar mass and luminosity using a single input feature. The model assumes a linear relationship of the form:

$$
\hat{L} = wM + b
$$

where \(M\) represents the stellar mass, \(w\) is the weight parameter, and \(b\) is the bias term.

To quantify how well the model fits the data, the Mean Squared Error (MSE) was used as the loss function:

$$
J(w, b) = \frac{1}{2m} \sum_{i=1}^{m} (\hat{L}^{(i)} - L^{(i)})^2
$$

Analytical gradients of the cost function with respect to \(w\) and \(b\) were derived and used to optimize the model parameters. Gradient descent was implemented in both non-vectorized and vectorized forms to compare efficiency and clarity.

Several learning rates were tested to study their impact on convergence behavior. Additionally, the cost surface was visualized to better understand the optimization landscape.

From this analysis, it was observed that the linear model captures the general trend of the data but underfits for larger stellar masses. The cost surface shows a clear convex shape with a single global minimum, and the experiments highlight how sensitive convergence is to the choice of learning rate.

#### Results
This notebook implements linear regression from scratch to model stellar luminosity as a function of stellar mass. It covers dataset visualization, model definition, MSE loss, gradient computation, and both iterative and vectorized gradient descent. To see the notebook check the following link:

[Open Notebook 1](01_part1_linreg_1feature.ipynb)

---
### Exercise 2
In the second part of the lab, the model was extended to capture more complex relationships by introducing additional features and nonlinear terms. Three different feature sets were evaluated:

- **M1:** \( [M, T] \)
- **M2:** \( [M, T, M^2] \)
- **M3:** \( [M, T, M^2, M \cdot T] \)

The full polynomial model (M3) is defined as:

$$
\hat{L} = w_1 M + w_2 T + w_3 M^2 + w_4 (M \cdot T) + b
$$

This model includes both quadratic and interaction terms, allowing it to represent nonlinear dependencies between stellar properties.

All models were trained using fully vectorized gradient descent. Feature standardization was applied prior to training to ensure numerical stability and improve convergence. Training progress was evaluated using cost-versus-iteration plots.

The results show that each additional nonlinear feature leads to a reduction in the final loss. The full polynomial model achieved the lowest cost, demonstrating the importance of higher-order terms and feature interactions in accurately modeling stellar luminosity.

#### Results
This notebook models nonlinear and interaction effects using polynomial features of mass and temperature. It implements vectorized gradient descent, compares models with different feature sets, evaluates the importance of the interaction term, and demonstrates prediction for a new star. To see the notebook check the following link:

[Open Notebook 2](02_part2_polyreg.ipynb)

---
### AWS SageMaker Execution Evidence
The main goal of this section is to upload both of the Jupyter Notebooks we already created to the AWS SageMaker domain that was stablished in class. In order to do the so, we'll use the Code Editor environment following these steps:

1. Open AWS Academy and look for the lab created by the teacher. Once it has been located, start the lab and access AWS.
2. Inside AWS use the search bar in order to find SageMaker Studio (Select the one that says AI). After that select the option Domains in the side bar and click the Open Studio button so you can access SageMaker; if done correctly, you''l see the next page:
![alt text](Images/First.png)

3. Inside SageMaker click the Code Editor App and create a new space.
![alt text](Images/Second.png)

4. Later on, when the Code Editor space is created, click the run button and wait for it to start.
![alt text](Images/Third.png)

5. Once the space is running, select the Open Code Editor option, so you can access the environment in which the Jupyter Notebooks will be uploaded. At first, it will take a while for the Code Editor to open in the new tab, but at the end you'll see the next page:
![alt text](Images/Fourth.png)

6. Inside the editor, the resemblance with Visual Studio Code will help in the following steps. Select the Open Folder option and select ``/home/sagemaker-user``folder so you can start uploading the files.

7. After the folder is open, drag both Jupyter Notebooks to the side bar.
![alt text](Images/Fifth.png)

8. Then, choose the Select Kernel button so you can create a Virtual Environment to run the ``.ipynb``files. In this case, select the option that is recommended by the Code Editor.
![alt text](Images/Sixth.png)

9. When the Kernel is selected, click the Run All button in both Notebooks to execute all code cells.
![alt text](Images/Seventh.png)

10. After the exectution is complete, verify that there's no error in any of the cells. If there's no error, then the process was completed successfuly. As the Lab requires here is the evidence of two plots, one for each notebook.
![alt text](Images/Ninth.png)
![alt text](Images/Eight.png)

11. Later, save the changes made an close the Code Editor tab so you can return to SageMaker and stop the CodeEditor space environment. After checking that the space has stopped running, you cna close the SageMaker tab and log out from AWS.
![alt text](Images/Eleven.png)

12. Return to the AWS Academy tab and stop the lab.
![alt text](Images/Twelve.png)

13. Finally, you can Log Out from AWS Acadamy and close all tabs.

**Local Execution vs AWS Execution**

The notebooks executed successfully in both local and AWS SageMaker environments with identical results and visual outputs. No code changes were required. The only difference observed was slightly longer execution time in SageMaker due to the cloud-based execution environment.

---
### Conclusion
This lab explored regression modeling by starting with a simple linear relationship between stellar mass and luminosity and then extending it using polynomial and interaction features. Implementing the loss function, gradients, and gradient descent from scratch helped clarify how optimization behaves and how learning rate choices affect convergence. Visualizing the cost surface and training curves provided intuition about model stability and minima. While the linear model captured the overall trend, it showed clear limitations at higher masses. Introducing nonlinear and interaction terms improved the model’s ability to represent the data and reduced the final loss. Overall, the lab highlighted the importance of feature design, careful experimentation, and interpretation when building regression models.


