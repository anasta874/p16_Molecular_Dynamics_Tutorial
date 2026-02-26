# p16 Molecular Dynamics Tutorial

A step-by-step educational tutorial for performing and analyzing a 200 ns molecular dynamics (MD) simulation of the small tumor suppressor protein p16 (CDKN2A, 156 amino acids) using GROMACS.  

The relatively small size of p16 makes it well suited for educational molecular dynamics workflows and trajectory analysis.

Designed for students learning molecular dynamics workflows and structural bioinformatics.

---

## Repository Structure

```text
.
├── Tutorial_part_1
│   ├── p16_Tutorial_1_ENG.pdf
│   ├── pdb1a5e.ent
│   └── russo1998.pdf
└── Tutorial_part_2
    ├── DSSP
    │   ├── P48L_H83Y_dssp.dat
    │   ├── R131P_G55C_dssp.dat
    │   ├── WT_dssp.dat
    │   ├── notebooks
    │   │   └── plots
    │   │       ├── sse_comparison_all.png
    │   │       └── sse_horizontal_line_comparison_2x_with_legend.png
    │   └── sse_P16.ipynb
    ├── Last-frame+Mutants_pdb
    │   ├── last_WT.pdb
    │   ├── p16_p48l_h83y.pdb
    │   └── p16_r131p_g55c.pdb
    ├── Maestro_mutagenesis_ENG.pdf
    ├── Prolif
    │   ├── P16_prolif.ipynb
    │   └── P16_prolif+results.ipynb
    ├── VMD_movi
    │   ├── P16_R131P_G55C.mp4
    │   └── P16_WT.mp4
    ├── p16_Tutorial_2_ENG.pdf
    └── p16_Tutorial_2+results_ENG.pdf
```
## Contents

### Tutorial Part 1 — MD Simulation Pipeline
**p16_Tutorial_1_ENG.pdf**

Complete 200 ns GROMACS workflow:

- Topology generation (pdb2gmx)
- Solvation and ion addition
- Energy minimization
- NVT and NPT equilibration
- 200 ns production MD
- PBC correction and trajectory centering
- Final frame extraction

Includes:
- `pdb1a5e.ent` — NMR structure of human p16 (PDB ID: 1A5E; MODEL 1 used by default in GROMACS).
- `russo1998.pdf` — Russo et al., *Nature* (1998), structural basis for inhibition of Cdk6 by the tumor suppressor p16INK4a

---

### Tutorial Part 2 — Trajectory Analysis
**p16_Tutorial_2_ENG.pdf**

Comparative analysis of WT and mutants:

- RMSD, RMSF, Radius of Gyration
- Energy stability analysis
- Hydrogen bonds
- DSSP secondary structure
- PCA (PC1–PC2, PC1–PC3)
- ProLif interaction analysis
- VMD visualization

Includes results in:
`p16_Tutorial_2+results_ENG.pdf`

---

## Mutations Studied

- P48L + H83Y  
- R131P + G55C  

All systems undergo the same standardized 200 ns MD pipeline.

---

## Data Availability

Full 200 ns production trajectories (WT and mutants) are available on Zenodo:

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18367796.svg)](https://doi.org/10.5281/zenodo.18367796)

Total dataset size: ~44.7 GB.

---

## Software

### Core Software

- GROMACS (version 2024 or newer)
- xmgrace
- VMD
- mkdssp

### DSSP Analysis Environment

- Python ≥ 3.9
- NumPy
- Pandas
- Matplotlib

### ProLif Analysis (separate environment recommended)

- Python ≥ 3.9
- MDAnalysis ≥ 2.4
- ProLif ≥ 2.0
- RDKit
- NumPy
- Pandas
- tqdm

---

## Educational Purpose

This repository demonstrates a complete and reproducible molecular dynamics workflow for teaching purposes in computational biology and molecular modeling.
