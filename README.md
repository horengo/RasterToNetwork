## RasterToNetwork
Jupyter Notebook to transform a raster file depicting spatial conections (roads, corridors, rivers, channels, etc.) into a full network <br>

<img width="149" height="203" alt="image" src="https://github.com/user-attachments/assets/fcedc42c-b518-4cc3-b553-e3800acc6af9" />
<img width="149" height="203" alt="image" src="https://github.com/user-attachments/assets/7cf20767-80de-4797-ad5d-41bcaf60f8c6" />
<img width="149" height="203" alt="image" src="https://github.com/user-attachments/assets/9753a5ec-a198-4142-9fad-75b01d48a44e" />


<br>

The Notebook is designed to provide tools to: <br>

- Skeletonise a raster network-style file using a rage of values <br>

- Eliminate groups of contiguous pixels if necessary (this can also be done at a later stage using the network segments lenght) <br>

- Transform the skeletonised raster into a network gpkg file including nodes and edges. This cell provides a series of optional modifiers for the creation and weghting of the network:

  - Edge smoothing, which addresses the typical 'stairs' shape of vectorised raster files
  - Gap filling: endpoint to endpoint, joins line endpoints within a user defined angle and distance
  - Gap filling: endpoint to vertex, joins line endpoints and vertices in nearby lines within a user defined angle and distance
  - Joins closely running (parallel or near-parallel) lines by adding connectors within a user defined angle and distance
  - Adds directionality from a user-provided slope/aspect/flow-direction raster
  - Adds costs per edge from a user-provided cost raster <br>

- Provides network metrics for neodes and edges as columns in the gpkg file's table <br>

## Setting up the environment

Create and activate an env using the provided YAML file: <br>
```
conda env create -f RasterToNetwork.ipynb  # Creates the environemt and installs the pinned packages
conda activate RasterToNetwork  # Activates the environment
python -m ipykernel install --user --name RasterToNetwork --display-name "RasterToNetwork"  # Optional: registers your current Python environment as a selectable Jupyter kernel. No need to use if you are going to lauch Jupyter from RasterToNetwork environment <br>
```
