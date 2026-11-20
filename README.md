# PureWindTool (PWT)

**Ion Urtiaga Chasco (2025)**  
ion.urtiaga@outlook.es  

---

## Overview

The PureWindTool (PWT) is a Jupyter Notebook-based framework developed within the **PUREWIND project (JPI Oceans initiative)**. It is designed to simulate underwater noise propagation from offshore wind turbines and evaluate potential acoustic impacts in the marine environment.

The tool integrates source modelling, environmental data, and acoustic propagation models to generate spatial and spectral estimates of underwater sound levels across user-defined scenarios.

---

## Repository contents

- **PWT.ipynb**  
  Main Jupyter Notebook for the standard workflow.

- **aux/**  
  Folder containing turbine noise spectral `.mat` files (wind speeds 3–16 m/s).

- **bellhop_linux.exe**  
- **bellhop_mac**  
- **bellhop.exe**  
  Bellhop executables for Linux, macOS, and Windows.

- **PyRAM.py**  
  Adapted version of the original PyRAM implementation for compatibility.

- **readme.txt**  
  Additional notes.

---

## How to use

Open **PWT.ipynb** in Jupyter and follow the step-by-step workflow:

1. Set working directory and install required modules (first run only).
2. Define inputs: source and receiver locations, date, sediment type, wind speed.
3. Compute turbine noise spectra.
4. Load seabed geoacoustic properties.
5. Download bathymetry (EMODnet) and temperature/salinity (Copernicus Marine).
6. Run RAM (f < 1 kHz) or Bellhop (f ≥ 1 kHz) propagation model.
7. Plot and export results.

A Copernicus Marine account is required for environmental data download.  
Register at: https://data.marine.copernicus.eu/register

---

## Notes

This tool provides a simplified representation of underwater sound propagation in offshore wind farm environments. Results should be interpreted as model-based estimates and, where possible, supported with observational data and additional ecological context.

---

## References and external tools

- **pyRAM** (Donnelly, 2017) – Python adaptation of RAM  
  https://pypi.org/project/pyram/

- **Bellhop** (Porter, 2005) – Acoustic propagation model  
  http://oalib.hlsresearch.com/AcousticsToolbox/

- **ARLpy** (Chitre, 2020) – Processing tools for Bellhop outputs  
  https://github.com/org-arl/arlpy/

- **Copernicus Marine Toolbox API (Subset)** – Oceanographic data access  
  https://help.marine.copernicus.eu/en/articles/8283072-copernicus-marine-toolbox-api-subset

- **erddapy** – ERDDAP data access client