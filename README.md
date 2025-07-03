# Decompositions of the Multi-controlled U Gate

**Author**: Julia Cen

This repository contains a Jupyter notebook that explores multiple strategies for decomposing **multi-controlled unitary (MCU)** quantum gates into basic 1- and 2-qubit gates. The study includes both theoretical decompositions based on seminal quantum computing literature and practical implementations using Qiskit's built-in features.

## 📘 Overview

Multi-controlled unitary gates are an essential component in quantum algorithms like Grover’s search and quantum arithmetic circuits. However, directly implementing these gates on real hardware requires decomposing them into native quantum gates (such as CNOT and single-qubit rotations).

This notebook:

- Explains how to decompose MCU gates using various methods
- Implements and compares decompositions manually and with Qiskit
- Analyzes resource requirements (e.g., number of CX gates)
- Benchmarks the performance of different decomposition strategies

## 🧪 Contents

### 1. Finding Phase and Euler Angles
Extracts the necessary parameters to express any single-qubit unitary \( U \) in terms of its ZYZ Euler decomposition.

### 2. Implementing MCU Gates in Qiskit
Uses Qiskit's built-in functionality to implement controlled unitary operations for small-scale demonstrations.

### 3. Nielsen & Chuang Figure 4.10
Reproduces and explains the decomposition circuit for a controlled- \( U \) operation based on Figure 4.10 in the standard quantum computing textbook.

### 4. Decomposing CCX and CU Gates
Builds decompositions for Toffoli (CCX) and controlled-unitary (CU) gates using only CNOTs and 1-qubit rotations.

### 5. MCU Decomposition with Basic Gates
Presents a general approach to decompose any MCU gate into a sequence of CNOT and 1-qubit operations. Also compares implementations with and without ancilla qubits.

### 6. Benchmarking
Measures circuit depth and gate count across decomposition methods to evaluate scalability and hardware feasibility.

### 7. Complexity Analysis
Summarizes the gate complexity of different decomposition techniques with respect to the number of control qubits.

### 8. Alternative Methods
Mentions newer or specialized decomposition techniques (e.g., linear-depth methods) from recent literature.

## ⚙️ Requirements

To run the notebook, install the following:

- Python 3.7+
- Jupyter Notebook or JupyterLab
- `numpy`
- `qiskit`
- `matplotlib` (optional for visualization)

```bash
pip install numpy qiskit matplotlib
```

## 🚀 Getting Started

1. Clone the repository:

```bash
git clone https://github.com/yourusername/mcu-decompositions.git
cd mcu-decompositions
```

2. Launch the notebook:

```bash
jupyter notebook MCUdecompositions.ipynb
```

## 📚 References

1. Nielsen, M. & Chuang, I. (2011). *Quantum Computation and Quantum Information*, Cambridge University Press.
2. Barenco, A. et al. (1995). *Elementary gates for quantum computation*, Physical Review A, 52(5), 3457.
3. Da Silva, A.J. & Park, D.K. (2022). *Linear-depth quantum circuits for multiqubit controlled gates*, Physical Review A, 106(4), 042602.
