# Erdos-Institute-Quantum-Projects

In this notebook, we will construct a multi-controlled U $\in$ U(2) gate that is composed of only 1-qubit gates and $CX$ gates. The definition of a multi-controlled U gate is as follows

\begin{equation}
C^{n}U |x\rangle_n |y\rangle_1=
\begin{cases}
    |x\rangle_n U|y\rangle_1,& \text{if } x= (1,1,\dots,1)\\
    |x\rangle_n |y\rangle_1,              & \text{otherwise}
\end{cases}
\end{equation}

meaning that the U gate only acts on our target qubit, $1$, only if all $n$ of our control qubits are in the $1$ state and we do nothing otheriwse. The construction presented below follows the decomposition presented in Chapter 4 of the Nielson and Chaung textbook.
