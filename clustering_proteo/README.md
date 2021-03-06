# Clustering the proteomic data

## Clustering dataset of protein can be useful to identify different groups with similar proteins. 

Here, the similarity is defined by keywords found on Uniprot, where around 1200 keywords are characterized by nine subgroups : biological process, domain, ligand, post-translational modification, cellular component, developmental stage, disease, molecular function and Technical term. For each protein, none or several keywords are associated. However, the keywords in the “Technical term” subgroup won’t be taken into account (not interesting for the clustering).

Our program uses the KMeans clustering to classify a list of genes into groups according to their keywords. Then, creates a plot using Principal Component Analysis (PCA) to visualize the clusters.

### PARAMETERS

#### Clustering_proteo tool
In the file "liste_proteines.txt", enter your proteins’ list (with Uniprot identifiers)
At the beginning of the program file, two parameters have to be define :
nb_cluster : enter the wanted number of clusters. Notice : to select the right number of cluster
top : enter the number of the most important keywords for each cluster

#### Clustering_proteo2 tool
The parameters nb_cluster and top don’t change between both programs, however this tool is used to visualize, for instance, proteins upregulated AND downregulated in the same plot. 
For that, write in the “liste_proteines_down.txt” file all your downregulated proteins, and in the “liste_proteines_up.txt” file all your upregulated proteins (with Uniprot identifiers). After performing the KMeans clustering, the PCA will plot the different clusters with different types of dots depending on whether the protein is up- ( or downregulated (x).


















