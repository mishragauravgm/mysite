+++
date = "2019-03-30"
draft = false
title = "Protein-Ligand Interaction: SAMBinder"
image="prot_lig_inter.png"
tags = ["project","bioinformatics","ml","protein-ligand"]

+++

# [->SAMbinder<-](https://webs.iiitd.edu.in/raghava/sambinder/index.html)

S-adenosyl-L-methionine (SAM) is one of the essential metabolic cofactor/intermediate which is found in almost every cellular life forms and enzymes. It plays a vital role in various metabolic and regulatory pathways, mainly involved in transfer of various groups (e.g., methyl, aminopropyl, methylene). It is a second widely studied ligand after ATP. SAM is a potential drug target for many diseases such as cancer, Alzheimer's, Parkinson, Epilepsy, Osrteoarthritis and many more. Some of the reported drug targets are Catechol O-methyltransferase, Glycine N-methyltransferase, S-adenosylmethionine synthase isoform type-1, S-adenosylmethionine decarboxylase proenzyme, Cystathionine beta-synthase. 

![image](../sam_new.png)

SAMbinder Major Features
------------------------

*   **[Sequence based module](https://webs.iiitd.edu.in/raghava/sambinder/batch.html)**:This module predict SAM binding residues in a protein from its promary sequence.
*   **[PSSM based Module](https://webs.iiitd.edu.in/raghava/sambinder/submit.html)**: This module utilize evolutionary information (in form of PSSM profile) of a protein to predict SAM binding residues in a protein.
*   **[Peptide Mapping](https://webs.iiitd.edu.in/raghava/sambinder/motif_scan.php)**: This server allow user to predict SAM binding residues in a protein by mapping known peptides that contains SAM interacting central residue.
*   **[Standalone Software](https://webs.iiitd.edu.in/raghava/sambinder/stand.html)**: It has been developed using Python and will be freely available to users.
*   **[Datasets](https://webs.iiitd.edu.in/raghava/sambinder/download.php)**: All datasets used in this study will be available to public.

## More about SAM

S-adenosyl-L-methionine (SAM; SAMe; AdoMet) is an important molecule which plays an important role in various cellular reactions and metabolic pathways. All living organism consists of small molecular weight ligands or cofactors which carries out an important function in some metabolic and regulatory pathways. SAM is one such important cofactor, which was first discovered in year 1952. After ATP, SAM is the second most versatile and widely used small molecule. SAM is conjugate molecule of two ubiquitous biological compound; (i) adenosine moiety of ATP and (ii) amino acid methionine. In summary, it is an important molecule which plays an important role in various cellular reactions and metabolic pathways.

Best of knowledge their is no method that can predict SAM binding sites in a protein sequence. In contrast, number of methods have been developed to predict wide range of ligands (e.g., ATP, GTP, NAD, FAD) interacting residues in a protein. Thus their is a need to develop method which can predict SAM interacting residues in a protein. Major existing methods includes, FINDSITE-metal, CHED, ATPint, ATPbind, TargetATPsite, NsitePred, GTPbinder, NADbinder, FADpred, and IonCom. 

First time, we made a systematic attempt to develop machine learning technique based models for predicting SAM interacting residues in a protein from its amino acid sequence. We used well established techniques commonly used to predict ligand binding sites in a protein, to develop SAMbinder. This server have number of modules to predict SAM binding sites in a protein.




## Model Evaluation
In this study, we used stanadrd procedure for evaluating the performance of our models. First, we divide in traing and validation dataset in ratio of 80% and 20%. All traing and testing is performed on training dataset and final performance of model is evaluated on validation or independent dataset. Following is brief description on evaluation  

*   **Five-fold cross validation**: Five-fold cross technique was performed to evaluate the performance of different models developed in this study. In this technique, dataset is divided into five different sets, out of which four sets are used to train the model and the fifth set is used for testing the performance of the model. This process is repeated five times, therefore, each set is used once for testing. The final performance is reported by averaging the performance obtained on five different sets.

*   **External Validation**: Five-fold validation described above is on internal validation where same data is used for training and testing; model may be over optimized. In order to measure realistic performance of our models, we also perform external valiadtion. In external validation we measure performance of our model developed on training dataset on an validation or independent dataset. As both training and validation dataset donot share sequence. It means datasets used for traing and validation are different so performance is realistic.

*   **Performance Measures**: In this study, we used both threshold dependent as well as threshold independent parameters to evaluate the performance of our models. In case of threshold dependent measures, we used all standard parameters to measure performance it includes sensitivity, specificity, accuracy. Similarly, we used area under curve of ROC to measure overall performance in case of threshold independent measures.


## Algorithm

In last one decade number of methods have been developed for predicting ligand interacting residues in a protein. We used similar approach for developing models for predicting SAM interacting residues. Following are major components of algorithm used in this study for developing model

*   **Machine Learning Techniques**: In this study, machine learning techniques have been used for developing models. Major machine learning techniques used for developing models includes SVM, Random Forest, ExtraTree, KNN, MLP and Ridge classifier. These machine learning technique has been implemented using Python library scikit-learn.

*   **Pattern Size or Window**: In order to develop models using machine learning techniques, we need fixed length vector. We have generated overlapping patterns or segments of window size 17. We also used dummy amino acid "X" at N-terminal and C-terminal to generate patterns for each residue. These patterns were divided in SAM interacting and non-interacting patterns based on status of central of pattern.

*   **Binary Profile**: In order to repersent a patterns of 17 amino acids by a vector to numerical vector, we repersent each amino acid by a vector of dimension 21 (20 type of amino acids and one for dummy amino acid "X"). This vector is known binary profile of dimension 357 (21x17); which is commonly used technique to present a pattern by numbers. Binary profile of SAM interacting and non-interacting is used for developing machine learning techniques based models.

*   **PSSM Profile**: Evolutionary information provides more information then single sequence of a protein. In this study, we generate PSSM profiles for a protein using PSIBLAST software to extract its evolutionary information. This PSSM profile is normalize and generated PSSM profile correspong to patterns of 17 amino acids. Finally, machine learning techniques based models have been developed using PSSM profiles of patterns.

*   **Peptide Mapping**: This is interesting module we introduce in this study, it is a simple concept of mapping known SAM interacting peptides on a protein. We compute propensity of SAM interaction of each pattern of different length. These patterns were mapped on a query protein with their propensity.
