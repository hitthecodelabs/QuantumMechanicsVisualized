# QuantumMechanicsVisualized

This repository contains functions to calculate and visualize the probability density of hydrogen atom orbitals in both 2D and 3D.

## Functions

### `calculate_hydrogen_density_2d`

Calculates the 2D probability density of a hydrogen atom orbital.

#### Parameters
- **n (int)**: Principal quantum number, defines the energy level.
- **l (int)**: Azimuthal quantum number, defines the shape of the orbital.
- **m (int)**: Magnetic quantum number, defines the orientation of the orbital.
- **a0 (float)**: Bohr radius, default is 1.0.
- **grid_size (int)**: Resolution of the grid for calculations.

#### Returns
- **X, Y, density**: 2D arrays representing the X, Y coordinates and the corresponding probability density.

#### Usage
```python
X, Y, density = calculate_hydrogen_density_2d(n, l, m, a0, grid_size)
```

### `calculate_hydrogen_density_3d`

Calculates the 3D probability density of a hydrogen atom orbital.

#### Parameters
- **n (int)**: Principal quantum number, defines the energy level.
- **l (int)**: Azimuthal quantum number, defines the shape of the orbital.
- **m (int)**: Magnetic quantum number, defines the orientation of the orbital.
- **a0 (float)**: Bohr radius, default is 1.0.
- **grid_size (int)**: Resolution of the grid for calculations.

#### Returns
- **X, Y, Z, density**: 3D arrays representing the X, Y, Z coordinates and the corresponding probability density.

#### Usage
```python
X, Y, Z, density = calculate_hydrogen_density_3d(n, l, m, a0, grid_size)
```

## Dependencies
- Numpy
- Scipy (for special functions like `sph_harm`)


## License
This project is open-source and available under the [MIT License](LICENSE.md).
