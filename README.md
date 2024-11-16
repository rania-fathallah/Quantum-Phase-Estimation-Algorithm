# Quantum Phase Estimation Algorithm (QPE) with Qiskit

This repository implements the Quantum Phase Estimation (QPE) algorithm using Qiskit. QPE is a powerful subroutine in quantum computing used to estimate the unknown phase of an eigenvalue of a unitary operator.

## What is QPE?

Imagine you have a box containing a coin. You can perform a specific operation (the unitary operator) on the coin, but you can't see inside the box to directly determine its state (eigenvalue). QPE allows you to estimate the probability of the coin landing on heads (the phase) by applying a series of quantum operations.

## How does QPE work?

QPE utilizes two registers:

1. **Counting register**: This register consists of multiple qubits initialized in the superposition state using Hadamard gates. The number of qubits determines the accuracy of the phase estimation.
2. **Eigenstate register**: This register holds the initial state (eigenvector) corresponding to the unknown phase.

### Steps in the Algorithm

1. **Controlled Rotation**: Controlled rotations (controlled-T or controlled-Hadamard) are applied between the counting register qubits and the eigenstate register qubit. These rotations depend on the unknown phase you're trying to estimate.
2. **Inverse Quantum Fourier Transform (QFT)**: The inverse QFT transforms the state of the counting register from its superposition state to the computational basis.
3. **Measurement**: Each qubit in the counting register is measured, resulting in a binary string representing an approximation of the unknown phase.

## Running the Code

1. Install the required libraries (refer to the explanation below).
2. Execute the code cells in your Python script or Jupyter Notebook.

## Explanation of the Code

The code defines two quantum circuits:

1. **Circuit with controlled-T**: This circuit implements the QPE algorithm using controlled-T rotations.
2. **Circuit with controlled-Hadamard**: This circuit demonstrates an alternative implementation using controlled-Hadamard rotations.

### Actions Performed by the Code

For each circuit:

- Defines the quantum circuit with the appropriate number of qubits.
- Applies Hadamard gates to the counting register qubits.
- Implements the controlled rotations and the inverse QFT.
- Measures the counting qubits.
- Simulates the circuit on a backend (simulator or real device).
- Visualizes the measurement results using histograms.

## (Optional) Running on a Real Quantum Device

The code allows you to run the circuit on a real quantum device using your IBM Quantum Experience account. However, this might take longer due to device availability and processing times.

## Additional Resources

- [Qiskit documentation](https://www.ibm.com/quantum)
- [Quantum Phase Estimation](https://en.wikipedia.org/wiki/Quantum_phase_estimation_algorithm)
