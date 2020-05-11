# Predicting co-authorship links between academics with supervised learning using network and attribute information 

Graph databases are becoming more ubiquitous for a variety of applications, particularly due to their ability to map multiple types of relational data. A graph database consists of nodes and edges, where a node represents an object and an edge represents a connection or a relationship between two objects. In many graph databases, such as social networks, edges are continuously being added between nodes that are not connected e.g. due to the formation of friendship connections in social networks. The activity of estimating the likelihood of an edge being formed, or being present, between two edges is called ‘link prediction’. 
 
The link prediction problem can be approached by analyzing the structure/topology of the graph, as well as the individual attributes of the nodes

## Problem setting 

The training dataset available was a graph as well as several features of the nodes (in a json file). The graph G(V,E) is an undirected graph representing a subsection of an academic co-authorship network. The vertices (V) represent the authors in the graph, whereas the edges (E) represent the link between authors vi and vj - if both authors have published a paper together. Each node has an identification number, 
 
The test data is a set of 2000 edges, between two nodes vi and vj. Link prediction aims to assign a probability of the existence of an edge between the two nodes. Therefore, the link prediction can be decomposed into a classification problem, where an edge is either present or absent. Therefore, the aim was to develop a machine learning model that would determine the probability of a link between two nodes in the test data, based on certain key features known for both nodes.  

## Method 

Logistic regression, a supervised learning algorithm, was used as the algorithm for predicting the presence of a link between two nodes. This algorithm was used as it assumes a Bernoulli distribution, which in this problem is attributable as a link can either exist or not. With Logistic regression, the probability of an edge being present between any two nodes (u and v) is determined by the sigmoid function shown below,

![alt text](https://github.com/agmo1993/LinkPrediction/blob/master/equation.JPG "Equation")

Where X is the training data present in this problem, used to train the model, and the weight vector (w) is based on the features used for the model. Moreover, the maximum likelihood estimation was used to find the w which results in the global maximum in the log likelihood function, a measure used to determine how well the function fits the data. Both network topological features, as well as node attributes were considered as features used to train the logistic regression models. The Algorithms used to calculate the network features for each pair of nodes (u,v) are Jaccard Similarity, Resource allocation Index, Preferential attachment, Adamic Adar Index, Number of common neighbors 

## Implementation



