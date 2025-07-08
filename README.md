# Quantum Computing for Thermal Science

This repository contains codes related to the publication "**Notes on Quantum Computing for Thermal Science**" (https://arxiv.org/abs/2503.19109). This document explores the potential of quantum computing for solving linear systems of interest in engineering. In particular, we focus on heat conduction as a paradigmatic example in thermal science.

![Quantum Computing for Thermal Science](https://github.com/giuliobarl/QuanThermal/blob/main/images/quantherm.png "Quantum Computing for Thermal Science")

March 2025 - Pietro Asinari, Nada Alghamdi, Paolo De Angelis, Giulio Barletta, Giovanni Trezza, Marina Provenzano, Matteo Maria Piredda, Matteo Fasano, Eliodoro Chiavazzo.

Original scripts written by Pietro Asinari, adapted as notebooks by Giulio Barletta.

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
