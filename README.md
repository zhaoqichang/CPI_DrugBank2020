# Datasets
 The datasets used in Section5 of "Biomedical data and deep learning computational models for predicting compound-protein relations".

## Data Explanation

### CPA dataset

We use KIBA for CPA task, which is a large-scale benchmark dataset. For more detailed information of KIBA, please refer to the [DeepDTA article](https://academic.oup.com/bioinformatics/article/34/17/i821/5093245).

### CPI dataset

DrugBank is the most commonly used database for CPI task. We downloaded the version 5.1.5 (released on 2020-01-03) to build the dataset. We deleted some drugs that lacked SMILES sequence or SMILES sequence could not be recognized by RDKit. After brushing, there were 6,655 drugs, 4,294 proteins and 17,511 positive samples in the dataset. We randomlyselected the same number of positive samples from unlabeled compound protein pairs as negative samples.

## Folder

### CPA

* KIBA.txt
Format: CompoundID ProteinID SMILES Amino_acid_sequence affinity

### CPI

* drug_str.txt 
Store the ID of the drug and the corresponding SMILES.
Format: CompoundID SMILES

* protein_str.txt
Store the ID of the protein and the corresponding Amino_acid_sequence.
Format: ProteinID Amino_acid_sequence

* positive.txt
Store the positive samples.
Format: CompoundID ProteinID SMILES Amino_acid_sequence 1

* negative.txt
Store the negative samples.
Format: CompoundID ProteinID SMILES Amino_acid_sequence 0

* drug_target_pairs.txt
Store the positive interactions.
Format: CompoundID ProteinID
