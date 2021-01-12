# State Inpired Ansatz of H<sub>2</sub>

The UCCSD operator to the Hartree Fock state of a Hydrogen molecule (STO-3G basis set) would give the equation:

<pre align="center" <a href="https://www.codecogs.com/eqnedit.php?latex=U|0101\rangle&space;=&space;\cos&space;(\theta&space;)|0101\rangle&space;-&space;\sin&space;(\theta&space;)|1010\rangle" target="_blank"><img src="https://latex.codecogs.com/gif.latex?U|0101\rangle&space;=&space;\cos&space;(\theta&space;)|0101\rangle&space;-&space;\sin&space;(\theta&space;)|1010\rangle" title="U|0101\rangle = \cos (\theta )|0101\rangle - \sin (\theta )|1010\rangle" /></a> </pre>
This is slightly different from Eq. (105) in [Quantum computational chemistry](https://arxiv.org/abs/1808.10402) by McArdle et al. becasue the spin orbitals (Jordan-Wigner mapping type) from the Qiskit package is ordered by spin down orbitals to spin up orbitals instead of an alternate arrangement of the spin up and spin down orbitals.

I could thus design a quantum circuit (image below) that satifies that equation and I call this new ansatz a State Inpired Ansatz because the final state of the Hartree Fock state after the UCCSD operation is used to design this low-depth ansatz.
| *State Inpired Ansatz with One Parameter* |
|-------------------------|
| <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/State%20Inspired%20H2/Image/State%20Inspired%20Ansatz.png" width="440">|

Result showed that all the energy on the potential energy surfaces obtained from the State Inpired and the UCCSD Ansatz was found to reach the chemical accuracy (1 kcal/mol) on a quantum simulator. However, the State Inpired Ansatz has a much lower depth than the UCCSD Ansatz so the State Inpired Ansatz would be able to reach a better accuracy in a real quantum device.

| *Potential Energy Surface of H<sub>2* | *Error of the Energy obtained from the State Inpsired <br /> and the UCCSD Ansatz* |
|------------|-------------|
| <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/State%20Inspired%20H2/Image/Potential%20Energy%20Surface.png" width="500"> | <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/State%20Inspired%20H2/Image/Error%20Comparison.png" width="500"> |
