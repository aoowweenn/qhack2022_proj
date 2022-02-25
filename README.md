# QHack2022 Project: LiH Excited States

We (QStruggler) want to find the corresponding energies of the ground state and the first excited state of a LiH molecule.
The energy of the second excited state is also what we want to check.
We will try to find these energies using `qiskit` and `qamuy`.

## Calculations with qiskit
[`LiH_excited-final.ipynb`](qiskit/LiH_excited-final.ipynb)

### qiskit numpy eigensolver

- ground state energy: -7.881146 Ha
- 1st excited state energy: -7.765750 Ha, Delta E_1: 0.115396 Ha
- 2nd excited state energy: -7.748064 Ha, Delta E_2: 0.133083 Ha

### qiskit QEOM solution is not good

- ground state energy: -7.881101 Ha
- 1st excited state energy: -7.702501 Ha, Delta E_1: 0.178600 Ha
- 2nd excited state energy: -7.612108 Ha, Delta E_2: 0.268993 Ha

### qiskit runtime failed on both `ibmq_qasm_simulator` and `ibm_perth`
Please check [`LiH_excited-runtime-sim.ipynb`](qiskit/LiH_excited-runtime-sim.ipynb) and [`LiH_excited-runtime.ipynb`](qiskit/LiH_excited-runtime.ipynb)

## Calculations with qamuy
[`LiH_excitedstate.ipynb`](qamuy/LiH_excitedstate.ipynb)

We try to caculate the excited states of LiH with `qamuy`. We can only calculate two excited states. When the parameter `num_excited_states` is 3 or above, we get nothing.

For the final results, we get:
- ground state energy: -7.979410 Ha
- 1st excited state energy: -7.829952 Ha, Delta E_1: 0.149458 Ha
- 2nd excited state energy: -7.305933 Ha, Delta E_2: 0.673476 Ha

Comparing the results with the [reference](https://doi.org/10.1063/1.1677704), we find out that our results have obvious differences with those from the reference, especially for the 2nd excited state.
