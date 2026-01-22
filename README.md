## RasterToNetwork
Jupyter Notebook to transform a raster file depicting spatial conections (roads, corridors, rivers, channels, etc.) into a full network

The Notebook is designed to 

## Setting up the environment

Create and activate an env using the provided YAML file: <br>
```
conda env create -f environment_m2conet.yml  # Creates the environemt and installs the pinned packages
conda activate m2conet  # Activates the environment
python -m ipykernel install --user --name m2conet --display-name "m2conet"  # Optional: registers your current Python environment as a selectable Jupyter kernel. No need to use if you are going to lauch Jupyter from m3conet environment (the YAML file installs jupyterlab) <br>
```

***Alternatively***, if you prefer to use the provided requirements pip file instead of conda pins, install only the heavy libs with conda, then pip the pinned set (helps when pip wheels struggle with GDAL/PROJ). <br>
```
conda create -n m2conet -c conda-forge python=3.10 -y  # Creates the environemt (with a supported Python 3.10, which is safe for NumPy 1.26.x) and installs the pinned packages
conda activate m2conet  # Activates the environemt
conda install -c conda-forge python=3.10 rasterio gdal -y  # Installs the pinned packages
pip install -r /mnt/data/requirements_M2CoNet.txt
python -m ipykernel install --user --name m2conet --display-name "m2conet"  # Register the kernel in Jupyter (optional, see above)
```
