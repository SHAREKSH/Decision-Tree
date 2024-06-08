# Decision-Tree
Decision Tree in Machine Learning
notebook : https://colab.research.google.com/drive/1bqXl6U1TrXIsNYZG9_38r-tOES_f8p6i?usp=sharing


Decision Tree in Machine Learning
A decision tree is a type of supervised learning algorithm that is commonly used in machine learning to model and predict outcomes based on input data. It is a tree-like structure where each internal node tests on attribute, each branch corresponds to attribute value and each leaf node represents the final decision or prediction. The decision tree algorithm falls under the category of supervised learning. They can be used to solve both regression and classification problems.

Decision Tree Terminologies
There are specialized terms associated with decision trees that denote various components and facets of the tree structure and decision-making procedure. :

#Root Node: A decision tree’s root node, which represents the original choice or feature from which the tree branches, is the highest node.
#Internal Nodes (Decision Nodes): Nodes in the tree whose choices are determined by the values of particular attributes. There are branches on these nodes that go to other nodes.
#Leaf Nodes (Terminal Nodes): The branches’ termini, when choices or forecasts are decided upon. There are no more branches on leaf nodes.
#Branches (Edges): Links between nodes that show how decisions are made in response to particular circumstances.
#Splitting: The process of dividing a node into two or more sub-nodes based on a decision criterion. It involves selecting a feature and a threshold to create subsets of data.
#Parent Node: A node that is split into child nodes. The original node from which a split originates.
#Child Node: Nodes created as a result of a split from a parent node.
#Decision Criterion: The rule or condition used to determine how the data should be split at a decision node. It involves comparing feature values against a threshold.
#Pruning: The process of removing branches or nodes from a decision tree to improve its generalisation and prevent overfitting.

@Attribute Selection Measures
While implementing a Decision tree, the main issue arises that how to select the best attribute for the root node and for sub-nodes. So, to solve such problems there is a technique which is called as Attribute selection measure or ASM. By this measurement, we can easily select the best attribute for the nodes of the tree. There are two popular techniques for ASM, which are:
1.Information Gain
2.Gini Index


1. Information Gain:
Information gain is the measurement of changes in entropy after the segmentation of a dataset based on an attribute.
It calculates how much information a feature provides us about a class.
According to the value of information gain, we split the node and build the decision tree.
A decision tree algorithm always tries to maximize the value of information gain, and a node/attribute having the highest information gain is split first. It can be calculated using the below formula:
Information Gain= Entropy(S)- [(Weighted Avg) *Entropy(each feature)  
Entropy: Entropy is a metric to measure the impurity in a given attribute. It specifies randomness in data. Entropy can be calculated as:

Entropy(s)= -P(yes)log2 P(yes)- P(no) log2 P(no)
Where,

S= Total number of samples
P(yes)= probability of yes
P(no)= probability of no
2. Gini Index:
Gini index is a measure of impurity or purity used while creating a decision tree in the CART(Classification and Regression Tree) algorithm.
An attribute with the low Gini index should be preferred as compared to the high Gini index.
It only creates binary splits, and the CART algorithm uses the Gini index to create binary splits.
Gini index can be calculated using the below formula:
Gini Index= 1- ∑jPj2



