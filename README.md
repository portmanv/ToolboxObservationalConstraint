# Toolbox Observational Constraint
This toolbox shows how to construct an observational constraint, from start to finish, based on an univariate example.
It shows how to import climate models data and observations, how to construct the variable to be constrained and the variable to constrain.

An example of univariate observational constraint, applied to the global temperature.




![im](https://github.com/user-attachments/assets/a8fdfc8d-945b-4a05-8ba3-65b146f50f17)


# Installation 
The needed packages may have conflictual versions. We recommand the use of a virtual environment where the packages versions are fixed. We proposes this procedure:
- Install anaconda https://docs.anaconda.com/anaconda/install/
- Open Anaconda Navigator
- Go to the tab "Environments". Create a new environment named for example toolbox. In this step I have chosen python version 3.9.19.
- Go to the tab "Home". Make sure you use the new environment created, "toolbox", indicated on the top. Click on "Install" on Jupyter Notebook.
- Click on "Launch" on Jupyter Notebook. A tab should open on your browser. Open the "ToolboxObservationalConstraint" file, go to /notebook
- Open and run "Part1_install_packages.ipynb" to install automatically all needed packages.


# Definition of the variables
Observational constrained enables to constrain the distribution of a future variable $X$, by using the observation of a given variable $X$. It is thus necessary to define $X$, $Y$, and import the $X$ and $Y$ values of climate models and the $X$ value observed.

The notebook "Part2_define_X_and_Y.ipynb" imports and computes the $X$ and $Y$ values associated to different CMIP6 climate models, and the $X$ value observed from HadCRUT5.
In this example, $X$ is the global temperature averaged between 2015 and 2023. $Y$ is the global temperature averaged between 2091 and 2100.

# Constrain the distribution of $Y$
The linear observational constrain is applied in the notebook "Part3_observational_constrain.ipynb".

As describe in the article, the unconstrained distribution expectation and variance are $\mu_{Y}$ and $\Sigma_{Y}$.

The constrained distribution expectation and variance are:

$$\mathbb{E}[Y|X_0=x_0] = \mu_Y+ \Sigma_{YX} (\Sigma_{X} + \Sigma_{N})^{-1}(x_0-\mu_X)$$

$$\mathbb{V}(Y|X_0) = \Sigma_{Y} - \Sigma_{YX} (\Sigma_{X} + \Sigma_{N})^{-1} \Sigma_{XY}$$

The parameters $\mu_{X}$, $\Sigma_{X}$, $\mu_{Y}$, $\Sigma_{Y}$ and $\Sigma_{XY}$ are estimated on climate models. The observational uncertainty, of variance $\Sigma_{N}$, is estimated as the covariance matrix of the HadCRUT5 ensemble.

![distributions](https://github.com/user-attachments/assets/ccefdadd-1e83-4ef5-b294-e56f4a3f8385)

In this example, the multi-model mean $\mu_X$ is close to the observation $x_0$. Consequently, the unconstrained and constrained expectations are very similar, as describes the equation:

$$\mathbb{E}[Y|X_0=x_0] = \mu_Y+ \Sigma_{YX} (\Sigma_{X} + \Sigma_{N})^{-1}(x_0-\mu_X)$$


The constrained variance is lower than the unconstrained variance, as there is a strong link between $X$ and $Y$, and a small observational uncertainty $\Sigma_{N}$, as describes the equation:

$$\mathbb{V}(Y|X_0) = \Sigma_{Y} - \Sigma_{YX} (\Sigma_{X} + \Sigma_{N})^{-1} \Sigma_{XY}$$


