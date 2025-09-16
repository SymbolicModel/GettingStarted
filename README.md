# GettingStarted
Setting up PySR and PySINDy environment for the Symbolic Model Discovery workshop.

## On your local machine: Linux/Mac
If you're confident with Python and setting up virtual environment, set a virtual environment up and run `GettingStarted.ipynb` in the virtual environment. 

If you're not familiar with setting up virtual environment, follow the procedure below using VS Code.

0. (Install Python - Recommended version: 3.13.x )
   Most Linux distro and Mac has python pre-installed. You may skip this step if your Python version is 3.11+

1. Install [VS Code](https://code.visualstudio.com/Download) and open it.
    We use Visual Studio Code to guide you through the rest of the installation process.

2. Go to `Extensions` (4th/5th/6th button on the left toolbar) and install `Python`, `Python Environments` and `Jupyter` extensions.

3. Clone this repo and change directory to this folder.

   - For those using WSL or on Linux, the command is

     ```
     git clone https://github.com/SymbolicModel/GettingStarted.git
     cd GettingStarted
     ```

4. Open the `GettingStarted` folder in VS Code and open `GettingStarted.ipynb`.

5. On the top right corner, select "Select Kernel", and follow the drop-down menu to "Python Environments...--> Create Python Environment --> venv --> Python 3.xx.xx" to create a local Python Environment.

   - If you cannot find the "Python Environment" option, make sure you have `Python`, `Python Environments` and `Jupyter` extensions installed.

6. Run the first cell of `GettingStarted.ipynb` to install the necessary packages.

   - Note that for `PySR`, a JULIA backend will be installed automatically only upon first import. Follow through the rest of teh notebook to finish the install.


7. Run the rest of the notebook to finish the install and test the installation.

A successful run will have learning outputs from `PySR` and `PySINDy`. Compare the output with [the version on Github](GettingStarted.ipynb). 
## On your local machine: Windows
### Option 1: WSL (recommended)

1. Install [VS Code](https://code.visualstudio.com/Download) and the [WSL extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) in VS Code.
2. Install WSL
   - Open PowerShell in **administrator** mode by right-clicking and selecting "Run as administrator", enter the `wsl --install` command, then **restart your machine**.
   - Open PowerShell or Terminal (not in administrator mode) and type in `wsl --install Ubuntu-24.04`.
     - You will be prompt to create a user name and password for the Linux system.
3. Open a **WSL terminal window** (using the start menu and navigate to `Ubuntu` or by typing `wsl` from a command prompt / PowerShell).
4. Type `code` to open a VS Code. 
5. Follow the rest of the guide above for Linux, starting from step 2.

### Option 2: Run Python directly on Windows

This option will require that you know your way around installing Python properly on your Windows Machine, setting up a virtual environment and a Python Notebook environment. If you do, please make sure you have

- Python 3.11 or above (3.13 recommended)
- Set up a Jupyter Notebook environment, through VS Code or JupyterHub.
  - With Matplotlib support
- Set up a Python virtual environment and install the latest version of the following packages
  - numpy
  - scipy
  - pysr
  - pysindy
  - pandas
  - matplotlib


## FAQ / Troubleshoot
If your system is using a Python version older than 3.11, you may run into issues. In this case, consider the following options:

Linux/Mac:
- Install [PyEnv](https://github.com/pyenv/pyenv) following the procedure on the website to install a separate Python version (3.13.xx recommended).
- PyEnv may require build dependency to be installed first.
  - For linux, these dependency are usually installed with a single command on the package manager.
  - For Mac, you may need to first enable developer options (`xcode-select --install`) and install [homebrew](https://brew.sh).


Mac:
- Installing custom python version via [homebrew](https://docs.brew.sh/Homebrew-and-Python) directly is an alternative to [PyEnv](https://github.com/pyenv/pyenv) if you already have homebrew installed.
  

Windows (non-WSL):
- Download and install the latest [Python version 3.13](https://www.python.org/downloads/windows/) and retry.
  
## Google Colab
It is recommended that you at least attempt to install Python and the packages locally. If all attempts fail, you may fall back on Google Colab as a working environment.

Setting up - Simply run the `GettingStarted.ipynb` on [this link](https://colab.research.google.com/github/SymbolicModel/GettingStarted/blob/main/GettingStarted.ipynb).
