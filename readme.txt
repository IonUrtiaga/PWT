-----------------------------------PureWindTool(PWT)------------------------------------------
    Ion Urtiaga Chasco (2025)                              ion.urtiaga@outlook.es
_______________________________________________________________________________________________

The PureWindTool (PWT) is a Jupyter Notebook-based framework developed within the PUREWIND project (JPI Oceans initiative). It is designed to simulate underwater noise propagation from offshore wind turbines and evaluate potential acoustic impacts in the marine environment.

The tool integrates source modelling, environmental data, and acoustic propagation models to generate spatial and spectral estimates of underwater sound levels across user-defined scenarios.


The PureWindTool folder must include the following files:

-PWT.ipynb (PWT main Jupiter Notebook)
-PWT_noCopernicus.ipynb (PWT JN adapted to run without Copernicus account)
-PWT_fromCSV.ipynb (PWT JN adapted to run from a CSV file)
-aux (folder with turbine noise .mat and temperature and salinity .nc files)
-bellhop_linux.exe (Compilation of Bellhop program for Linux)
-bellhop_mac (Compilation of Bellhop program for Mac)
-bellhop.exe (Compilation of Bellhop program for Windows)
-PyRAM.py (adapted version of original PyRAM, to allow compatibility)
-PWT_inputs.csv (CSV file used in PWT_fromCSV.ipynb)

To execute the PWT, open the desired Jupyter Notebook (.ipynb extension):

- PWT.ipynb -
It is the basic PWT notebook

- PWT_noCopernicus.ipynb -
Same as PWT.ipynb but using an already downloaded NETCDF file, contained in aux folder, so the user doesn't need a Copernicus account.

- PWT_fromCSV -
Similar, but taking the inputs from a CSV file.

Notes

This tool provides a simplified representation of underwater sound propagation in offshore wind farm environments. Results should be interpreted as model-based estimates and, where possible, supported with observational data and additional ecological context.


------------------------------ ## References and Credits ## ----------------------------------

This notebook uses several external libraries and tools:

- **pyRAM** (Donnelly, 2017): Python adaptation of RAM. (https://pypi.org/project/pyram/)
- **Bellhop** (Porter, 2005): Original Fortran program, freely available (http://oalib.hlsresearch.com/AcousticsToolbox/)
- **Arlpy** (Chitre, 2020): Python library for processing Bellhop outputs. (https://github.com/org-arl/arlpy/)
- **Copernicus Marine Toolbox API - Subset**: Used for oceanographic data retrieval. (https://help.marine.copernicus.eu/en/articles/8283072-copernicus-marine-toolbox-api-subset)
- **EDDAPY**: Python client for accessing ERDDAP servers.
