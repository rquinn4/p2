# Spectral Solutions to Schrödinger's Equation

## Introduction

The **Schrödinger equation** is the foundational equation of non-relativistic quantum mechanics. It governs the quantum behavior of particles by describing how their wavefunction evolves in space or time. In its time-independent form, it is written as:

Here:
- `ψ(r)` is the wavefunction,
- `V(r)` is the potential energy,
- `E` is the energy eigenvalue,
- `ħ` is the reduced Planck constant,
- and `∇²` is the Laplacian operator.

Analytical solutions exist for only a few potential energy functions. To study more complex systems, we use **spectral methods**—numerical techniques known for their high spatial accuracy and convergence efficiency.

## Systems Studied

This project numerically solves the time-independent Schrödinger equation using spectral methods for the following potential energy models:

### 1. Square Barrier (1D)

A finite potential barrier separating two regions. This setup illustrates quantum tunneling and the existence of bound and scattering states.

### 2. Simple Harmonic Oscillator (1D)

A quadratic potential well. This model has known analytical solutions and serves as a benchmark to validate our numerical implementation.

### 3. Hydrogen Atom (2D Approximation)

A two-dimensional approximation of the hydrogen atom using a Coulomb-like potential. We study the resulting bound states and degeneracy of energy levels.

### 4. Double Well Potential (2D)

A two-dimensional potential with two symmetric minima. This system exhibits quantum tunneling between wells and energy level splitting due to symmetry breaking.

## Methodology

We employ **spectral methods** to convert the Schrödinger equation into a matrix eigenvalue problem:

- The spatial domain is discretized using a uniform grid.
- The kinetic energy operator is approximated using a spectral (Fourier or sine basis) second-derivative matrix.
- The total Hamiltonian is constructed as: `H = T + V`, where `T` is the kinetic energy matrix and `V` is the diagonal potential matrix.
- The eigenvalues and eigenvectors of `H` give us the energy levels and wavefunctions.
