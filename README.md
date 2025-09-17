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

### Manual Installation of WSL (Windows only)
If you have run out of storage on your C:\ drive, WSL installation will fail. To install WSL on another drive, first find the Ubuntu 24.04 link on [this page](https://learn.microsoft.com/en-us/windows/wsl/install-manual#downloading-distributions) and copy the link to download the distribution, which should look something like `https://aka.ms/wslubuntu`. Move it to a space on your preferred drive. Then run Powershell as an administrator (right click -> 'run as administrator') and type the following commands: 
`Set-Location D:` 
   - This sets the current working directory (cwd) to the D: drive. If you want to use a different drive, replace the `D:` with the name of that drive.
`New-Item WSL -Type Directory`
   - This creates a folder to store our new WSL installation in.
`Set-Location .\WSL`
   - This moves our cwd to our new folder.
`curl -L -o Linux.appx <distribution_url>`
   - This will download the distribution from the link that we found earlier, and put it in a file called `Linux.appx`.
`Copy-Item .\Linux.appx .\Linux.zip`
   - Makes a backup copy of our linux distribution.
`Expand-Archive .\Linux.zip`
   - Extracts our Linux distribution so that we can use the files in it.
`Get-Childitem -Filter *.exe`
   - Looks for an executable file that we can use to run WSL from.
Once you have found the executable, which should be called `ubuntu.exe`, run it (by typing `ubuntu.exe` into either Powershell or cmd) and you should have a working terminal where you can type commands.
It might be the case that `Get-Childitem -Filter *.exe` does not return any results. If this happens, set your cwd to the new `Linux` folder:
`Set-Location Linux`
Then look for an `appx`-extension file:
`Get-Childitem -Filter *.appx`
Then rename it to `.zip` so that we can extract it:
`ren .\Ubuntu_2404.x.x.xx.appx .\Ubuntu_2404.zip`
Extract the new file:
`Expand-Archive .\Ubuntu_2404.zip`
Set cwd to the new folder:
`Set-Location .\Ubuntu_2404`
Now we should be able to see the executable:
`Get-Childitem -Filter *.exe`
And then we can run it:
`ubuntu.exe`
  
## Google Colab
It is recommended that you at least attempt to install Python and the packages locally. If all attempts fail, you may fall back on Google Colab as a working environment.

Setting up - Simply run the `GettingStarted.ipynb` on [this link](https://colab.research.google.com/github/SymbolicModel/GettingStarted/blob/main/GettingStarted.ipynb).
