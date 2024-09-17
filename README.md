# Conformational Heterogeneity Scanner #

This Python script performs structural alignment of two PDB files and calculates the Root Mean Square Fluctuation (RMSF) between corresponding C-alpha atoms. It uses the Biopython library for PDB parsing and superposition, and generates an Excel file and a plot visualizing the RMSF values. So, at its core it does

## "PDB Structure Alignment and RMSF Analysis" ##

This tool currently is limited to ONLY utilizing PDBs with a SINGLE CHAIN ##

## Requirements

- Python 3.x
- Biopython (`pip install biopython`)
- pandas (`pip install pandas`)
- openpyxl (`pip install openpyxl`)
- matplotlib (`pip install matplotlib`)

## Usage

1.  **Upload PDB files:** The script will prompt you to upload two PDB files:
    *   **Reference PDB file:** The structure to which the target structure will be aligned.
    *   **Target PDB file:** The structure to be aligned.
2.  **Alignment:** The script aligns the target structure to the reference structure based on their C-alpha atoms using the `align_structures` function.
3.  **Distance Calculation:** The `calculate_distances` function computes the Euclidean distances between corresponding C-alpha atoms in the aligned structures.
4.  **Output:**
    *   An Excel file (`temp_PDB_RMSF.xlsx`) is generated, containing the reference residue ID, aligned residue ID, and the distance between their C-alpha atoms.
    *   A scatter plot (`temp_PDB_RMSF_plot.png`) is created, visualizing the RMSF values against the residue IDs.

## Note

This script is designed to run in a Jupyter notebook environment (e.g., Google Colab) and utilizes the `google.colab.files` module for file uploads. 

The script focuses specifically on C-alpha atoms for alignment and distance calculation. Ensure that your PDB files contain C-alpha atom coordinates.
