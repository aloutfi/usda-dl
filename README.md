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



##### Please consult the [Jupyter Lab Documentation](https://jupyterlab.readthedocs.io/en/stable/user/interface.html) for instructions on how to navigate the Jupyter Lab interface.

# Project Questions:

![BQs taken from phase 2](https://i.imgur.com/mfPhi8I.png)

# Repository structure overview

```

├── APS_Varieties.ipynb <- Varieties scraped from American Pomological Soceity Registrar
|
├── UMN_Apples.ipynb <- Names of UMN Apples Scraped from UMN's website
|
├── cultivar_creation.ipynb <- Creation of mapping between cultivar and common name
|
├── cultivar_mapping.ipynb <- Used for M1. Mapping of result from cultivar_creation.ipynb to pomo dataset.
|
├── data
│	├── USA_2019_Fruit_Totals.csv <- Pulled from https://www.ers.usda.gov/data-products/fruit-and-tree-nuts-data/fruit-and-tree-nuts-yearbook-tables
│  	├── cultivar-pomo-usda.csv <- Output of usda-recognized.ipynb
|
│  	├── cultivar-pomo.csv <- Output of cultivar_mapping.ipynb
|
│  	├── final.csv <- Output of final_df.ipynb
|
│  	├── polity_cultivar_pomo_usda.csv <- Output of polity_export_mapping.ipynb
|
│  	├── usda.csv <- Retrieved from https://plants.sc.egov.usda.gov/Data/plantlst.txt
|
│  	└── usda_pomological.csv <- Output of usda-pomo.ipynb.
|
├── dl.py <- Original script that the project was inspired from.
|
├── final_df.ipynb <- Final formatting of cultivar-pomo-usda.csv for elasticsearch upload
|
├── ingestion_and_upload.ipynb <- Upload to elastic search
|
├── is_usda.ipynb <- Preview usda txt file returned
|
├── null_value_analysis.ipynb <- Used for E5. Validates elasticsearch query for per column NVA.
|
├── polity_export_mapping.ipynb <- Used for H1. Probably the best documented notebook here.
|
├── requirements.txt
|
├── usda-pomo.ipynb <- dl.py modified into a quick and dirty python notebook to pull pomo dataset metadata.
|
└── usda-recognized.ipynb <- Used for M4. Determines USDA recognized via Scientific Name.
```



