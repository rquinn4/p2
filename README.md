# Spectral Solutions to Schrödinger's Equation

The Schrödinger equation is the foundational equation of quantum mechanics. It describes the behavior of particles by describing how their wavefunction evolves in space or time. In its time-independent form, it is written as:

$$
-\frac{\hbar^2}{2m} \nabla^2 \psi(\mathbf{r}) + V(\mathbf{r}) \psi(\mathbf{r}) = E \psi(\mathbf{r})
$$

Here:
- `ψ(r)` is the wavefunction,
- `V(r)` is the potential,
- `E` is the energy,
- `ħ` is the reduced Planck constant,
- and `∇²` is the Laplacian operator.

Analytical solutions exist for only a few potential energy functions. To study more complex systems, we use spectral methods.

This project numerically solves the time-independent Schrödinger equation using spectral methods for the following potential energy models:

1. Square Barrier
2. Simple Harmonic Oscillator
3. Hydrogen Atom (2D Approximation)
4. Double Well Potential (2D)

There are two key features used in all the models, apart from general methods, that we use to solve the equations:

1. Defining a fourier space, so that the laplacian becomes just a multiplication by -k^2 (-k_x^2 - k_y^2 in 2D)
2. Finding Eigenvalues and Eigenvectors numerically using the eigsh function from scipy.sparse.linalg

Required Dependencies:

1. numpy
2. matplotlib
3. scipy

Team members: Luke, Ryan, Amrit
