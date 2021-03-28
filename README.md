# Team SAA Watercolor Pomology Data Science Project Repository

This repository is a collection of Jupyter notebooks that serve as the ETL process for the SENG 5709 Data Science group project. 

# Installation/Running instructions

This implementation was done in Python3 on iPython notebooks running in a Jupyter environment. Please consult the [Jupyter Lab Documentiaton](https://jupyterlab.readthedocs.io/en/stable/getting_started/installation.html) for instructions on how to install a Jupyter server onto your local machine.

The server can be ran by running `jupyter lab` in your terminal window.

#### Kernel installation

Once the Jupyter server has been installed on your machine, you will need to create a virtual environment driven kernel to act as an interpreter for the project’s code.

#### Virtual Environment Creation

Abridge instructions derived from: https://janakiev.com/blog/jupyter-virtual-envs/

From hereon out, the following instructions assume you are operating within the directory where you cloned this repository.

##### Create a virtual environment 

`python3 -m venv <venvName>`

##### Start the virutal environment 

`source <venName>/bin/activate`

##### Install package-level dependencies

`pip install -r requirements.txt`

Add the virtual environment to Jupyter:

`python3 -m ipykernel install --user --name <venvName> --display-name “display name you want for the venv”`

You can ensure that the kernel has been installed to your jupyter lab by running `jupyter kernelspec list`