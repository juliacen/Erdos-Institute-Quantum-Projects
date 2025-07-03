# Multi-controlled Unitary Gate Decomposition

This repository contains a Jupyter notebook that explores the decomposition of **multi-controlled unitary (MCU)** quantum gates. Specifically we look at an arbitary 2x2 unitary and restrict ourselves to the use of single-qubit and cnot gates only.

## Introduction

Multi-controlled unitary gates are a powerful class of operations in quantum computing. They apply a specific unitary operation to the target qubit only when all control qubits are in the 1-state. However, these gates are not directly implementable on quantum hardware. They require decomposition into simpler native quantum gates, which is the aim of this project.

## Contents of Notebook

### 1. Finding Phase and Euler Angles for a Given Unitary Matrix
Extracts the necessary parameters to express any single-qubit unitary in terms of its ZYZ Euler decomposition.

### 2. Implementing MCU Gates with Built-in Qiskit Function
Uses Qiskit's built-in functionality to implement controlled unitary operations for demonstration.

### 3. Nielsen & Chuang Decomposition
Reproduces and explains the decomposition circuit for a controlled operation based on Figure 4.10 in the standard quantum computing textbook.

### 4. Decomposing CCX and CU Gates
Builds decompositions for Toffoli (CCX) and controlled-unitary gates using only CNOTs and 1-qubit rotations.

### 5. Decomposing MCUs
Put everything together and present a general approach to decompose any MCU gate into a sequence of CNOT and 1-qubit operations.

### 6. Benchmarking
Testing that the decompostion works!

### 7. Complexity Analysis
Summarizes resource costs (number of gates and gate depth) for MCUs with an abitrary number of control qubits.
