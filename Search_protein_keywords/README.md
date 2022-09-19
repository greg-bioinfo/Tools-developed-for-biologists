# Representation of the interactions with the closest proteins containing a keyword in their biological process

## Objective

When we study the impact of a protein within a biological pathway, it is interesting to find the close proteins that are involved in this pathway and the interactions that link them to the protein under study.
  
The human interactome used comes from “STRING”, it contains 16948 proteins and 290849 interactions, saved in text format (edges_string.txt).

The biological processes of each protein were retrieved by the QUICKGO API and saved in JSON format (bp_string2.json).

In order to select the closest proteins, the nodes of the graph were transformed into vectors using the “node2vec” library.


## Parameters
The input parameters are the name of the protein studied, the keywords searched for in the biological processes, as well as the number of closest proteins to be selected.


## Results

The final graph represents the shortest path between the starting protein (red) and the closest proteins containing the keyword in their biological processes
(blue). The proteins in green make it possible to understand the indirect interaction between the protein of interest and the targeted proteins. The size of the nodes of the graph represents the similarity of the interactions of the protein with those of the protein of interest.

The program outputs the graph in PNG format, as well as a text file containing the name, biological processes and molecular functions of the proteins in the graph.




















