## RasterToNetwork
Jupyter Notebook to transform a raster file depicting spatial conections (roads, corridors, rivers, channels, etc.) into a full network

The Notebook is designed to provide tools to:

- Skeletonise a raster network-style file

- <img width="982" height="839" alt="image" src="https://github.com/user-attachments/assets/a86197b5-309a-4cac-a46e-28ad267e09ae" />

- 

## Setting up the environment

Create and activate an env using the provided YAML file: <br>
```
conda env create -f RasterToNetwork.ipynb  # Creates the environemt and installs the pinned packages
conda activate RasterToNetwork  # Activates the environment
python -m ipykernel install --user --name RasterToNetwork --display-name "RasterToNetwork"  # Optional: registers your current Python environment as a selectable Jupyter kernel. No need to use if you are going to lauch Jupyter from RasterToNetwork environment <br>
```
