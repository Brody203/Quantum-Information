My Goals for this project:

Mathematical: Understand and derive quantum phase estimation using linear algebra, complex numbers, eigenvalues, eigenvectors, and tensor products.

Computational: Implement QPE from scratch in Python and investigate how accurately it estimates eigenvalue phases as the number of qubits change


# Quantum Phase Estimation Simulator

## Overview

This project focuses on the mathematical foundations and computational implementation of the **Quantum Phase Estimation (QPE) algorithm**.

Quantum Phase Estimation is a fundamental quantum algorithm used to estimate the phase associated with an eigenvalue of a unitary operator. It is an important subroutine in quantum algorithms such as Shor's factoring algorithm and quantum simulation.

Given a unitary operator \(U\) and one of its eigenstates \(|\psi\rangle\),

\[
U|\psi\rangle = e^{2\pi i\theta}|\psi\rangle,
\]

the objective is to estimate the unknown phase \(\theta \in [0,1)\).

The goal of this project is to derive the algorithm mathematically, implement its operations using Python and NumPy, and investigate its accuracy under different configurations.

## Mathematical Foundations

The project explores several mathematical concepts underlying quantum computation:

- **Complex Vector Spaces:** Representing quantum states as normalized complex vectors.
- **Eigenvalues and Eigenvectors:** Understanding the spectral properties of unitary operators.
- **Matrix Operations:** Constructing and applying quantum gates through matrix multiplication.
- **Tensor Products:** Constructing multi-qubit state spaces.
- **Unitary Matrices:** Understanding probability-preserving quantum transformations.
- **Quantum Fourier Transform:** Deriving and implementing the inverse QFT.
- **Measurement Theory:** Calculating measurement probabilities and interpreting measurement outcomes.

## Algorithm Structure

The simulator will implement the standard Quantum Phase Estimation procedure:

1. Initialize the phase register and target eigenstate.
2. Apply Hadamard gates to the phase register.
3. Apply controlled powers of the unitary operator \(U^{2^k}\).
4. Apply the inverse Quantum Fourier Transform.
5. Measure the phase register.
6. Convert the measurement outcome into an estimate of \(\theta\).

## Implementation

**Language:** Python

**Libraries:**
- NumPy — matrix operations, complex vectors, tensor products, and linear algebra.
- Matplotlib — visualizing measurement distributions and estimation accuracy.

The core algorithm will be implemented from scratch rather than relying on an existing quantum computing framework.

## Initial Experiment

Begin with a diagonal unitary operator:

\[
U =
\begin{bmatrix}
1 & 0\\
0 & e^{2\pi i/8}
\end{bmatrix}.
\]

Using the eigenstate

\[
|\psi\rangle =
\begin{bmatrix}
0\\
1
\end{bmatrix},
\]

the corresponding eigenvalue is

\[
\lambda = e^{2\pi i/8}.
\]

Therefore, the expected phase is

\[
\boxed{\theta = \frac{1}{8}}.
\]

The initial experiment will test whether the simulator correctly estimates this phase.

## Experiments and Analysis

The project will investigate:

- Phase estimation with different numbers of evaluation qubits.
- Exact versus non-exact binary phase representations.
- Measurement probability distributions.
- Estimation accuracy and precision.
- The effects of finite measurement shots.
- The relationship between the Quantum Fourier Transform and phase estimation.

## Research References

1. A. Y. Kitaev (1995), *Quantum Measurements and the Abelian Stabilizer Problem*. [arXiv:quant-ph/9511026](https://arxiv.org/abs/quant-ph/9511026)

2. R. Cleve, A. Ekert, C. Macchiavello, and M. Mosca (1998), *Quantum Algorithms Revisited*. [arXiv:quant-ph/9708016](https://arxiv.org/abs/quant-ph/9708016)

3. R. B. Griffiths and C.-S. Niu (1996), *Semiclassical Fourier Transform for Quantum Computation*. [arXiv:quant-ph/9511007](https://arxiv.org/abs/quant-ph/9511007)

4. P. W. Shor (1994), *Algorithms for Quantum Computation: Discrete Logarithms and Factoring*. [arXiv:quant-ph/9508027](https://arxiv.org/abs/quant-ph/9508027)

## Project Objective

The ultimate objective is to develop a working Quantum Phase Estimation simulator while demonstrating a mathematical understanding of the linear algebra, complex vector spaces, unitary transformations, and Fourier analysis that make the algorithm possible.
