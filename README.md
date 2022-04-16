# Clifford VQE

In quantum chemistry application, the problem of finding the minimum eigenvalue of a matrix is very crucial, as it can be used to correspond to the minimum eigenvalue of a Hermitian matrix characterizing the molecule's ground state energy.

Although the quantum phase estimation algorithm may be used to find the minimum eigenvalue, Its implementation on useful problems requires circuit depths exceeding the limits of quantum hardware available in the NISQ era. Alternatively, in 2014, Peruzzo et al. proposed VQE to estimate the ground state energy of a molecule using much shallower circuits. VQE uses a variational technique to find the minimum eigenvalue of the Hamiltonian H of a given system. A VQE requires defining two algorithmic components: a trial state (ansatz), and a classical optimizer. The ansatz is varied by the optimizer via its set of parameters, such that it optimizes towards a state, as determined by the parameters applied to the variational form, that will result in the minimum expected value being measured of the input operator or Hamiltonian.

In this tutorial, a H2 molecule's ground state energy (Hartree) is calculated for a range of atomic bond lengths (Angstrom) using a Variational Quantum Eigensolver (VQE), where it is implemented using CAFQA; a Clifford Ansatz For Quantum Accuracy approach presented in G. S. Ravi et al., CAFQA: Clifford Ansatz For Quantum Accuracy. arXiv, 2022.

The CAFQA is implemented against the conventional HF approach and a CXs Clifford example. They are all compared to the FCI which is considered to give the exact energy values and used as the base to measure the other approaches' performances. OpenFermion and Braket SDK were used among other packages during the implementation of the algorithm.
