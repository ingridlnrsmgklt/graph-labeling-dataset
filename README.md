# Graph Labeling Dataset

This repository contains graph datasets in graph6 (.g6) format and computed solutions for several graph labeling problems, including graceful labeling, graceful antimagic labeling, and graceful distance-antimagic labeling.

## Repository Structure

graph/
    graph2.g6
    graph3.g6
    ...

solutions/
    graceful/
    graceful_antimagic/
    graceful_distance-antimagic/

## Data Description

Each .g6 file contains graphs with a fixed number of vertices.

Each CSV file contains the following fields:

- graph_id : graph index  
- g6 : graph6 encoding  
- n : number of vertices  
- m : number of edges  
- status : indicates whether a valid labeling exists (YES/NO)  
- labeling : an example labeling if it exists  

Example entry:

3,BW,3,2,YES,"0:2,1:1,2:0"

## Graph Format

Graphs are stored using the graph6 format, which is a compact representation of simple undirected graphs.

Example of reading graph6 in Python (NetworkX):

import networkx as nx

G = nx.from_graph6_bytes(b'BW')
print(G.nodes())
print(G.edges())

## Notes

- All graphs are simple undirected graphs.
- Some results (e.g., for larger values of n) may still be incomplete.
- The labeling results are obtained through computational methods.

## Author

Ingrid Lenora Simanungkalit

## License

This dataset is provided for academic and research purposes.
