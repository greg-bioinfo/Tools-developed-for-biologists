# Proximity keywords

The objective of this tool is to find other proteins which have the same characteristics as our target protein and which interact with proteins similar to neighboring proteins of our target

The keywords for each protein are taken from UNIPROT and are characterized by nine subgroups : biological process, domain, ligand, post-translational modification, cellular component, developmental stage, disease, molecular function and Technical term.

To compare the keywords of each protein these were encoded according to the method Multihotencoding. The folder “dico_mlb.json” contain a dictionnary with proteins name as keys and and the keywords of their neighbors as value (To avoid storing large matrices filled with 0, only the index of 1 are stored).

The folder “kw_string3.json” contains the keywords of each protein and the folder “bp_string2.json”  contains the biological processes of each protein.

To measure the difference between protein keywords we use the Hamming distance. 
 
## Parameters

As input, the user must enter the name of the protein studied, as well as the number of proteins close to it that he wishes to obtain. He can also specify one or more keywords which must be in the protein keywords.

## Results

As output, a text file will be downloaded with the name, keywords and biological processes of the proteins closest to the protein, classified according to the similarity of their neighbors.

On the notebook the most similar proteins are displayed along with their keywords and those that do not match the target are displayed in red.
