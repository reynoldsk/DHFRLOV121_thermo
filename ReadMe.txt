********************************************************************************
This directory contains the data and python notebooks necessary to reproduce the
analysis in:




Copyright (C) 2024
This collection of python notebooks is free software distributed under the BSD
3-clause license, please see the file LICENSE for details
********************************************************************************
This code is written in Python 3.8, and makes use of numpy (1.24.3),
matplotlib (3.7.2), pandas (2.0.3), scipy (1.9.3), scikit-learn (1.3.0),
biopython (1.78), ipywidgets (8.0.4), statsmodels (0.14.0), and seaborn (0.12.2). 
It has been tested on Windows 10 and mac OS14, but has no special dependencies
on hardware or OS. yml files are provided. 

It is presented as two Jupyter notebooks.
We suggest installing the Anaconda distribution of python for scientific computing as
one route to obtaining the necessary dependencies.

Once Anaconda has been installed, the Jupyter notebooks can be run following standard usage. Clicking 
through each cell will repeat the calculations and generate the figures in the main text of 
McCormick et al. Most notebooks are expected to run on the order of a few seconds on a standard laptop 
computer, however the energetics bootstrapping calculations in the "Thermal_kinetics_and_stability_analysis" 
notebook is expected to take about 15 minutes. The notebooks also allow these calculations to be skipped by 
loading in csv files, e.g. energetics_df_5-35C_5000boot.csv.


The code provides an analysis of our DHFR_asLOV2 thermal kinetics and CD spectroscopy data. 

Contents:

        .gitignore              specifies intentionally untracked files that git should ignore
                                (not track during commits)

        ReadMe                  this file

        LICENSE                 BSD 3-clause license

        input_data/             Directory of containing csv files used to load the experimental data. 
                                This information is broken up into four directories: eyring, melt, 
                                mutant_spectral_scans, and spectrum. 

        output/                 Output data in the form of csv text files, png images, and PDF files. 
                                Includes energetics, melt, and best-fit model parameters

        Thermal_kinetics_and_stability_analysis.ipynb         
                                First jupyter notebook in the series. This notebook takes data generated 
                                from kinetics experiments at varying temperatures and calculate the 
                                transition state thermodynamic properties. The notebook then plots the results,
                                saving results to the output directory 

        Spectra_melt_analysis.ipynb  
                                Second jupyter notebook in the series. This notebook takes data generated from a 
                                Jasco J-815 CD Spectrometer and analyze it for: 1. The far UV spectra in the 
                                light and dark. 2. The alpha helical content as measured by CD at 222nm at different 
                                temperatures to determine the thermal stability of the protein in the light and dark.
                                3. Determine the effect of this light dependent effect on thermal stability and compare 
                                it with the light dependent effect on transition state thermodynamics. These three steps
                                draw on data stored in spectrum, melt, and mutant_spectral_scans, respectively. Those
                                directories are located in input_data. The notebook also loads in energetics data from 
                                Thermal_kinetics_and_stability_analysis.ipynb and compares the results, plotting them with 
                                the melt data and saving the results to the output directory. 

        thermal_kinetics.yml    Yaml file corresponding to Thermal_kinetics_and_stability_analysis.ipynb



        spectra_melt.yml        Yaml file corresponding to Spectra_melt_analysis.ipynb