# PROTEIN-LIGAND-DOCKING-8IFR-SARS-CoV-2-3CL-protease-3CLpro-in-complex-with-compound-3-
PROTEIN LIGAND DOCKING 8IFR = SARS-CoV-2 3CL protease (3CLpro) in complex with compound 3 
# Molecular Docking Simulation: Protein-Ligand Interaction (8IFR and P0O) 🧪🖥️

## Overview

This repository contains the input files, configuration parameters, and results from a **Protein-Ligand Docking** simulation. The simulation was performed to predict the preferred binding pose and affinity score of a small molecule **ligand (P0O)** within the binding pocket of the **protein (PDB ID: 8IFR)**.

The primary tool used for this simulation is likely **AutoDock Vina** or a related software, based on the use of `.pdbqt` and configuration files.

---

## Target System Details

* **Protein Target (Receptor):** PDB ID **8IFR** (Found in files: `8IFR.pdb`, `8IFR_PROTEIN.pdb`, `8IFR_PROTEIN.pdbqt`, `8ifr.cif`).
* **Ligand (Small Molecule):** **P0O** (Found in files: `3. P0O_LIGAND.pdb`, `4. P0O.pdbqt`).
* **Methodology:** Molecular Docking (Likely rigid or flexible receptor docking).

---

## Repository Files

This repository is organized into input and output files crucial for reproducing and analyzing the docking results.

### 📥 Input Files (Preparation)

| File Name | Format | Description |
| :--- | :--- | :--- |
| `1. 8IFR.pdb` | PDB | Original PDB structure file for the protein. |
| `2. 8IFR_PROTEIN.pdb` | PDB | Prepared protein structure (cleaned, protonated, etc.). |
| `3. P0O_LIGAND.pdb` | PDB | Prepared ligand structure file. |
| `8ifr.cif` | CIF | Crystallographic Information File for the protein structure (alternative format). |
| `4. P0O.pdbqt` | PDBQT | **Ligand file prepared for AutoDock Vina** (includes charges and atom types). |
| `5. 8IFR_PROTEIN.pdbqt` | PDBQT | **Receptor file prepared for AutoDock Vina** (includes charges and atom types). |
| `config.txt` | Text | **Docking configuration file** specifying the search space (grid box coordinates) and parameters. |

### 📤 Output Files (Results)

| File Name | Format | Description |
| :--- | :--- | :--- |
| `out.pdb` | PDB | Predicted **best binding pose** of the ligand within the receptor cavity. |
| `out.pdbqt` | PDBQT | Docking results file containing all predicted poses and their corresponding **binding affinity scores** (e.g., kcal/mol). |
| `log.txt` | Text | Log file output from the docking software, detailing the execution steps, energy minimization, and final results summary. |

---

## Setup and Analysis

To view and verify the docking results, you will typically need a molecular visualization and analysis tool.

1.  **Dependencies:**
    * **Molecular Viewer:** PyMOL, ChimeraX, or VMD.
    * **Docking Software (Optional):** AutoDock Vina (if re-running the simulation).

2.  **Visualization Steps:**
    * Load the prepared receptor: `5. 8IFR_PROTEIN.pdb` or `5. 8IFR_PROTEIN.pdbqt`.
    * Load the docking result: `out.pdbqt`. The viewer can typically read the various binding poses and scores directly from this file.
    * Examine the **binding affinity score** in the `log.txt` or the `out.pdbqt` file to determine the predicted strength of the protein-ligand interaction.

The `config.txt` file defines the search space. Key parameters from this file are likely:

* **Center X/Y/Z:** [Check `config.txt` and fill in coordinates]
* **Size X/Y/Z:** [Check `config.txt` and fill in dimensions]
* **Exhaustiveness:** [Check `config.txt` and fill in value]
