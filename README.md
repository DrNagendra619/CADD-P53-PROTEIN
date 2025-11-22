# CADD-P53-PROTEIN
# 🧬 CADD @ P53 Tumor Suppressor Protein Analysis

## 📝 Overview

This Jupyter Notebook introduces **Computational-Aided Drug Discovery (CADD)** and **Structural Bioinformatics** concepts using the **BioPython** and **RDKit** libraries. The primary focus is on analyzing the structure and sequence of the **P53 tumor suppressor protein** (or its binding partners/complexes, PDB ID: 4RP6) to understand its properties, which is critical for cancer drug development.

The notebook demonstrates fundamental tasks such as fetching protein structures, inspecting their composition, and performing basic sequence analysis (GC content calculation).

## 🚀 Analysis Demonstrations

The notebook executes two main examples, utilizing both BioPython and an RDKit installation setup:

---

### Example 1: Protein Structure Retrieval and Inspection

* **Objective**: To fetch a relevant protein structure from the Protein Data Bank (PDB) and inspect its composition.
* **PDB ID**: **4RP6** (Structure of p53 complexed with a DNA element).
* **Steps**:
    1.  The `Bio.PDB.PDBList` function is used to **download the structure** in `mmCIF` format (`4rp6.cif`).
    2.  `Bio.PDB.MMCIFParser` parses the file into a BioPython `Structure` object.
    3.  The console output confirms the structure contains **1 Model** and **1 Chain**.

---

### Example 2: Sequence Analysis (FASTA)

* **Objective**: To read the FASTA sequence data associated with the PDB entry and compute the GC content.
* **Input File**: Assumes a FASTA file named **`rcsb_pdb_4RP6.fasta`** is available.
* **Steps**:
    1.  `Bio.SeqIO.parse()` reads the sequence data from the FASTA file.
    2.  `Bio.SeqUtils.gc_fraction()` calculates the **GC content** (Guanine-Cytosine ratio) of the sequence.
    3.  The example output shows a GC Content of **0.00%**, which strongly suggests the sequence provided in the FASTA file for this PDB entry is **not a DNA sequence**, but likely a **protein sequence**, as protein sequences lack Guanine (G) and Cytosine (C) bases.

## 🛠️ Requirements

The notebook requires the following Python libraries for successful execution:

```bash
# Core bioinformatics library for structure and sequence handling
!pip install Biopython

# Cheminformatics library for potential future drug molecule analysis
!pip install rdkit
