# interact_keyword

When a biologist seeks to understand the impact of a protein on a biological process, it may be interesting to visualize the interaction 
between the protein studied and proteins known to intervene in this biological process.

This tool takes 3 parameters as input: The name of the protein studied, the keywords that we want to find in the biological processes of proteins and The number
of proteins that we want to display on the graph.

The database used for protein interactions comes from the STRING database human interactome that contains 17000 proteins and 300 000 interactions. The edges of this graph 
are stored in the file "edges_string.txt".

The biological processes of each protein were retrieved using the Quick go API, and stored in the file "bp_string.json" as a dictionary.
The biological processes are stored in the form of go term and will be translated thanks to the file "go-basic.obo"  by the library goatools.

To find the proteins which contain the keywords in their biological process and which are closer to the studied protein I used node2vec.
Node2vec makes it possible to vectorize proteins according to their interactions and to calculate the proximity between 2 proteins.

The output of this program is a graph in PNG format with a red node for the studied protein, blue nodes for the proteins containing the keyword and green nodes for 
the intermediate proteins. The size of the nodes is proportional to the proximity of the protein to the studied protein.
A text file is also created containing the names of the proteins as well as their biological processes and their molecular functions.
