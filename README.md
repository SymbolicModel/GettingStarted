# GettingStarted
Setting up PySR and PySINDy environment for the Symbolic Model Discovery workshop.

## On your local machine: Linux/Mac
If you're confident with Python and setting up virtual environment, set a virtual environment up and run `GettingStarted.ipynb` in the virtual environment. 

If you're not familiar with setting up virtual environment, follow the procedure below using VS Code.

0. (Install Python - Recommended version: 3.13.x )
Most Linux distro and Mac has python pre-installed - skip this step.

1. Install [VS Code](https://code.visualstudio.com/Download).
We use Visual Studio Code to guide you through the installation process.

2. Go to `Extensions` (4th/5th/6th button on the left toolbar) and install `Python`, `Python Environments` and `Jupyter` extensions.

3. Download (or git clone) this repo and change directory to this folder

4. Open `GettingStarted.ipynb` in VS Code.

5. On the top right corner, select "Select Kernel", and follow the dropdown menu to "Python Environments...--> Create Python Environment --> venv --> Python 3.xx.xx" to create a local Python Environment.

6. Run the first cell of `GettingStarted.ipynb` to install the necessary packages.
- Note that for `PySR`, a JULIA backend will be installed automatically only upon first import. Follow through the rest of teh notebook to finish the install.

7. Run the rest of the notebook to finish the install and test the installation.

## On your local machine: Windows
(To appear)

## Google Colab
It is recommended that you at least attempt to install Python and the packages locally. If all attempts fail, you may fall back on Google Colab as a working environment.

Setting up - Simply run the `GettingStarted.ipynb`.
