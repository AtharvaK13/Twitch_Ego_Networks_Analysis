# Twitch_Ego_Networks_Analysis
Analysis of the ego-nets of Twitch users for graph classification.  

This project aims to classify users based on their ego networks. The ego networks are graphs, which connect a user with other twitch users.  

## Dataset
The dataset used for this project is publicly available at https://chrsmrrs.github.io/datasets/docs/datasets/ as twitch_Egos  

## Code files
The file descriptions are listed below.
* Preprocessing_dataset.ipynb : This notebook was used to preprocess the dataset. The available dataset needed to be converted into csv format to make it more flexible and interchangable into graph representations.
* The graphs were generated using the CSV file and the networkx library.
* Traditional_ML_Models : This notebook contains the implementation used to classify the graphs using traditional machine learining models such as Random Forest, SVM and Logistic Regression. The features used for these models were:
   * Densities, Number of nodes and number of edges
  * Weisfeiler_Lehman Kernels
   * Feather Graph Embeddings and
   * Graph2Vec Embeddings.
* GCN_Implementation.ipynb : This notebook contains the implementation of a Graph Convolutional Network created using the pytorch-Geometric Library. The features used as an input to the GCN were:
   * Closeness and Betweenness Centralities
   * GraphWave to obtain node embeddings
   * Role2vec
* GAT_Implementation.ipynb :  This notebook contains the implementation of a Graph Attention Network. The features used as input were similar to the GCN.
