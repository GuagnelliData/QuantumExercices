# Quantum Exercises - Unitarity and NAND

## Exercise 1: Composition of Unitary Operators

> Show that the product of two unitary matrices U and V is also unitary.  
> As a consequence, the net effect of any quantum circuit (before measurement) is to effect a unitary operation on the state space of the system.

### ✅ Solution:

Recall that a matrix \( U \) is unitary if:

\[
U^\dagger U = I
\]

Let \( U \) and \( V \) be unitary matrices. Then:

\[
(UV)^\dagger (UV) = V^\dagger U^\dagger U V = V^\dagger I V = V^\dagger V = I
\]

Thus, \( UV \) is unitary.

---

## Exercise 2: NAND gate with quantum circuits

### 🔹 What’s a quantum circuit that computes the NAND gate?

The NAND of two classical bits is defined as:

\[
\text{NAND}(x, y) = \text{NOT}(x \land y)
\]

Since NAND is not reversible, we use an ancillary qubit initialized to \( |1\rangle \).

### 🔹 Solution with a single Toffoli gate:

Let the initial state be \( |x\rangle |y\rangle |1\rangle \).  
Applying a Toffoli gate:

\[
\text{Toffoli}(x, y, 1) = |x\rangle |y\rangle |1 \oplus (x \land y)\rangle
\]

This third qubit ends up being \( \text{NAND}(x, y) \).

Thus, **a single Toffoli gate** computes the NAND if the target qubit is initialized to \( |1\rangle \).

