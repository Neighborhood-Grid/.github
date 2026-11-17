The discrete space-filling (or serialization) problem consists in organizing spatial data so that geometric processing can be performed efficiently. One want to sort a dataset in a spatially coherent way rather than just arbitrary as they come up in memory.

Space-filling curves solve this by mapping multidimensional data to a one-dimensional ordering. However, this unfolding can break local spatial relationships: nearby points may become distant in the resulting order.

`Neighborhood-grids`, instead of reducing the data to one dimension, construct a regular multidimensional grid passing through all points. Each point $(x,y,z,\ldots)$ receives a `spatial multi-index` $[i,j,k,\ldots]$, preserving the geometric structure of the original point cloud. The local neigborhood preservation is ensured by the stable-state property and it's extension, describing how the points coordinates evolved along the axes of the grid.
Thus a neighborhood-grid is nothing more but a multi-dimensional sorting algorithm with a grid based storage instead of standard linear storage. Kind of an adaptative, bijective voxel structure with a strict one-to-one correspondance between data points and grid cells.



The project is split into four repositories:

- [Cartesian Grid Sort](https://github.com/Neighborhood-grid/Cartesian-Grid-Sort): starting point: mathematical details of the optimization algorithm.
- [Squarenet](https://github.com/Neighborhood-grid/SquareNet): Python package with extensive fonctionalities (plot, neighbor querys, tutorials)
- [Gridpoints](https://github.com/Neighborhood-grid/gridpoints): v2, enhanced optimizatino algorithm
- [Flatpoints](https://github.com/Neighborhood-grid/flatpoints): specialised for thin / flat point clouds (surfaces)

Theoretical background:

For neighborhood grid: Skrodzki, Reitebuch, Polthier, arXiv:1710.03435, 2018 (expanded in: Skrodzki, PhD thesis, Freie Universität Berlin, 2019).
See also Kaplan, C., Dahm, J., Oran, E., Alexandrov, N., & Boris, J. (2010). The Monotonic Lagrangian Grid for rapid air-traffic evaluation. AIAA Paper 2010-9336 for monotonic lagrangian grid and extensions 
