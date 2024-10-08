# Toolbox Observational Constraint
This toolbox shows how to construct an observational constraint, from start to finish, based on an univariate example applied to the global temperature.
This example shows how to import climate models data and observations, how to construct the variable to be constrained and the variable to constrain, and how to build and represents the observational constraint.



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
The linear observational constrain is applied and illustrated in the notebook "Part3_observational_constrain.ipynb".


