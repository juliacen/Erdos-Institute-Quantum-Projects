
# MCU Decompositions: Multi-Controlled U Gate in Qiskit

This project demonstrates how to **decompose a multi-controlled single-qubit unitary gate** using only single-qubit gates and CNOTs, based on methods from *Nielsen and Chuang's Quantum Computation and Quantum Information* (Chapter 4).

It also explores various **Qiskit implementations** of multi-controlled gates, including `MCMTGate`, `ControlledGate`, and manual decompositions using Gray code and Barenco-style constructions.

---

## 📘 Features

- ✅ Explanation of multi-controlled unitary gate definition
- ✅ Euler angle decomposition of any 2×2 unitary matrix
- ✅ Construction of `CⁿU` from elementary gates
- ✅ Comparison of:
  - `MCMTGate`
  - `ControlledGate`
  - Manual Gray-code-based decomposition
- ✅ Circuit visualization and correctness verification via statevector comparisons

---

## 📁 Files

- `MCUdecompositions.ipynb`: Main Jupyter notebook with explanations, code, and circuit visualizations.

---

## 🧠 Background

The goal is to build a circuit for:
\[
C^{n}U |x\rangle_n |y\rangle = 
\begin{cases}
|x\rangle_n U|y\rangle, & \text{if } x = (1,1,...,1) \\
|x\rangle_n |y\rangle, & \text{otherwise}
\end{cases}
\]

We do this by:
1. Extracting Euler angles from the target unitary.
2. Constructing the decomposition using CNOTs and RZ/RY gates.
3. Using ancilla qubits to reduce control complexity when needed.

---

## 🧪 Dependencies

- [Qiskit](https://qiskit.org/)
- NumPy
- Matplotlib (optional, for any plots)

Install via pip:

```bash
pip install qiskit numpy matplotlib
```

---

## 🛠️ Usage

Clone the repository and run the notebook:

```bash
git clone https://github.com/your-username/MCUdecompositions.git
cd MCUdecompositions
jupyter notebook MCUdecompositions.ipynb
```

You can modify the input unitary matrix to test different decompositions.

---

## 📚 References

1. M.A. Nielsen & I.L. Chuang, *Quantum Computation and Quantum Information* (Cambridge University Press, 2000).
2. Qiskit Documentation: https://qiskit.org/documentation/

---

## 🧑‍💻 Author

**Julia Cen**  
Feel free to connect or raise issues/PRs for improvements!
