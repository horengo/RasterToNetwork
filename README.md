## RasterToNetwork
Jupyter Notebook to transform a raster file depicting spatial conections (roads, corridors, rivers, channels, etc.) into a full network

The Notebook is designed to provide tools to:

- Skeletonise a raster network-style file using a rage of values
<img width="198" height="170" alt="image" src="https://github.com/user-attachments/assets/d10c8085-d9c9-4bd8-89ef-a872b7198e3d" />



<img width="198" height="170" alt="image" src="https://github.com/user-attachments/assets/8d85b53a-4b1f-465a-960f-95c4f1a407db" />


- 

## Setting up the environment

Create and activate an env using the provided YAML file: <br>
```
conda env create -f RasterToNetwork.ipynb  # Creates the environemt and installs the pinned packages
conda activate RasterToNetwork  # Activates the environment
python -m ipykernel install --user --name RasterToNetwork --display-name "RasterToNetwork"  # Optional: registers your current Python environment as a selectable Jupyter kernel. No need to use if you are going to lauch Jupyter from RasterToNetwork environment <br>
```
