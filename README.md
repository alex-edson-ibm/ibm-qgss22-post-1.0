# Alex's QGSS 22 Lab Work

These are the submissions I produced when attending the Qiskit Global Summer School in 2022.
They have been reworked to function with Qiskit v1.0+ since much of the original code used deprecated libraries.

### Run locally

Pre-requisites:

- [IBM Quantum account](https://quantum.ibm.com/)
- [Python](https://www.python.org/) (3.10 or later) environment with
    - Classic [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install/notebook-classic.html) interface or [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)

1. Install PyEnv - since different use cases for qiskit require certain versions of packages, it's good to be able to switch between different versions of Python and different versions of pip packages.<br>
    NOTE: you can just follow the [Qiskit installation guide](https://docs.quantum.ibm.com/guides/install-qiskit) if you only want to set up one Python version/environment.
    For Mac/Linux users:
    - Run the following commands:
    ```bash
    brew install pyenv
    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
    echo '[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
    echo 'eval "$(pyenv init -)"' >> ~/.zshrc
    ```
    - Restart your terminal
    <br>

    For Windows users:
    - See [https://github.com/pyenv-win/pyenv-win] for how to install the Windows port of PyEnv.
    - If using Powershell, you may need to run it as administrator and run the following: `Set-ExecutionPolicy Unrestricted -Force`

2. Install required Python versions and libraries - the qgss22-labs Jupyter notebooks work with Python v3.12.3 whereas the portfolio optimization example requires v3.8.18.<br>
    For Mac/Linux users:
    ```zsh
    pyenv install 3.12.7
    pyenv virtualenv 3.12.7 qgss22-labs
    pyenv install 3.8.18
    pyenv virtualenv 3.8.18 portfolio-optimization
    cd qgss22-labs
    pyenv local qgss22-labs
    pip install -r requirements.txt
    python -m ipykernel install --user --name=qgss22-labs
    cd ../portfolio-optimization
    pyenv local portfolio-optimization
    pip install -r requirements.txt
    python -m ipykernel install --user --name=portfolio-optimization
    ```
    You will now have Qiskit and the other tools required to run the lab notebooks.
