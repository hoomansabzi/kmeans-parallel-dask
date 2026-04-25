# Distributed k-Means|| with Dask

A from-scratch, distributed implementation of the scalable k-Means|| (parallel k-Means) clustering algorithm using Python and Dask. 

This project adapts the standard k-Means clustering approach for MapReduce-like architectures, focusing specifically on the scalable initialization procedure described in the paper [*Scalable K-Means++* by Bahmani et al. (2012)](https://arxiv.org/abs/1203.6402). 

**Note:** This implementation is built entirely from the ground up using Dask's distributed computing primitives, intentionally bypassing pre-existing clustering functions in Dask ML or Spark MLlib to demonstrate core distributed systems engineering.

## Features
* **Distributed Initialization:** Implements the $O(\log n)$ k-Means|| initialization method, vastly reducing the number of sequential passes required by standard k-Means++.
* **Cluster Computing Ready:** Built with Dask, allowing the algorithm to scale from a single multi-core laptop to a distributed cluster.
* **Benchmarking:** Includes performance evaluations against standard synthetic and real-world datasets.

## Datasets
The algorithm's performance and scalability were evaluated using mid-to-large scale datasets, including:
* Standard synthetic datasets (via Scikit-learn).
* **RCV1 Dataset:** Real-world text categorization data.
* **KDD Cup 1999:** Network intrusion detection data.

## Installation & Usage

### Prerequisites
Ensure you have Python 3.8+ installed along with Dask and Scikit-learn.

```bash
pip install dask distributed scikit-learn pandas numpy
