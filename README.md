<div align="center">
  <a href="https://github.com/mnsh0409/Quantum-Workshop-QGSS"><img src="asset/quantum1.jpg" height="500" width="500" /></a
</div>

# QGSS 2025 Quantum Workshop
Quantum Computation Challenge (Lab 1~4)
=======

<div align="left">
Qiskit Global Summer School: The Past, Present and Future of Quantum Computing

# Launch on qBraid

qBraid is an official Jupyter Lab cloud platform host for the Qiskit Global Summer School this year. Follow our quick tutorial [here](https://docs.qbraid.com/lab/user-guide/qgss-2025) to get started with no set-up, installations, or hassle.

To open the QGSS files, labs, and resources directly on qBraid, click this button:

[<img src="https://qbraid-static.s3.amazonaws.com/logos/Launch_on_qBraid_white.png" width="150">](https://account.qbraid.com/?gitHubUrl=https://github.com/qiskit-community/qgss-2025.git&api=v2)


Welcome to the official repository for the **Qiskit Global Summer School 2025 Quantum Workshop**. This repository contains all the labs, exercises, and supplementary materials you'll need to participate in the workshop.

## 🚀 Getting Started

To get started with the labs, you'll need to set up your environment.

### Prerequisites

* **Python 3.10+**
* **Jupyter Notebook or JupyterLab**
* An **IBM Quantum account** for running exercises on real quantum hardware.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd quantum-workshop-qgss
    ```

2.  **Install the required Python packages:**
    We recommend creating a virtual environment to avoid conflicts with other projects.
    ```bash
    python -m venv qgss_env
    source qgss_env/bin/activate  # On Windows use `qgss_env\Scripts\activate`
    pip install -r requirements.txt
    ```
    The labs typically require Qiskit SDK, Qiskit Runtime, Rustworkx, Pandas, yfinance, and `qc-grader`. You can install them using pip:
    ```bash
    pip install -U qiskit qiskit-ibm-runtime rustworkx qiskit-aer qiskit_ibm_catalog yfinance pandas "qc-grader[qiskit,jupyter] @ git+[https://github.com/qiskit-community/Quantum-Challenge-Grader.git](https://github.com/qiskit-community/Quantum-Challenge-Grader.git)"
    ```
    > **Note:** The `pyscf` library, used in Lab 3, can sometimes be challenging to install with `pip` on Windows. If you encounter issues, we recommend installing it via Conda: `conda install -c conda-forge pyscf`.
    
3.  **Set up your IBM Quantum account:**
    For labs that require access to IBM Quantum hardware or to grade your solutions, you will need an IBM Quantum API key and CRN. Follow the instructions in `lab0.ipynb` to save your account credentials. **Remember to never commit your API key directly to a public repository.**


## 📂 Repository Structure

The workshop is divided into several lab sections:

* **/lab-0 to /lab-4:** Core labs covering fundamental concepts of quantum computing with Qiskit.
* **/functions-labs:** A special track featuring labs from our partners, demonstrating the power of Qiskit Functions for solving real-world problems.
* **/community-labs:** Labs and projects created by the QGSS community.

## 🔬 Labs Overview

### Core Labs

* **Lab 0: Getting Started with Qiskit:** An introduction to the basic elements of Qiskit and quantum circuits.
* **Lab 1: Quantum Principles & Dynamic Circuits:** Explore fundamental quantum phenomena like superposition and entanglement, and learn how to use dynamic circuits for advanced algorithms.
* **Lab 2: Mitigating Errors with ZNE:** Learn about quantum noise and apply Zero-Noise Extrapolation (ZNE) to improve the accuracy of your results.
* **Lab 3: Simulating Chemistry with FF-SIM:** Dive into quantum chemistry by simulating molecular Hamiltonians.
* **Lab 4: Quantum Error Correction:** An introduction to the principles of protecting quantum information from errors using codes like the Steane and Toric codes.

* `lab0.ipynb`: Introduction to Qiskit, setting up the environment, and generating GHZ states.
* `lab1.ipynb`: Recreating famous quantum experiments (double-slit, Schrödinger's Cat, CHSH game, quantum teleportation).
* `lab2.ipynb`: Understanding and mitigating quantum noise in QAOA for Max-cut problems.
* `lab3.ipynb`: Quantum chemistry simulations using Sample-based Quantum Diagonalization (SQD) and improving ansatzes.
* `lab4.ipynb`: Quantum Error Correction (QEC) concepts, decoders, and advanced QEC codes.
* `utils.py`: Helper functions used across various labs (e.g., for plotting, ZNE).
* `lab4_util.py`: Helper functions specific to Lab 4 (e.g., for QEC code visualization, matrix rank).
* `backend_target_v20.pkl`: Pre-computed data file for Lab 3 (e.g., Hamiltonian matrix).
* `backend_target_v21.pkl`: Pre-computed data file for Lab 3 (e.g., Overlap matrix).
* `N2_device_bitarray.npy`: Pre-computed data file for Lab 3 (e.g., N2 configuration bitarray).
* `grumpy.png`: Image asset for Lab 1.
* `happy.png`: Image asset for Lab 1.
* `Supplemental_long_range_entanglement_with_limited_qubit_connectivity.ipynb`: Supplemental notebook for Lab 1.

### Qiskit Functions Labs

This track showcases how to solve complex problems using high-level abstractions without needing to manage the underlying quantum hardware details. These labs are provided by our industry partners.

**Partner Labs:**

* **Algorithmiq:** Tensor-Network Error Mitigation (TEM).
* **ColibriTD:** Solving partial differential equations with QUICK-PDE.
* **Global Data Quantum:** Quantum Portfolio Optimization.
* **Kipu Quantum:** Iskay Quantum Optimizer for QUBO and HUBO problems.
* **Multiverse Computing:** Singularity Machine Learning for classification tasks.
* **Q-CTRL:** Performance management for error suppression.
* **QEDMA:** Quantum Error Suppression and Error Mitigation (QESEM).
* **Qunova:** Handover Iterative VQE (HI-VQE) for chemistry simulations.

* `functions-labs/`: Directory containing labs for Qiskit Functions.
    * `algorithmiq/algorithmiq_tensor-network_error_mitigation (TEM).ipynb`: Lab on Tensor-Network Error Mitigation.
    * `colibri-td/colibritd_quick-pde.ipynb`: Lab on solving PDEs with QUICK-PDE.
    * `global-data-quantum/gdq_quantum_portfolio_optimizer.ipynb`: Lab on quantum portfolio optimization.
    * `kipu/kipu_iskay_quantum_optimizer.ipynb`: Lab on the Iskay Quantum Optimizer.
    * `multiverse/multiverse_singularity.ipynb`: Lab on Multiverse Singularity.
    * `q-ctrl/q-ctrl_performance_management.ipynb`: Lab on Q-Ctrl Performance Management.
    * `qedma/qedma_qesem.ipynb`: Lab on QEDMA QESEM.
    * `qunova/qunova_hi-vqe.ipynb`: Lab on Qunova Hi-VQE.
* `TEM_lab_validation.py`, `grader.py`, `grader_iskay.py`: Grader scripts for various labs.
* `mnsh0409/quantum-workshop-qgss/Quantum-Workshop-QGSS/*lab*/`: Original workshop files (including PDFs, other language versions, etc.).

---

## Lab Exercises Overview

### Lab 0: Hello Quantum World! 🌍

This introductory lab covers the basics of setting up your Qiskit environment, connecting to IBM Quantum, and running your first quantum circuits.

* **Exercise 1: Design a GHZ state**
    * **Goal:** Create a 3-qubit Greenberger–Horne–Zeilinger (GHZ) state circuit using Hadamard and CNOT gates.
    * **Expected Output:** A quantum circuit diagram showing the GHZ state preparation.
    

* **Exercise 2: Transpile a GHZ state**
    * **Goal:** Transpile the GHZ circuit to adhere to specific qubit connectivity constraints, demonstrating circuit optimization.
    * **Expected Output:** A transpiled circuit diagram showing added SWAP gates or a remapped layout.
    

* **Bonus Challenge: Run GHZ on hardware**
    * **Goal:** Execute the GHZ circuit on a **real IBM Quantum computer** and analyze the results, comparing them to simulator outcomes to observe noise effects.

---

### Lab 1: Recreating famous experiments at home! 🔬

This lab delves into fundamental quantum mechanics concepts like superposition, interference, and entanglement, implementing them with Qiskit.

* **Exercise 1-1 to 1-4: Double-slit Experiment**
    * **Goal:** Construct circuits to model a particle passing through two slits, creating superposition, observing interference on a screen, and introducing phase differences to generate a full interference fringe pattern.
    

* **Exercise 2: Is the cat happy or grumpy?**
    * **Goal:** Simulate Schrödinger's Cat experiment using an $R_X$ gate to create a superposition, then perform a single measurement to determine the cat's "mood."
    

* **Exercise 3: Double-slit with a path detector**
    * **Goal:** Modify the double-slit experiment to include a path detector (measurement), demonstrating how observation affects interference.

* **Exercise 4 & 5: CHSH Game**
    * **Goal:** Implement the quantum strategy for the CHSH game using a Bell state and measurement basis rotations, then calculate win probabilities to demonstrate quantum advantage.
    

* **Exercise 6 & 7: Quantum Teleportation**
    * **Goal:** Construct the complete quantum circuit for teleporting an unknown quantum state using an entangled Bell pair and mid-circuit measurements with conditional operations.
    * **Bonus Challenge:** Implement the teleportation protocol on a **real IBM Quantum backend**, focusing on dynamic circuits and optimizing for long-range entanglement.

---

### Lab 2: Cutting through the noise 📉

This lab focuses on understanding and mitigating quantum noise to obtain accurate results on current quantum computers, using a Max-cut problem solved with QAOA.

* **Exercise 1: Find the best qubits**
    * **Goal:** Analyze hardware properties (T1, T2, gate fidelities, readout errors) of IBM Quantum devices to identify the best-performing qubits and qubit pairs.
    

* **Exercise 2: From Graph to Hamiltonian**
    * **Goal:** Convert a given graph problem (Max-cut) into an Ising Hamiltonian, which serves as the cost function for QAOA.

* **Exercise 3: Error Counting**
    * **Goal:** Estimate the total accumulated error of a quantum circuit by summing errors from single-qubit gates, two-qubit gates, and readout errors for specific backend properties.

* **Exercise 4 & 5: Optimal Layout**
    * **Goal:** Find the optimal qubit layout for a circuit on a given backend by minimizing accumulated two-qubit gate errors through transpiler seed sweeps, leveraging Qiskit's transpiler.

* **Exercise 6a: Global Folding**
    * **Goal:** Implement a function to apply global circuit folding for Zero Noise Extrapolation (ZNE), artificially increasing noise across the entire circuit.
* **Exercise 6b: Local Folding**
    * **Goal:** Implement a function to apply local circuit folding, selectively increasing noise around individual gates for ZNE.

* **Bonus Challenge: Scale it up!**
    * **Goal:** Implement and execute a larger Max-cut problem on **IBM Quantum hardware**, applying all learned transpilation and error mitigation techniques (e.g., dynamical decoupling, Pauli twirling, TREX, ZNE) to improve results in a noisy environment.

---

### Lab 3: Quantum Chemistry with SQD 🧪

This lab explores quantum chemistry simulations, focusing on molecular Hamiltonians and the Sample-based Quantum Diagonalization (SQD) algorithm.

* **Exercise 1: Measure the size of the O2 Hamiltonian**
    * **Goal:** Calculate the total number of electron spin configurations for the $O_2$ molecule in a specific basis set (6-31G), illustrating how problem size scales.
    

* **Exercise 2: Flip a bit by configuration recovery**
    * **Goal:** Implement a function to "flip a bit" in a given electron configuration represented as a `BitArray`, a concept used in configuration recovery for noise mitigation.

* **Exercise 3: Change the basis set**
    * **Goal:** Load molecular Hamiltonian and Overlap matrices corresponding to a specific basis set (e.g., STO-3G for $N_2$), which are essential inputs for quantum chemistry simulations.

* **Exercise 4: Select the best layout**
    * **Goal:** Select the best qubit layout for the molecular ansatz on a given backend by minimizing accumulated two-qubit gate errors through transpiler seed sweeps.

* **Exercise 5: Add more interaction to LUCJ ansatz**
    * **Goal:** Modify the variational ansatz (e.g., EfficientSU2) to include more complex interactions (e.g., RZZ gates) based on specific indices, enhancing its expressibility for molecular simulations.
    

* **Bonus: Real hardware execution with error mitigation**
    * **Goal:** Execute the SQD algorithm on **real quantum hardware** to find the ground state energy of a molecule, incorporating various error mitigation techniques (dynamical decoupling, Pauli twirling, TREX, ZNE) to improve accuracy.
    

---

### Lab 4: Quantum Error Correction 🛡️

This lab covers Quantum Error Correction (QEC), from classical foundations to advanced topological codes.

* **Practice: Lookup table-based Decoder of [3,1,3] Code**
    * **Goal:** Complete a lookup table that maps all possible 3-bit received strings to the most likely 1-bit message for the [3,1,3] classical repetition code.

* **Exercise 1: Lookup Table-based Decoder of 3-bit code**
    * **Goal:** Create a lookup table mapping 2-bit syndromes to single-qubit error codes (I, X0, X1, X2) for the 3-qubit bit-flip code.

* **Exercise 2: Lookup table of [[7,1,3]] Steane Code**
    * **Goal:** Create a Python dictionary mapping 6-bit syndromes to single-qubit error codes (I, Xn, Yn, Zn for n=0-6) for the [[7,1,3]] Steane code.

* **Exercise 3: Detect Error with a Lookup Table**
    * **Goal:** Construct a quantum circuit to measure the Steane code stabilizers, initialize it with a given quantum state, and use your lookup table to identify an injected single-qubit error.
    

* **Exercise 4: Find the parity check matrices of the toric code**
    * **Goal:** Determine the $H_X$ (Z-type) and $H_Z$ (X-type) parity check matrices for the 2x2 Toric code, following specific qubit labeling and stabilizer definitions.
    

* **Exercise 5: Find the parity check matrices of the gross code**
    * **Goal:** Determine the $H_X$ (Z-type) and $H_Z$ (X-type) parity check matrices for the [[12,2,4]] Gross code.

* **Exercise 6: Count the number of logicals for the Toric and Gross codes**
    * **Goal:** Calculate the number of logical qubits ($k$) for both the Toric and Gross codes using their parity check matrices and the formula $k = n - \text{rank}(H_X) - \text{rank}(H_Z)$.

### Functions Labs Overview

These labs demonstrate the use of **Qiskit Functions**, which are pre-built, optimized quantum algorithms accessible via the IBM Quantum platform, designed to simplify complex quantum computing workflows.

#### Algorithmiq TEM (Tensor-Network Error Mitigation)

This lab focuses on simulating many-body physics experiments with error mitigation using Algorithmiq's TEM function.

* **Task 1: Build the kicked Ising circuit**
    * **Goal:** Implement a function to construct a quantum circuit representing the time evolution of a state under the transverse kicked Ising Hamiltonian.
* **Task 2: Define the X Pauli observable**
    * **Goal:** Create a function to return the correct `SparsePauliOp` observable to measure the correlation function on a specific qubit.
* **Task 3: Estimate correlation function**
    * **Goal:** Estimate the correlation function for different qubits at a fixed timestep using both `StatevectorEstimator` and `EstimatorV2` with `AerSimulator`.
* **Task 4: Execute different timesteps**
    * **Goal:** Implement a loop to create and run circuits for multiple timesteps, measuring the X observable on each qubit to reproduce a diagonal correlation plot.
    
* **Task 5: Select backend and transpile**
    * **Goal:** Select an appropriate Heron backend and transpile the circuit for it, mapping logical observables to physical qubits.
* **Task 6: Run TEM**
    * **Goal:** Execute the Algorithmiq TEM Qiskit Function on a real QPU, providing the necessary `pubs` and `options`.
* **Task 7: Get the results and compare**
    * **Goal:** Extract and compare the expectation values from statevector simulation, unmitigated hardware runs, and TEM-mitigated results using a bar plot.
    

---

#### ColibriTD QUICK-PDE

This lab demonstrates how to model a flowing non-viscous fluid using the QUICK-PDE function, leveraging ColibriTD's H-DES solver.

* **Exercise 1: Select the physics problem and set the boundary condition**
    * **Goal:** Choose `cfd` as the use case and set initial conditions for the inviscid Burger's equation (e.g., `a=1.0`, `b=1.0`).
* **Exercise 2: Adjust execution parameters**
    * **Goal:** Configure algorithmic parameters like qubit allocation (`t`=2 qubits, `x`=1 qubit), depth (`u`=3), shots (`[500, 2500, 5000, 10000]`), and initialization (`"RANDOM"`) for a specific problem (`a=0.5`, `b=0.25`).
* **Exercise 2.2: Adjust execution parameters (max_iters)**
    * **Goal:** Further refine execution parameters by setting `max_iters` to a list of lower values (`[100, 10, 2, 1]`) to save QPU time.
* **Exercise 3: Process the final output and visualize**
    * **Goal:** Retrieve the solution data (`t_samples`, `x_samples`, `u_functions`) from the job result and visualize the fluid velocity field `u(t,x)` in a 3D plot.
    
    * **Comparison:** Plot and compare the solutions for different initial conditions (`a=1.0, b=1.0` vs. `a=0.5, b=0.25`).
    

---

#### Global Data Quantum Portfolio Optimizer

This lab demonstrates how to use Qiskit’s quantum portfolio optimizer function to solve dynamic portfolio optimization problems.

* **Exercise 1: DPO Job Execution**
    * **Goal:** Perform a portfolio optimization using three financial assets (NVDA, TSLA, AMZN), four time steps, and a 2-bit resolution. Configure the optimizer to execute a total of 70 quantum circuits and apply SQD-based postprocessing.
    * **Goal (Part b):** Retrieve and display key performance metrics (return, Sharpe ratio, deviation from investment restriction, and transaction costs) from the job result.
* **Exercise 2: Resuming Job Execution**
    * **Goal:** Resume a previous optimization job by modifying the number of generations (adding two more) and providing the `previous_session_id` for a warm restart.

---

#### Kipu Iskay Quantum Optimizer

This lab will guide you through using the Kipu Iskay Quantum Optimizer function.
* **Goal:** (Details would be extracted from `kipu_iskay_quantum_optimizer.ipynb`)

---

#### Multiverse Singularity

This lab explores the Multiverse Singularity function.
* **Goal:** (Details would be extracted from `multiverse_singularity.ipynb`)
    

---

#### Q-Ctrl Performance Management

This lab demonstrates performance management using the Q-Ctrl function.
* **Goal:** (Details would be extracted from `q-ctrl_performance_management.ipynb`)

---

#### QEDMA QESEM

This lab focuses on using the QEDMA QESEM function.
* **Goal:** (Details would be extracted from `qedma_qesem.ipynb`)
    
    

---

#### Qunova Hi-VQE

This lab explores the Qunova Hi-VQE function.
* **Goal:** (Details would be extracted from `qunova_hi-vqe.ipynb`)

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
</div>
