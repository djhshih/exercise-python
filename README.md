# Programming Exercises for Python

## Instructions

Please submit your Python scripts (or `.ipynb` files) and PDF (or HTML) outputs
in a zip file. Include only output files specified below.
Do *not* send `.py` files directly because many email servers will block them.  


## Text processing

Allowed dependencies: None  
Required output: tab-delimited file of CDR amino acid sequences  

Using the reference sequence (AA, WithGaps) fasta file from [IMGT][imgt],
implement code to generate extract the CDR1 and CDR2 amino acid sequences 
from each T cell receptor V segment allele from human (Homo sapiens).

A subset of your output tab-delimited table should look like:
```
allele	cdr1	cdr2
TRAV26-1*01	TISGNEY	GLKNN
TRBV14*01	SGHDN	FVKESK
TRBV7-8*01	SGHVS	FQNEAQ
```

[imgt]: https://www.imgt.org/download/GENE-DB/


## Text mining

Allowed dependencies: Any  
Required output: tab-delimited file of PMIDs and titles  

Implement code to perform the following tasks:

1. [Collect][bio-entrez] Pubmed medline abstracts on "medulloblastoma" published by any author
   with surname "Shih" between 2010 and 2020.
   Save the data to disk as a CSV table.

2. Import the CSV table and build a SQLite database.

3. Obtain the PMIDs and titles of publications that mention the *MYC* gene in 
   the abstract.

[bio-entrez]: https://biopython.org/docs/1.76/api/Bio.Entrez.html


## Neural network

Allowed dependencies: Any  
Required output: confusion matrix in which each row is a predicted class  

Construct training and test data from [IMGT nucleotide sequence data][imgt-fasta-nt].
Implement a neural network to predict the species given a nucleotide sequence.


[imgt-fasta-nt]: https://www.imgt.org/download/GENE-DB/IMGTGENEDB-ReferenceSequences.fasta-nt-WithoutGaps-F+ORF+allP

