## Setup
To run the code on a local or remote machine, you can follow the recommendation below.
We use `pip` and `venv`, which are the default Python environment management system and are effective for that purpose.
### Prerequisite
* The code was tested using `Python` 3.10.9, and the environment was set up using `pip` and `venv` (rather than `conda`). I use `vscode` as the IDE.
* Make sure you have a compatible version of Python (3.7.x-3.10.x) and the necessary tools `pip` and `git` installed. You can check if they are installed and see their versions by running `python --version`, `pip --version` (or `pip3 --version`), and `git --version` in the command line. If any of these are missing, please install them according to the official guides: [python](https://www.python.org/downloads/), [pip](https://pip.pypa.io/en/stable/installation/) and [git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
### Setup Steps
1. To get a local copy of this repository, run `git clone https://github.com/mahmudnahid/Tuberculosis-Detection-From-X-Ray-Images.git` in the command line. This will create a new sub-folder with a local copy of the repository. Note that if you encounter any issues during the setup process below, you can delete this folder and start fresh by cloning again. The changes made during the setup should only affect files within this folder, so deleting it will give you a clean slate to work from. If there are any issues with the set up, make sure to have a look at the notes below.
2. The goal of the setup process is to create a virtual environment and install necessary packages for running the notebooks. The required packages as defined in the `requirements_xray_clsf.txt` file will be installed in the environment. There are two ways to accomplish this, so you can choose the method that works best for you:
    1. **Semi-automatically using the `setup.py` script**: From the repository root folder, run `python ./setup/setup.py`. This should complete all required steps for you. If you get no error, the setup should be completed, and you could verify it by testing it as described below. This script was tested on Windows 10, but not Mac and Ubuntu (although it is likely to work). If it does not work and you are unable to quickly debug the issue, simply delete the folder, go back to step 1, and try the manual version instead. Deleting the folder will revert any changes made. It may also be helpful to spend a few minutes reviewing `setup.py` to see how it implements the manual steps below.
    2. **Manually** - following the steps below in the command line:
        1. Create a subfolder named `venv` within the local repository folder, i.e. by `mkdir venv`
        2. `cd` into `venv` and initialize two environments by running:
            * `python -m venv xray_clsf`
        3. `cd` out back to the repository root folder, and activate the virtual environment by running:
            * Linux or Mac: `source ./venv/xray_clsf/bin/activate` 
            * Windows CMD: `.\venv\xray_clsf\Scripts\activate.bat`
            * Windows Powershell: `.\venv\xray_clsf\Scripts\Activate.ps1`
         4. Install the packages: `pip install -r requirements_xray_clsf.txt`
         5. Install `ipykernel`: `python -m ipykernel install --user --name=xray_clsf --display-name=xray_clsf`
         6. Deactivate the environment by: `deactivate`

### Setting Up `vscode` to work with Notebooks and Virtual Environments
* `vscode` needs to be restarted after setting up the virtual environments for the first time. Otherwise, the environments will not be visible in `vscode`.
* To run Python notebooks in `vscode`, you first need to install the `Python` extension by Microsoft (done via the Extensions menu on the left sidebar).
* Then, open a notebook and set the right kernel(`xray_clsf`). Setting the kernel is done on the top right side in `vscode`. 
* Note that if you see wiggly orange lines below the package names in the import statement, change the interpreter to that of the virtual environment by typing in the command-palette `Python: Select Interpreter` ([stackoverflow](https://stackoverflow.com/a/72721797/10006823)).

### Testing the Setup
To make sure that the environment, and the `vscode` integration were all set up correctly - open the file `setup/test_setup.ipynb`, set the right kernel(`xray_clsf`), and run. If you get a `succeeded` message - these modules are working fine. 