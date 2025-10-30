# A-Pan-cancer-in-silico-study-KRAS-mutation.
molecular docking and molecular dynamics simulation 
# Overview
KRAS mutations are among the most common oncogenic alterations in human cancers, including pancreatic, colorectal, and lung carcinomas. These mutations lead to constitutive activation of KRAS signaling, resulting in uncontrolled cell proliferation.  
This project focuses on identifying potential inhibitors of wild-type and mutant KRAS proteins (G12C, G12D, G12V, and G12R) through **molecular docking** and **molecular dynamics (MD) simulations** using an **FDA-approved drug library**.

# Project Objectives
- Retrieve and prepare KRAS wild-type and mutant protein structures.  
- Perform virtual screening using an FDA-approved ligand library.  
- Identify high-affinity inhibitors through molecular docking using PyRx (AutoDock Vina).  
- Evaluate the stability and conformational behavior of top complexes via GROMACS-based molecular dynamics simulation.

# Methodology

# 1. *Protein and Ligand Preparation*
- **Protein Source:** RCSB Protein Data Bank.  
- **Mutants Studied:** G12C, G12D, G12V, Q61H, and Wild-Type KRAS.  
- Protein structures were cleaned (removal of water and heteroatoms) and optimized using **PyMOL**.  
- **Ligand Library:** FDA-approved drug dataset retrieved from **DrugBank / ZINC / PubChem**.  
- All ligands were energy minimized using PyRx prior to docking.

# 2. *Molecular Docking*
- Docking was performed using **PyRx** (AutoDock Vina engine).  
- The **grid box** was defined around the conserved binding pocket region.  
- All ligands were screened against each KRAS mutant and wild-type structure.  
- Binding affinities (kcal/mol) and interaction residues were analyzed using **Discovery Studio Visualizer** and **PyMOL**.  
- The top-ranked ligands were shortlisted for molecular dynamics simulations.

#3. *Molecular Dynamics Simulations*
- Conducted using **GROMACS 2024** to assess complex stability.  
- **Force Field:** CHARMM36  
- **Ligand Parameters:** Generated via **CGenFF**.  
- **Simulation Duration:** 100 ns for each complex under NPT conditions (300 K, 1 bar).  
- **Key Analyses Performed:**
  - RMSD (Root Mean Square Deviation)  
  - RMSF (Root Mean Square Fluctuation)  
  - Rg (Radius of Gyration)  
  - SASA (Solvent Accessible Surface Area)  
  - Hydrogen Bond Analysis  

#Results
Molecular docking studies were performed for the wild-type KRAS and four oncogenic mutants (G12C, G12D, G12V, and Q61H) using an FDA-approved ligand library.  
Comparative binding affinity analysis revealed that several compounds exhibited **stronger binding interactions with the mutant forms of KRAS** compared to the wild-type protein.

The wild-type KRAS served as a **reference (control)** to validate mutant-specific interactions.  
As expected, **binding affinities in the wild-type KRAS were relatively lower**, indicating **reduced ligand accommodation within its native binding pocket**.  
In contrast, the **mutant KRAS variants demonstrated enhanced binding scores and additional stabilizing interactions**, likely due to **structural rearrangements and altered pocket conformations** 

MD simulation analyses further supported these findings:
- The mutant–ligand complexes maintained **stable conformations** throughout 100 ns trajectories.  
- RMSD and RMSF profiles indicated **minimal fluctuations** and **robust structural stability** in mutant complexes.  
- Hydrogen bond occupancy and SASA patterns confirmed **consistent ligand engagement** with the active site residues.  
- The wild-type complex showed comparatively **weaker interaction persistence** and **higher dynamic deviation**.

Collectively, these results suggest that **KRAS mutations enhance drug-binding potential** by reshaping the binding pocket environment, supporting the feasibility of **mutation-selective inhibitor design**.

#Conclusion
This in silico study successfully identified potential inhibitors for KRAS mutants using an FDA-approved ligand library.  
The combined molecular docking and simulation approach provided insights into the **binding stability** and **dynamic behavior** of KRAS–ligand interactions.  
Further **experimental validation** and **structure–activity optimization** are recommended to advance these findings toward clinical applicability.

Tools and Software Used

FDA-approved Drug Library – Used as the ligand dataset for virtual screening; contains clinically validated small molecules.

PyRx (AutoDock Vina) – Used to perform molecular docking and evaluate binding affinities across KRAS mutants and the wild-type protein.

Discovery Studio Visualizer – Used for analyzing docking results, examining hydrogen bond interactions, and visualizing the active binding pockets.

GROMACS 2024 – Utilized for molecular dynamics (MD) simulations to analyze the structural stability and conformational behavior of protein–ligand complexes over time.


Contact For any queries or contributions, please reach out via GitHub Issues or email kavyashreev003@gmail.com
