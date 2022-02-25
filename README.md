# QHack2022 Project: LiH Excited States

We (QStruggler) want to find the first excited state of a LiH molecule.
There are two excited states (2-1Sigma+, 1-3Sigma+) very near the ground state.
Reference: https://aip.scitation.org/doi/10.1063/1.1677704
We will try to differentiate these two states using `qiskit` and `qumay`.

## original calculations from the reference

We take https://aip.scitation.org/doi/10.1063/1.1677704 as reference and find out the three lowest energies as the ground state energy, 1st excited state energy, and 2nd excited state energy of LiH.
The energies and corresponding states are listed below:
$1{\text -}{}^1\Sigma^+=-8.0160$
$1{\text -}{}^3\Sigma^+=-7.9152$ ,  $\Delta E_1=1{\text -}{}^3\Sigma^+ - 1{\text -}{}^1\Sigma^+=0.1008$
$2{\text -}{}^1\Sigma^+=-7.8998$ ,  $\Delta E_2=2{\text -}{}^1\Sigma^+ - 1{\text -}{}^1\Sigma^+=0.1162$


## calculations with qamuy

We try to caculate the excited states of LiH with `qumay`. We can only calculate two excited states. When the parameter `num_excited_states` is 3 or above, we get nothing.

For the final results, we get:
- ground state energy: -7.979410371934547
- 1st excited state energy: -7.829952097591878, $\Delta E_1=0.149458274342669$
- 2nd excited state energy: -7.305933835615826, $\Delta E_2=0.673476536318721$

Comparing the results with the reference, we find out that our results have obvious differences with those from the reference, especially for the 2nd excited state.