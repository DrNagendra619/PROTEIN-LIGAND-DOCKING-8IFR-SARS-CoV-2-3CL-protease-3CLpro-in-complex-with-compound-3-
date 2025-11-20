# PROTEIN-LIGAND-DOCKING-8IFR-SARS-CoV-2-3CL-protease-3CLpro-in-complex-with-compound-3-
PROTEIN LIGAND DOCKING 8IFR = SARS-CoV-2 3CL protease (3CLpro) in complex with compound 3 
# Protein-Ligand Docking Simulation: Interaction Analysis (8IFR and P0O) 🧪🖥️

## Overview

This repository contains the input files, configuration parameters, and results from a **Protein-Ligand Docking** simulation. This specific application of molecular docking was performed to predict the preferred binding pose and affinity score of the small molecule **ligand (P0O)** within the binding pocket of the **protein (PDB ID: 8IFR)**.

The simulation files, including `.pdbqt` and configuration files, suggest the use of **AutoDock Vina** or a related docking software package.

---

## Target System Details

* **Protein Target (Receptor):** PDB ID **8IFR**.
* **Ligand (Small Molecule):** **P0O**.
* **Simulation Goal:** Predict the stable binding conformation and quantify the predicted binding affinity (e.g., in kcal/mol).

---

## Repository Files

This repository is organized into input files necessary for running the simulation and output files containing the results.

### 📥 Input Files (Preparation & Configuration)

| File Name | Format | Description |
| :--- | :--- | :--- |
| `1. 8IFR.pdb` | PDB | Original Protein Data Bank structure file. |
| `2. 8IFR_PROTEIN.pdb` | PDB | Cleaned and prepared protein structure file. |
| `3. P0O_LIGAND.pdb` | PDB | Prepared ligand structure file. |
| `8IFR_PROTEIN.pdbqt` | PDBQT | **Receptor file prepared for AutoDock Vina** (includes charges and atom types). |
| `4. P0O.pdbqt` | PDBQT | **Ligand file prepared for AutoDock Vina** (includes charges and atom types). |
| `config.txt` | Text | **Docking configuration file** specifying the search space (grid box coordinates) and simulation parameters. |
| `8ifr.cif` | CIF | Crystallographic Information File (alternative structure format). |

### 📤 Output Files (Results)

| File Name | Format | Description |
| :--- | :--- | :--- |
| `out.pdb` | PDB | Predicted **best binding pose** of the ligand within the receptor cavity. |
| `out.pdbqt` | PDBQT | **Docking results file** containing all predicted poses and their corresponding **binding affinity scores**. |
| `log.txt` | Text | Log file output from the docking software, detailing the execution steps, command parameters, and final results summary. |

---

## Setup and Analysis

To analyze the predicted interaction, you will need molecular visualization software.

1.  **Dependencies:**
    * **Molecular Viewer:** PyMOL, ChimeraX, or VMD (for visualizing PDB/PDBQT files).
    * **Docking Software (Optional):** AutoDock Vina (if reproducing the simulation).

2.  **Visualization Key:**
    * Load the prepared receptor (`5. 8IFR_PROTEIN.pdbqt`).
    * Load the results (`out.pdbqt`).
    * Examine the predicted **binding pose** (`out.pdb`) and the top **binding affinity score** (found in `log.txt` and `out.pdbqt`) to quantify the strength and location of the interaction.

The search space used in the simulation is defined in `config.txt`. Key parameters determined the location of the binding pocket:

* **Center X/Y/Z:** [Check `config.txt` and fill in coordinates]
* **Size X/Y/Z:** [Check `config.txt` and fill in dimensions]
