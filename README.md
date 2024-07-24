# Toolbox_Observational_Constraint
An example of univariate observational constraint, applied to the global temperature.




![im](https://github.com/user-attachments/assets/a8fdfc8d-945b-4a05-8ba3-65b146f50f17)


# Installation 
The needed packages may have conflicual versions. We recommand the use of a virtual environment where the packages versions are fixed. We proposes this procedure:
- Install anaconda https://docs.anaconda.com/anaconda/install/
- Open anaconda Navigator
- Go to the tab "Environments". Create a new environment named for example toolbox. In this step I chose python version 3.9.19.
- Go to the tab "Home". Make sure you use "toolbox", indicated on the top. Click on "Install" on Jupyter Notebook.
- Click on "Launch" on Jupyter Notebook. A tab should open on your browser. Open the "ToolboxObservationalConstraint" file, go to /notebook
- Open and run "Part1_install_packages.ipynb" to install automatically all needed packages.


# Definition of the variables
Observational constrained enables to constrain the distribution of a future variable Y, by using the observation of a given variable X. It is thus necessary to define X, Y, and import the X and Y values of climate models and the X value observed.

The notebook "Part2_define_X_and_Y.ipynb" imports and computes the X and Y values associated to different climate models.
In this example, X is the global temperature averaged between 1851 and 2014. Y is the global temperature averaged between 2091 and 2100.
