# Multi-Agent Bug Workflow Automator

Machine learning system that analyzes Jira bug reports and automatically recommends workflow routing and developer skill assignment.

## Problem

Large software teams receive many bug reports. Managers must decide:

- bug difficulty
- which developer should handle it
- how it should move through the workflow

This project uses machine learning to group similar bugs and recommend handling strategies.

## Approach

Pipeline:

1. Load Jira dataset (issues, comments, changelog, issuelinks)
2. Data preprocessing
3. Feature engineering
4. TF-IDF representation of bug descriptions
5. Dimensionality reduction using TruncatedSVD
6. Clustering using:
   - KMeans
   - DBSCAN
   - Hierarchical clustering
7. Cluster evaluation
8. Workflow recommendation using a skill matrix

## Output

The system generates clustered bugs and workflow suggestions.

Example output file:

issues_with_clusters.csv

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- SciPy
- Matplotlib

## Repository Structure

multi-agent-bug-workflow-automator
│
├── notebooks
│   └── bug_triage.ipynb
├── data
├── models
├── outputs
├── requirements.txt
└── README.md
