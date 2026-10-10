# Hyper-Redundant Transformer

Transformer-Based Shape Prediction and Neural Shape Control for Whole-Arm Object Caging with Hyper-Redundant Robots

Repository: https://github.com/chatklaw/Hyper-Redundant-Transformer

## Overview

This repository provides a Python notebook implementing a Transformer-based framework for whole-body shape prediction and neural shape control of hyper-redundant robots. The research pipeline combines environmental feature encoding, Transformer-based backbone prediction, symmetry-preserving shape optimization, and neural shape control to study geometric object caging in constrained environments.

Experiments use an idealized two-dimensional kinematic simulation. This implementation is intended for academic research and reproducibility.

## Repository Contents

- Robot_FINAL.ipynb: notebook containing the proposed framework and simulation experiments.

## Recommended: Run in Google Colab

1. Open https://colab.research.google.com/
2. Choose File > Open notebook > GitHub.
3. Paste https://github.com/chatklaw/Hyper-Redundant-Transformer
4. Select Robot_FINAL.ipynb.
5. Choose Runtime > Change runtime type. Use Python 3; a GPU is recommended if available.
6. Choose Runtime > Run all.

Direct Colab link:
https://colab.research.google.com/github/chatklaw/Hyper-Redundant-Transformer/blob/main/Robot_FINAL.ipynb

Execution time depends on runtime resources and experiment settings.

## Running Locally

Suggested environment (not experimentally verified minimum specifications):

- Operating system: Windows, Linux, or macOS
- Python: 3.10 or newer, subject to notebook compatibility
- RAM: 16 GB or more recommended
- CPU: modern multicore processor
- GPU: optional; CUDA-compatible NVIDIA GPU recommended for accelerated training
- Disk: at least 5 GB free space suggested
- Notebook environment: JupyterLab or Jupyter Notebook

### 1. Clone the repository

git clone https://github.com/chatklaw/Hyper-Redundant-Transformer.git
cd Hyper-Redundant-Transformer

### 2. Create a virtual environment

python -m venv .venv

Activate on Windows:
.venv\Scripts\activate

Activate on Linux/macOS:
source .venv/bin/activate

### 3. Install suggested packages

python -m pip install --upgrade pip
pip install numpy pandas scipy matplotlib torch scikit-learn tqdm jupyterlab

These packages are a provisional starting set, NOT a verified complete requirements list. Inspect the notebook imports and pin tested versions before claiming exact reproducibility. For GPU acceleration, install the PyTorch build appropriate for your CUDA configuration: https://pytorch.org/get-started/locally/

### 4. Launch the notebook

jupyter lab

Open Robot_FINAL.ipynb and execute cells in order. Adapt any Colab-specific operations, Google Drive mounts, and input/output paths for local use.

## Experimental Geometry

- Robot model: planar hyper-redundant robot
- Total links: 50
- Stem links: 38
- Cage links: 12
- Total robot length: 15.0
- Nominal cage radius: 0.6286
- Environment: 2D kinematic simulation

## Methodology

1. Environmental feature encoding represents obstacle and geometric information.
2. Transformer-based shape prediction estimates the desired robot backbone configuration.
3. Symmetry-preserving shape optimization balances symmetry, collision avoidance, smoothness, and task-oriented enclosure.
4. Neural shape control produces robot configuration commands to approximate the target backbone shape.

## Limitations

The implementation is evaluated under idealized two-dimensional kinematic assumptions. Actuator dynamics, contact forces, frictional interactions, and sensing uncertainty are not explicitly modeled. Geometric enclosure does not establish force closure, physically validated transportation, or collision-free whole-body operation. Contact-aware modeling and hardware validation remain future work.

## Reproducibility

Use the same notebook version, simulation settings, random seeds, and evaluation metrics when comparing results. Record Python and package versions, hardware, and runtime configuration. The repository contents should be checked against the specific implementation used for the published experiments.

## Citation

If you use this implementation, please cite the associated manuscript:

Transformer-Based Shape Prediction and Neural Shape Control for Whole-Arm Object Caging with Hyper-Redundant Robots in Dynamic Environments.

Complete bibliographic details will be added when available.

## Authors and Contact

Chatklaw Jareanpon and collaborators.
For questions, please contact the repository maintainer through GitHub.

## License

No license is asserted by this README. Consult the repository's LICENSE file, if provided, for reuse and redistribution permissions.
