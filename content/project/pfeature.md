+++
date = "2019-01-27T16:46:17+05:30"
draft = false
title = "Pfeature"
img="protein.jpg"
tags = ["project","ml","bioinformatics"]
+++

Pfeature is a web server for computing wide range of protein and peptides features from their amino acid sequence. Following are main menus for computing features; i) Composition-based features, ii) Binary profile of sequences, iii) evolutionary information based features, iv) structural descriptors,and v) pattern based descriptors, for a group of protein/peptide sequences. Additionally, users will also be able to generate these features for sub-parts of protein/peptide sequences. Pfeature be helpful to annotate structure, function and therapeutic properties of proteins/peptides

![Summary of Functionalities of Pfeature](../pfeature_webpage_banner.png)_

## Major segments of Pfeature

### Compositional Features

This module is desisigned for computing composition based features. These features has been calssified in following five submenus/modules; i) Simple compostions like amino acid, dipeptide, tripeptide; ii) Physico-chemical properties base composition, iii) Measuring repeats and dstribution of amino acids, iv) Shannon entropy to measure complexity in sequence and v) Miscellaneous features frequently used in previous studies like autocorrelation, conjoint triad, composition transition, pseudo amino acid composition and quasi-sequence-order descriptors.

### Binary Profiles

This module is heavily used in annoation of a protein at residue level, for example predicting secondary state of residues, surface accessibility of residues, identification of ligand interacting residues. Generally, overlapping windows are used to create all possible patterns of fixed length from a protein. Then each pattern is converted in binnary profile (1 for presence and 0 for absent) for numerical repersentation of profile. This module/menu have following submenus; i) Amino acid, ii) Dipeptide, iii) atom & bond, iv) residue properties, and v) AAindex.

### Evolutionary Information

It has been shown in past that evolutionay information provides more information then single sequence. In this module evolutionary information is provided in form of PSSM (Position Specific Scoring Matrix) profile. These PSSM profiles are generated using PSIBLAST software. This module/menu allows user to compute following type of features; i) geneartion of PSSM profile from amino acid sequence, ii) Normalization of PSSM profile using different techniques, iii) composition of PSSM, and iv) PSSM profile for whole protein or postion of a protein.

### Structural Features

Modules under this category generate structure based features includes 2D and 3D descriptors, different types of Fingerprints. Also the module generates features in the form of SMILES format using tertiary structure.This kind of features have been heavily used in developing different types of prediction methods and drug designing methods.

### Pattern Generation

In case of residue level annotation one need to genertate all possible patterns of fixed length. This menu is designed to generate different length of patterns from different type of profiles. This module/menus has been divided in following submenus; i) Binary Profile, ii) PSSM profile, iii)Properties, iv) AA Index, and v) universal.


### 

