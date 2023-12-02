# QuantumMechanicsVisualized

This repository contains functions to calculate and visualize the probability density of hydrogen atom orbitals in both 2D and 3D.

## Theoretical Background

The probability density $|\Psi|^2$ of the hydrogen atom's electron is calculated using the wave function $\Psi$, which is a product of the radial and angular parts. The radial part depends on the principal and azimuthal quantum numbers `n` and `l`, while the angular part depends on the azimuthal and magnetic quantum numbers `l` and `m`.

### Radial Part

The radial part of the wave function is given by:

$$ R_{nl}(r) = \sqrt{\left(\frac{2}{n a_0}\right)^3 \frac{(n-l-1)!}{2n[(n+l)!]^3}} e^{- \frac{r}{n a_0}} \left(\frac{2r}{n a_0}\right)^l L_{n-l-1}^{2l+1}\left(\frac{2r}{n a_0}\right) $$

where `L` are the generalized Laguerre polynomials and $a_0$ is the Bohr radius.

### Angular Part

The angular part of the wave function is given by the spherical harmonics:

$$ Y_{lm}(\theta, \phi) = (-1)^{\frac{m + |m|}{2}} \sqrt{\frac{(2l + 1)}{4\pi} \frac{(l - |m|)!}{(l + |m|)!}} P_l^{|m|}(\cos \theta) e^{im\phi} $$

where $P_l^m$ are the associated Legendre polynomials.

### Probability Density

The probability density $|\Psi|^2$ is the product of the square of the radial part and the square of the absolute value of the angular part:

$$ |\Psi|^2 = |R_{nl}(r) Y_{lm}(\theta, \phi)|^2 $$

## Functions

### `calculate_hydrogen_density_2d`

Calculates the 2D probability density of a hydrogen atom orbital.

#### Parameters
- **n (int)**: Principal quantum number, defines the energy level.
- **l (int)**: Azimuthal quantum number, defines the shape of the orbital.
- **m (int)**: Magnetic quantum number, defines the orientation of the orbital.
- **$a_0$ (float)**: Bohr radius, default is 1.0.
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
- **$a_0$ (float)**: Bohr radius, default is 1.0.
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
