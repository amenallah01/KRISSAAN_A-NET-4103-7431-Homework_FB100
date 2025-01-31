Below is a **sample README.md** file that you can use in your GitHub repository to describe this entire lab. It briefly explains the **context** (FB100 dataset), the **objectives** (various network analyses), the **structure** of the code, and **how to run** it. Feel free to adapt the style or content to match your exact project structure.

---

# **README: Network Science and Graph Learning Lab (NET 4103/7431)**

This repository contains all code and documentation for the **Network Science and Graph Learning** lab, which examines the **Facebook100 (FB100)** dataset. The FB100 dataset consists of Facebook friendship networks from 100 U.S. universities, circa 2005.

---

## **1. Overview**

- **Course**: NET 4103/7431 — *Network Science and Graph Learning*  
- **Instructor**: Vincent Gauthier  
- **Dataset**: [Facebook100](https://classroom.github.com/a/jm4seIEs) (or downloadable from [this link](https://partage.imt.fr/index.php/s/iyFWSQPJNmc7AC7)), featuring social networks of U.S. universities, each with attributes like dorm, major, gender, and class year.

**Goals**:  
1. **Social Network Analysis**: Degree distributions, clustering coefficients, density, degree–clustering relationships.  
2. **Assortativity**: Measuring homophily for attributes (student/faculty, dorm, year, major, gender).  
3. **Link Prediction**: Implement and evaluate Common Neighbors, Jaccard, Adamic–Adar.  
4. **Label Propagation**: Recover missing node attributes (dorm, major, gender) using semi-supervised label propagation.  
5. **Community Detection**: Formulate a research question (e.g., “Do students form communities primarily by dorm or year?”) and validate it using Louvain or another algorithm.

---


## **2. Results & Key Observations**

1. **Network Properties**: FB100 networks are generally **sparse**, **highly clustered**, with **heavy-tailed** degree distributions.  
2. **Assortativity**: Some attributes (year, dorm) show moderate to high homophily in certain schools; others (gender) show near-zero.  
3. **Link Prediction**: Common Neighbors, Jaccard, Adamic–Adar all recover edges with varying precision–recall trade-offs, depending on graph density and the fraction of edges removed.  
4. **Label Propagation**: Binary attributes (gender) yield higher accuracy than multi-category dorm or major. The fraction of removed labels and attribute homophily strongly impact success.  
5. **Community Detection**: Attributes like dorm (in small residential schools) or year (in larger universities) align with discovered communities. Modularity reveals moderately distinct clusters, while homogeneity and assortativity clarify whether local or global correlation is stronger.

---

## **3. Contributing & Contact**

- If you find a bug or want to add functionality, feel free to open an **issue** or submit a **pull request**.  
- For course-related questions, contact:  
  - *Vincent Gauthier* (vincent.gauthier@telecom-sudparis.eu)  
- * Krissaan Amen Allah*(amen-allah.krissaan@ens.uvsq.fr)

**License**: This repository is for educational purposes. Check with your instructor or the original assignment guidelines for usage permissions.

---
