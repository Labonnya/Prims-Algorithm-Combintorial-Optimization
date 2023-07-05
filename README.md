# Combintorial-Optimization

This code implements Prim's algorithm to find the Minimum Spanning Tree (MST) of a given graph. The graph is represented as a 2D array `graph` with V vertices, where V is defined as a constant `V`. 

The `selectMinVertex` function is used to find the vertex with the minimum value from the `value` array that is not yet included in the MST. It returns the index of the selected vertex.

The `findMST` function performs the main steps of Prim's algorithm. It initializes an array `parent` to store the MST, a vector `value` to keep track of the minimum edge weights, and a vector `setMST` to indicate whether a vertex is included in the MST or not. Initially, all values in `value` are set to `INT_MAX` to represent infinity, and all values in `setMST` are set to `false`.

The algorithm starts with node 0 as the starting point. It sets `parent[0]` to -1 and `value[0]` to 0. Then, it iteratively selects the minimum value vertex from the `value` array using `selectMinVertex` and includes it in the MST by setting the corresponding index in `setMST` to `true`. 

For each selected vertex `U`, it relaxes the adjacent vertices `j` that are not yet included in the MST. If there is an edge from `U` to `j`, and `j` is not in the MST, and the edge weight is smaller than the current value of `value[j]`, it updates `value[j]` with the edge weight and sets `parent[j]` to `U`.

Finally, the code prints the MST by iterating over the `parent` array and displaying the edges from `parent[i]` to `i` along with their weights.

The main function initializes a sample graph represented by the `graph` 2D array and calls the `findMST` function to find and print the MST of the graph.
