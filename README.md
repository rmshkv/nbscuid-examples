# nbscuid-examples 📓

## About

This repo contains an assortment of Jupyter Notebook collections built to be run with `nbscuid`. Some are in development and may not yet run properly.

## How to run (most) notebook collections in this repo

1. Clone this repo: 

        git clone https://github.com/rmshkv/nbscuid-examples.git 
        
    
2. `cd` into the directory of the collection you want to run. In this directory, install the environment specified by `environment.yml`: 

        conda env create -f environment.yml

    This will create an environment which has `nbscuid` installed, as well as the packages necessary to run the notebooks in the collection.

3. Activate the environment you just installed:
        
        conda activate [environment-name]
        
   (Note that the environment name is different for each collection).

4. Run 
            
        nbscuid-run config.yml 

    This will run all the notebooks specified in the collection's `config.yml` file. The executed notebooks get copied to a directory called `computed_notebooks/[some_folder]` created in the `run_dir` specified in `config.yml` (by default, the same directory that `config.yml` is in).

5. Next, run 

        nbscuid-build config.yml
        
     This will build the Jupyter Book based on the table of contents specified in the `config.yml` file, under Jupyter Book Table of Contents. The html files that make up the Jupyter Book will be created under `computed_notebooks/[some_folder]/_build/html`. If you want to publish this Jupyter book online, copy these html files to the location where you want to host them.

