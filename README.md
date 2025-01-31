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

## **2. Repository Structure**

```
├── data/
│   ├── Caltech36.gml
│   ├── MIT8.gml
│   ├── JohnsHopkins55.gml
│   └── ... (other FB100 .gml files)
├── notebooks/
│   ├── 01_degree_distribution.ipynb
│   ├── 02_assortativity_analysis.ipynb
│   ├── 03_link_prediction.ipynb
│   ├── 04_label_propagation.ipynb
│   └── 05_community_detection.ipynb
├── src/
│   ├── link_prediction.py          # Classes for CommonNeighbors, Jaccard, Adamic–Adar
│   ├── label_propagation.py        # Semi-supervised label propagation
│   ├── community_analysis.py       # Louvain + homogeneity/modularity/assortativity
│   └── utils.py                    # Helper functions (loading data, etc.)
├── README.md
└── requirements.txt
```

**Key Directories**:
- **data/**: Contains GML files for the FB100 networks you’re analyzing.  
- **notebooks/**: Jupyter notebooks demonstrating each step of the lab.  
- **src/**: Python modules with your implementation of link prediction, label propagation, and community detection analyses.

---

## **3. Setup & Installation**

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YourUsername/fb100-lab.git
   cd fb100-lab
   ```
2. **Install dependencies** (e.g., using `pip`):
   ```bash
   pip install -r requirements.txt
   ```
   - Make sure you have *NetworkX*, *numpy*, *matplotlib*, *seaborn*, and any other libraries (e.g., *python-louvain* for community detection).

3. **Download FB100 data**  
   - Place `.gml` files (like `Caltech36.gml`, `MIT8.gml`) inside `data/`.

---

## **4. Running the Analysis**

### 4.1 From Notebooks

1. **Degree Distributions & Clustering (Question 2)**  
   - Open `notebooks/01_degree_distribution.ipynb`.  
   - Execute the cells to compute and plot degree distributions, clustering coefficients, edge density, etc.

2. **Assortativity (Question 3)**  
   - Open `notebooks/02_assortativity_analysis.ipynb`.  
   - Run the code to calculate assortativity for attributes (dorm, year, major, etc.) across multiple networks.

3. **Link Prediction (Question 4)**  
   - In `notebooks/03_link_prediction.ipynb`, you can remove fractions of edges, compute metrics (Common Neighbors, Jaccard, Adamic–Adar), and evaluate precision/recall at k.

4. **Label Propagation (Question 5)**  
   - `notebooks/04_label_propagation.ipynb` shows how you remove 10%, 20%, or 30% of node attributes and propagate labels using a semi-supervised approach, measuring accuracy, MAE, or F1-score.

5. **Community Detection (Question 6)**  
   - `notebooks/05_community_detection.ipynb` loads specific networks (Caltech, MIT, etc.), applies Louvain or another algorithm, and compares discovered communities to node attributes (dorm vs. year). This addresses the research question about which attribute best explains community structure.

### 4.2 From Command Line

- You can also run Python scripts directly from the `src/` folder (e.g., `python src/link_prediction.py`) if you’ve organized them to accept command-line arguments.

---

## **5. Results & Key Observations**

1. **Network Properties**: FB100 networks are generally **sparse**, **highly clustered**, with **heavy-tailed** degree distributions.  
2. **Assortativity**: Some attributes (year, dorm) show moderate to high homophily in certain schools; others (gender) show near-zero.  
3. **Link Prediction**: Common Neighbors, Jaccard, Adamic–Adar all recover edges with varying precision–recall trade-offs, depending on graph density and the fraction of edges removed.  
4. **Label Propagation**: Binary attributes (gender) yield higher accuracy than multi-category dorm or major. The fraction of removed labels and attribute homophily strongly impact success.  
5. **Community Detection**: Attributes like dorm (in small residential schools) or year (in larger universities) align with discovered communities. Modularity reveals moderately distinct clusters, while homogeneity and assortativity clarify whether local or global correlation is stronger.

---

## **6. Contributing & Contact**

- If you find a bug or want to add functionality, feel free to open an **issue** or submit a **pull request**.  
- For course-related questions, contact:  
  - *Vincent Gauthier* (vincent.gauthier@telecom-sudparis.eu)  
- *Special Thanks* to Prof. Aaron Clauset and Prof. Mason A. Porter for providing the original adapted problems.

**License**: This repository is for educational purposes. Check with your instructor or the original assignment guidelines for usage permissions.

---
