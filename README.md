## RasterToNetwork
Jupyter Notebook to transform a raster file depicting spatial conections (roads, corridors, rivers, channels, etc.) into a full network

The Notebook is designed to provide tools to:

- Skeletonise a raster network-style file using a rage of values
<img width="198" height="170" alt="image" src="https://github.com/user-attachments/assets/d10c8085-d9c9-4bd8-89ef-a872b7198e3d" />

<img width="198" height="170" alt="image" src="https://github.com/user-attachments/assets/8d85b53a-4b1f-465a-960f-95c4f1a407db" />

- Eliminate groups of contiguous pixels if necessary (this can also be done at a later stage using the network segments lenght) 
- Transform the skeletonised raster into a network gpkg file including nodes and edges. This cell provides a series of optional modifiers for the creation and weghting of the network:
  - Edge smoothing, which addresses the typical 'stairs' shape of vectorised raster files
  - Gap filling: endpoint to endpoint, joins line endpoints within a user defined angle and distance
  - Gap filling: endpoint to vertex, joins line endpoints and vertices in nearby lines within a user defined angle and distance
  - Joins closely running (parallel or near-parallel) lines by adding connectors within a user defined angle and distance
  - Adds directionality from a user-provided slope/aspect/flow-direction raster
  - Adds costs per edge from a user-provided cost raster
- Provides network metrics for neodes and edges as columns in the gpkg file's table

## Setting up the environment

Create and activate an env using the provided YAML file: <br>
```
conda env create -f RasterToNetwork.ipynb  # Creates the environemt and installs the pinned packages
conda activate RasterToNetwork  # Activates the environment
python -m ipykernel install --user --name RasterToNetwork --display-name "RasterToNetwork"  # Optional: registers your current Python environment as a selectable Jupyter kernel. No need to use if you are going to lauch Jupyter from RasterToNetwork environment <br>
```
