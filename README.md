# Different Means Grouper

The project gives a solution to the problem of creating groups of items depending on how close their averages are. Currently the closeness decision can only be based on a simple t-test and p-value calculation using the items' mean (m), standard deviation (sd) and sample size (n), so these group statistics need to be prepared beforehand. No correction for multiple comparisons possible yet!

The solution (1) generates an adjacency matrix representing the closeness between two items (nodes) as an edge. If two items are not significantly different from each other, there will be an edge between the two nodes representing them, otherwise there will be no edge. Then (2) all cliques (complete sub-graphs) are found in this graph representing the relationships between the items. After (3) the removal of the redundant cliques, (4) the groups are named and their names are added to the original input table. Finally (5) this extended table and a simple summary of the groups are written out into a csv. 

## Prerequisites

The script was developed in Jupyter Lab and was tested with Python 3.6.9. All the necessary libraries can be found in the 1st cell.

## Usage

The main parameters of the script are set up in the 2nd cell.