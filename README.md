# Network Science and Graph Learning Project

## Overview

This project involves analyzing social networks from the Facebook100 dataset. The tasks include:
1. Social Network Analysis
2. Assortativity Analysis
3. Link Prediction
4. Label Propagation
5. Community Detection

## Tasks and Code

### 1. Social Network Analysis
- **Degree Distribution**: Analyze the degree distribution of networks.
- **Clustering and Density**: Compute global and local clustering coefficients and network density.
- **Degree vs. Local Clustering Coefficient**: Scatter plot of degree vs. local clustering coefficient.

### 2. Assortativity Analysis
- **Load Data**: Load the FB100 dataset.
- **Compute Assortativity**: Calculate assortativity based on attributes like student_fac, major, vertex degree, dorm, and gender.
- **Plot Results**: Visualize the results using scatter plots and density plots.

### 3. Link Prediction
- **Abstract Base Class**: Define an abstract base class for link prediction.
- **Common Neighbors, Jaccard Coefficient, Adamic/Adar Index**: Implement these link prediction methods.
- **Evaluate Link Prediction**: Evaluate the link prediction methods by removing a fraction of edges and computing precision, recall, and top@k.

### 4. Label Propagation
- **Label Propagation Algorithm**: Implement a semi-supervised label propagation algorithm to predict missing labels.
- **Test Algorithm**: Test the algorithm on the Facebook100 dataset by removing a fraction of labels and measuring accuracy, F1-score, etc.

### 5. Community Detection
- **Research Question**: Formulate a research question about community formation based on dorm assignments or other attributes.
- **Louvain Algorithm**: Use the Louvain algorithm for community detection.
- **Analyze Communities**: Analyze the detected communities and correlate them with node attributes like dorm, major, or year.

## Running the Code

1. **Setup**: Ensure you have the required libraries installed (e.g., NetworkX, Matplotlib, Seaborn, Scikit-learn).
2. **Load Data**: Place the FB100 dataset files in the `data/` directory.
3. **Run Notebooks**: Execute the Jupyter notebooks to perform the analyses and visualize the results.

## Conclusion

The project provides insights into the structure and properties of social networks, including degree distribution, clustering, assortativity, link prediction, and community detection. The results highlight the influence of attributes like dorm, major, and year on community formation and network structure.

## References

- [NetworkX Documentation](https://networkx.github.io/documentation/stable/)
- [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
