+++
date = "2019-03-30"
draft = false
title = "Protein-Ligand Interaction: SAMBinder"
image="prot_lig_inter.png"
tags = ["project","bioinformatics","ml"]

+++

# SAMbinder

S-adenosyl-L-methionine (SAM) is one of the essential metabolic cofactor/intermediate which is found in almost every cellular life forms and enzymes. It plays a vital role in various metabolic and regulatory pathways, mainly involved in transfer of various groups (e.g., methyl, aminopropyl, methylene). It is a second widely studied ligand after ATP. SAM is a potential drug target for many diseases such as cancer, Alzheimer's, Parkinson, Epilepsy, Osrteoarthritis and many more. Some of the reported drug targets are Catechol O-methyltransferase, Glycine N-methyltransferase, S-adenosylmethionine synthase isoform type-1, S-adenosylmethionine decarboxylase proenzyme, Cystathionine beta-synthase. 

![image](../sam_new.png)

SAMbinder Major Features
------------------------

*   **[Sequence based module](https://webs.iiitd.edu.in/raghava/sambinder/batch.html)**:This module predict SAM binding residues in a protein from its promary sequence.
*   **[PSSM based Module](https://webs.iiitd.edu.in/raghava/sambinder/submit.html)**: This module utilize evolutionary information (in form of PSSM profile) of a protein to predict SAM binding residues in a protein.
*   **[Peptide Mapping](https://webs.iiitd.edu.in/raghava/sambinder/motif_scan.php)**: This server allow user to predict SAM binding residues in a protein by mapping known peptides that contains SAM interacting central residue.
*   **[Standalone Software](https://webs.iiitd.edu.in/raghava/sambinder/stand.html)**: It has been developed using Python and will be freely available to users.
*   **[Datasets](https://webs.iiitd.edu.in/raghava/sambinder/download.php)**: All datasets used in this study will be available to public.


S-adenosyl-L-methionine (SAM; SAMe; AdoMet) is an important molecule which plays an important role in various cellular reactions and metabolic pathways. All living organism consists of small molecular weight ligands or cofactors which carries out an important function in some metabolic and regulatory pathways. SAM is one such important cofactor, which was first discovered in year 1952. After ATP, SAM is the second most versatile and widely used small molecule. SAM is conjugate molecule of two ubiquitous biological compound; (i) adenosine moiety of ATP and (ii) amino acid methionine. In summary, it is an important molecule which plays an important role in various cellular reactions and metabolic pathways.

Best of knowledge their is no method that can predict SAM binding sites in a protein sequence. In contrast, number of methods have been developed to predict wide range of ligands (e.g., ATP, GTP, NAD, FAD) interacting residues in a protein. Thus their is a need to develop method which can predict SAM interacting residues in a protein. Major existing methods includes, FINDSITE-metal, CHED, ATPint, ATPbind, TargetATPsite, NsitePred, GTPbinder, NADbinder, FADpred, and IonCom. 

First time, we made a systematic attempt to develop machine learning technique based models for predicting SAM interacting residues in a protein from its amino acid sequence. We used well established techniques commonly used to predict ligand binding sites in a protein, to develop SAMbinder. This server have number of modules to predict SAM binding sites in a protein.