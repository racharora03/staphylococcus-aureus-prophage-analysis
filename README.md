# staphylococcus-aureus-prophage-analysis
Genomic characterization of PVL+ Indian Staphylococcus aureus ST22 clones
# Genomic Characterization of PVL+ Indian Staphylococcus aureus ST22 Clones

## Overview
This repository contains the bioinformatics SOP and analysis results for characterizing Panton-Valentine Leukocidin (PVL)-positive Staphylococcus aureus ST22 clones from Indian hospitals.

## Objectives
1. Determine genomic characteristics of PVL+ Indian Staphylococcus clones
2. Identify genomic location of PVL (lukS-PV/lukF-PV) gene
3. Compare Indian ST22-PVL+ strains with global ST22-MRSA clones

## Sample Information
- 5 S. aureus isolates (IDs: G20253359, G20253360, G20253361, G20253517, G20253518)
- ST22-MRSA clones from Indian hospitals

## Pipeline Summary
- Assembly: GHRU Assembly pipeline / SPAdes
- Annotation: Bakta
- MLST: mlst tool
- Spa Typing: spaTyper
- SCCmec Typing: sccmec tool
- AMR Genes: AMRFinderPlus
- Virulence Genes: ABRicate (VFDB database)
- Prophage Analysis: PHASTEST
- Phylogeny: Snippy → IQ-TREE → Microreact

## Key Findings
- PVL-positive samples: G20253360, G20253517, G20253518
- SCCmec type: IV (multiple subtypes) for PVL+ strains
- Spa types: t1309, t309, t005 identified
- MLST: Sequence types determined via mlst and ARIBA

## Repository Contents
- `scripts/`: All analysis scripts used
- `results/`: Output files from each analysis step
- `data/`: Sample metadata and summary files
- `docs/`: Detailed methods and documentation

## Dependencies
See `requirements.txt` and `environment.yml`

