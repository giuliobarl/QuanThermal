# Quantum Computing for Thermal Science

This repository contains codes related to the publication "**Notes on Quantum Computing for Thermal Science**" (https://arxiv.org/abs/2503.19109). This document explores the potential of quantum computing for solving linear systems of interest in engineering. In particular, we focus on heat conduction as a paradigmatic example in thermal science.

![Quantum Computing for Thermal Science](https://github.com/giuliobarl/QuanThermal/blob/main/images/quantherm.png "Quantum Computing for Thermal Science")

March 2025 - Pietro Asinari, Nada Alghamdi, Paolo De Angelis, Giulio Barletta, Giovanni Trezza, Marina Provenzano, Matteo Maria Piredda, Matteo Fasano, Eliodoro Chiavazzo.

Original scripts written by Pietro Asinari, adapted as notebooks by Giulio Barletta.

## List of contents

- [Getting started](#getting-started)
- [Qiskit folder overview](#qiskit-folder-overview)

## Getting started

### Prerequisites

Make sure you have the following installed:

- [Git](https://git-scm.com/)

- [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main) or [Anaconda](https://www.anaconda.com/)

### Clone the GitHub repository

```bash
git clone https://github.com/giuliobarl/QuanThermal
cd QuanThermal
```

### Create a virtual environment

```bash
conda create --name qiskit-env python==3.11
```

### Activate the virtual environment

```bash
conda activate qiskit-env
```

### Install the dependencies

```bash
pip install -r requirements.txt
```

Even though you're using Conda, pip is used here because requirements.txt is a pip-formatted file.

Tip: You can install both conda and pip packages in the same environment, but it's best to install as many packages via conda as possible (for compatibility and performance), and use pip for the rest.

## Qiskit folder overview

This folder contains Jupyter notebooks demonstrating quantum computing algorithms using Qiskit. The aim is to explore quantum computing algorithms — especially VQE — for solving problems in heat conduction and thermal science, as well as illustrate physical analogies and competitive dynamics using quantum circuits.

### `VQE-example_v15.ipynb`

Implements the Variational Quantum Eigensolver (VQE) to approximate the solution of a linear system derived from the finite-difference discretization of the 1D heat conduction equation.

Key features:

- Constructs a quantum observable mimicking the system matrix for heat transfer.
- Uses VQE to find the ground state (analogous to updated temperature profiles).
- Demonstrates encoding/normalization and de-normalization steps tied to physical temperature fields.
- Relates directly to Sections 3–3.6 of the paper.

Libraries Used:

- `qiskit`
- `matplotlib`, `numpy`, `scipy`, `statistics`, `time`

### `two-athletes_v01.ipynb`

Illustrates quantum modeling of strategic competition between two agents (athletes) as described in Appendix A of the paper.

Key features:

- Each athlete's strategy is encoded as a quantum state.
- Simulates the outcomes using unitary operations and measurement statistics.
- Shows how quantum superposition and entanglement can capture correlated strategic behavior (e.g., collaboration, competition).
- Acts as a pedagogical analogy for quantum entanglement in decision-making.
- Corresponds to Appendix A of the paper ("*Two-athlete strategy*").

Libraries Used:

- `qiskit`
- `numpy`

### `real-data-loader_v06.ipynb`

Implements a recursive divide-and-conquer algorithm to prepare a quantum state that encodes a real-valued probability distribution:

- Based on the method by [Araujo et al.](https://www.nature.com/articles/s41598-021-85474-1)
- Computes a set of RY rotation angles to load real classical data into a quantum amplitude-encoded state.
- Executes the circuit and compares simulated measurement results with the original distribution.
- Corresponds to Appendix D of the paper ("*Real data loading/encoding*").

Libraries Used:

- `qiskit`
- `numpy`