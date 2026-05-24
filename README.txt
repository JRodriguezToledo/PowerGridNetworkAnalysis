Western US Power Grid
Author: Jorge Rodríguez Toledo

1. OVERVIEW 
This project analyses the Western US Power Grid and reproduces the figures, tables, and numerical results.
The main analysis is implemented in the Jupyter notebook individualProject.ipynb, which loads the power grid graph from an edge list file and computes the 
a full network analysis.
​

2. REQUIREMENTS
To run the notebook and reproduce the results, you need:
A) Python 3.9 or newer. (Python 3.13.5 was used for the results)
B) The following Python packages:
	- networkx
	- numpy
	- pandas
	- matplotlib
	- scipy
	- python-louvain (imported as community / community_louvain)
C) Standard-library modules used (no extra installation needed):
	- collections
	- itertools
	- warnings​
D) Recommended installation steps (inside a virtual environment):
	pip install networkx numpy pandas matplotlib scipy python-louvain

3. INPUT DATA
Place the USpowergrid.txt file in the same directory as individualProject.ipynb​
NOTE: The function load_network(filepath='USpowergrid.txt') assumes this exact filename and relative path.


4. HOW TO RUN THE ANALYSIS
A) Open a terminal in the project folder.
B) Start Jupyter:
	jupyter notebook
C) Open individualProject.ipynb.
D) From the Jupyter menu, select:
	Kernel → Restart & Run All

This executes all sections in order and regenerates all numerical results and figures used in the report.


5. REPRODUCIBILITY
A) Randomness in ER and BA null models, as well as in some community detection and sampling procedures, is controlled with fixed seeds (e.g. seed=42+i).


