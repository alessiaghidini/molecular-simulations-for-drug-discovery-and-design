# Hands-on sessions: Molecular Dynamics, Enhanced Sampling and Ligand-Based Methods

**Molecular simulations for drug discovery and design**
A Lorentz Center – CECAM workshop · Bogotá, Colombia · 23–27 November 2026

Material for the two hands-on sessions: Jupyter notebooks that run directly in your browser with Google Colab, with nothing to install.

| Session | Topic | Open in Colab |
|---|---|---|
| 1 | Molecular dynamics and enhanced sampling | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO/blob/main/Session1_MD_enhanced_sampling.ipynb](https://github.com/alessiaghidini/molecular-simulations-for-drug-discovery-and-design/blob/main/MD_enhanced_sampling.ipynb)) |
| 2 | Ligand-based methods | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO/blob/main/Session2_ligand_based.ipynb](https://github.com/alessiaghidini/molecular-simulations-for-drug-discovery-and-design/blob/main/ligand_based.ipynb)) |

---

## Getting started (Google Colab)

You only need a **Google account** and a web browser.

1. Click the **Open in Colab** button of the session.
2. In Colab, click **Copy to Drive** (or **File → Save a copy in Drive**). A copy opens in a new tab: **work in that copy**, so your changes are saved.
3. Run the cells from the top, in order (**Shift + Enter** runs a cell).
4. If Colab disconnects after a long pause, your code is kept but the variables are lost: use **Runtime → Run all** to get back to where you were.

---

## Session 1: Molecular dynamics and enhanced sampling

`Session1_MD_enhanced_sampling.ipynb`

We build a molecular dynamics engine from scratch for a particle in a 1D double-well potential, then use it to understand why free energy calculations need enhanced sampling.

**Part A: Molecular dynamics**
1. A particle in a double-well potential
2. Integrating Newton's equations with Velocity Verlet (NVE), and the role of the time step
3. Adding a thermostat: the Andersen thermostat (NVT)
4. From sampling to free energies: the Boltzmann distribution

**Part B: Enhanced sampling**

5. The rare event problem
6. Setting up umbrella sampling: windows and force constant
7. Running umbrella sampling simulations
8. Reconstructing the potential of mean force (PMF) with WHAM
9. Going further: from the toy model to ligand unbinding

Requires only `numpy` and `matplotlib`. The longest simulations take 1–2 minutes on Colab.

---

## Session 2: Ligand-based methods

`Session2_ligand_based.ipynb`

We predict the water solubility of small molecules from their structure.

1. Molecules to numbers: RDKit, molecular descriptors and data curation
2. Mapping chemical space with principal component analysis (PCA)
3. Predicting solubility with a Random Forest model
4. Improving the model: more descriptors and hyperparameters

Requires `rdkit`, `scikit-learn`, `pandas`, `numpy` and `matplotlib`. On Colab, the first code cell installs RDKit automatically (about 30 seconds); everything else is preinstalled.

**Data:** a subset of the ESOL solubility dataset: J. S. Delaney, *ESOL: Estimating Aqueous Solubility Directly from Molecular Structure*, J. Chem. Inf. Comput. Sci. 2004, 44, 1000–1005. [doi:10.1021/ci034243x](https://pubs.acs.org/doi/10.1021/ci034243x)

---

## Running on your own computer (optional)

If you prefer a local installation, create an environment with conda:

```bash
conda create -n cobo2026 -c conda-forge python=3.11 numpy matplotlib pandas scikit-learn rdkit jupyterlab
conda activate cobo2026
jupyter lab
```

or with pip:

```bash
pip install numpy matplotlib pandas scikit-learn rdkit jupyterlab
```

Note: the package is installed as `scikit-learn` but imported as `sklearn`.

---

## Repository contents

```
├── README.md
├── Session1_MD_enhanced_sampling.ipynb
├── Session2_ligand_based.ipynb
└── solutions/                 (added after the sessions)
```

## Author and license

Prepared by Alessia Ghidini, EPFL, for the workshop *Molecular simulations for drug discovery and design* (Bogotá, 2026).

