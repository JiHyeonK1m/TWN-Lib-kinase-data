# TWN-Lib-kinase-data

**TWN analysis was conducted on a set of 210 human kinases with DFG-in conformations, excluding atypical kinase groups.**

### File Structure

Each kinase directory is organized as follows:

[Kinase Name]  
├── TWN-Pattern   
├── TWN-Pharma    
└── TWN-Region


Topological Water Networks (TWN) can be defined topological ring structures (3-ring, 4-ring, 5-ring, and 6-ring) formed by hydrogen-bonding interactions between water molecules.
These water network patterns reflect the cooperative behavior of water molecules and provide insights into protein–ligand interactions from a novel perspective.

<img width="2000" height="376" alt="image" src="https://github.com/user-attachments/assets/10eda073-fd87-4d71-a643-48e88acb677d" />

The physicochemical properties of water molecules at protein–ligand binding sites have emerged as critical determinants of binding affinity, selectivity, and binding kinetics.

Most existing algorithms require full free energy calculations to analyze binding site water molecules, and their analysis is typically limited to the first hydration layer on the protein surface.
In contrast, TWN enables quantitative analysis of water molecule behavior without requiring free energy calculations and allows integrated consideration of not only surface water but also the second hydration layer within the binding site.

Topological Water Network (TWN) analysis was performed based on molecular dynamics (MD) simulations.
MD simulations were conducted for 10 ns using the GROMACS package (version 5.1) with the CHARMM27 force field and the TIP3P water model.

The analysis was focused on the hinge binding site, which is the primary binding pocket of kinases.

#### TWN Pattern & Region
  - The central point (centroid) of each TWN 4 ring pattern was determined.
  - Patterns with centroids closer than 1Å to each other were considered part of the same group.
  - Each grouped pattern was defined as a TWN region after duplicate removal based on union frequency

#### TWN-Pharma
Based on TWN-Patterns, TWN-Pharma represents the pharmacophore features of the water network.
  - Hydrogen Bond Donor(Cyan)/Acceptor(Magenta), Ring Aromatic(Orange)
  - In TWN-Pattern analysis, O atoms with a Solvent Dipole Order (SDO) ≥ 0.7 are considered forming hydrogen bonds with binding site.

#### CIM
Homepage : https://ccim.cnu.ac.kr/cim/index.do/
