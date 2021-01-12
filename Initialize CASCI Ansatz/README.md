# Initialize CASCI Ansatz (Check out the HTML file if the plots in the notebook does not show up)

As a followup of the [State Inpired Ansatz of H<sub>2](https://github.com/randyshee/Quantum-Chemistry/tree/main/State%20Inspired%20H2) project, 
single excitations were also considered in this project. I prepared the Ansatz directly from the state vectors and produce the quantum 
circuits using the Qiskit Initializer so that this kind of Ansatz can be used as a complete active space configuration interaction (CASCI) 
Ansatz and had shorter depth than UCCSD Ansatz. On the other hand, since these states were directly prepared from the state vectors so the 
finals states would always be physical states (fixed numbers of electrons) unlike hardware-inspired Ansatz where the final states could be non-physical.

| *4 Qubit CASCI Ansatz for H<sub>2* |
|-------------------------|
| <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/Initialize%20CASCI%20Ansatz/Image/4%20Qubit%20Initialize%20Ansatz.png" width="1000">|

Potential energy surfaces of H<sub>2</sub> and LiH using the UCCSD or the Initialize CASCI Ansatz and their error comparing to the exact energy.
Notice that LiH uses 6 qubits so this method is a generalized method and could possibly scale up if the costs for state preparation decrease.

| *Potential Energy Surface of H<sub>2* | *Error of the Energy obtained from the Initilize CASCI <br /> and the UCCSD Ansatz for H<sub>2* |
|------------|-------------|
| <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/Initialize%20CASCI%20Ansatz/Image/H2%20PES.png" width="500"> | <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/Initialize%20CASCI%20Ansatz/Image/H2%20Error.png" width="500"> |

| *Potential Energy Surface of LiH* | *Error of the Energy obtained from the Initilize CASCI <br /> and the UCCSD Ansatz for LiH* |
|------------|-------------|
| <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/Initialize%20CASCI%20Ansatz/Image/LiH%20PES.png" width="500"> | <img src="https://github.com/randyshee/Quantum-Chemistry/blob/main/Initialize%20CASCI%20Ansatz/Image/LiH%20Error.png" width="500"> |

Please also check out the [paper by Shende et al.](https://arxiv.org/abs/quant-ph/0406176) for how [Qiskit Initializer](https://qiskit.org/documentation/tutorials/circuits/3_summary_of_quantum_operations.html) 
works and how a state is prepared to a quantum circuit.
