# Alex's QGSS 22 Lab Work

These are the submissions I produced when attending the Qiskit Global Summer School in 2022.
They have been reworked to function with Qiskit v1.0+ since much of the original code used deprecated libraries.

### Run locally

Pre-requisites:

- [IBM Quantum account](https://quantum.ibm.com/)
- [Python](https://www.python.org/) (3.10 or later) environment with
    - Classic [Jupyter Notebook](https://jupyter.readthedocs.io/en/latest/install/notebook-classic.html) interface or [JupyterLab](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html)

1. Follow the Qiskit installing guide at: [Install Qiskit](https://docs.quantum.ibm.com/guides/install-qiskit)<br>
    For Mac/Linux users:
    - Create your virtual environment: `python3 -m venv qiskit_env`
    - Activate your new environment: `source qiskit_env/bin/activate`
    <br>

    For Windows users:<br>
    - If using Powershell, you may need to run it as administrator and run the following: `Set-ExecutionPolicy Unrestricted -Force`
    - Create your virtual environment: `python3 -m venv .\qiskit_env`
    - Activate your new environment: `.\qiskit_env\Scripts\Activate.ps1`

2. Install the pinned pip dependencies: `pip install -r requirements.txt`
