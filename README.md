# Power Grid Network Analysis

## Overview
This repository analyzes the **Western US Power Grid** using complex network theory. It loads
the grid as a graph from an edge list and runs a full network analysis — basic descriptors,
clustering, distances, degree statistics, centrality measures, null-model comparisons
(Erdős–Rényi and Barabási–Albert), and community detection — with all calculations and figures
produced in a single reproducible Jupyter notebook. Results are summarized in a final PDF report.

## Repository Structure
This is a flat repository — all files live at the root:

* `PowerGridAnalysis.ipynb` — Jupyter notebook with the complete analysis (data loading through visualization).
* `USpowergrid.txt` — input data: edge list of the Western US Power Grid.
* `FinalReportPowerGridAnalysis.pdf` — final written report with figures, tables, and discussion.
* `requirements.yml` — Conda environment specification (environment name: `complex-networks`).
* `Data_provenance.txt` — source and provenance of the dataset.
* `LICENSE` — MIT License.

The notebook is organized into sections: Load Data, Basic Descriptors, Clustering, Distances,
Degree Statistics, Centrality Measures, Null Models, Community Detection, and Network Visualization.

## Getting Started

### 1. Clone the repository

```
git clone https://github.com/JRodriguezToledo/PowerGridNetworkAnalysis.git
cd PowerGridNetworkAnalysis
```

### 2. Create and activate the environment with Conda

Make sure you have [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or
[Anaconda](https://docs.anaconda.com/anaconda/install/) installed. Create the environment from
`requirements.yml`:

```
conda env create -f requirements.yml
conda activate complex-networks
```

### 3. Run the analysis

The input data (`USpowergrid.txt`) is already included in the repository — no download step is
required. Its provenance is documented in `Data_provenance.txt` (sourced from the
[Netzschleuder](https://networks.skewed.de/net/power) network repository).

Launch Jupyter and open the notebook:

```
jupyter notebook PowerGridAnalysis.ipynb
```

Then run every cell (Kernel → Restart & Run All) to regenerate all numerical results and figures
used in the report. If `jupyter` is not found in the environment, install it first with
`conda install jupyter`.

> **Reproducibility:** randomness in the ER/BA null models and in community-detection sampling is
> controlled with fixed seeds (e.g. `seed=42+i`), so results are deterministic across runs.

## Citation
If you use this repository, please cite as follows:

```
@misc{PowerGridNetworkAnalysis2026,
  author       = {Jorge Rodríguez Toledo},
  title        = {Power Grid Network Analysis},
  year         = {2026},
  howpublished = {\url{https://github.com/JRodriguezToledo/PowerGridNetworkAnalysis}}
}
```

## License
Released under the MIT License — see the [`LICENSE`](LICENSE) file for details.
