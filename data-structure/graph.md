# Graph types

### Undirected graph

![alt text](./readme_assets/screenshot_000.png)

### Directed graphs / Digraphs

![alt text](./readme_assets/screenshot_001.png)

### Weighted graphs

![alt text](./readme_assets/screenshot_002.png)

### Tree

![alt text](./readme_assets/screenshot_003.png)

### Rooted tree

![alt text](./readme_assets/screenshot_004.png)

### Directed Acyclic Graphs

![alt text](./readme_assets/screenshot_005.png)

- scheduler, compiler, build system
- shortest paths algorithm
- topological ordering: how to process the nodes of graph so I don't perform a task before having complete all it's dependencies

### Bipartite graph

![alt text](./readme_assets/screenshot_006.png)

- often question to ask is "what is maximum matching on bipartite graph"
- "how many people can be matched to jobs"
- tougher constrains, more conflicts
- play critical role in field of network flow

### Complete graph

![alt text](./readme_assets/screenshot_007.png)

- worst case of graph, because of number of the edges.
- good place for start of testing algorithm efficiency.

# Representing graphs

### Adjacency matrix

![alt text](./readme_assets/screenshot_008.png)
![alt text](./readme_assets/screenshot_009.png)

### Adjacency matrix

- each node tracks all it's edges
  ![alt text](./readme_assets/screenshot_010.png)
  ![alt text](./readme_assets/screenshot_011.png)

### Edge list

![alt text](./readme_assets/screenshot_012.png)
![alt text](./readme_assets/screenshot_013.png)

# Common problems and solutions

![alt text](./readme_assets/screenshot_014.png)

### Shortest path

![alt text](./readme_assets/screenshot_015.png)

- algorithms: BFS, Dijkstra's, Bellman-Ford. Floyd-Warshall, A\*,

### Connectivity

![alt text](./readme_assets/screenshot_016.png)

- typical solution: union find data structure, or any search algorithm (DFS)

### Negative cycles in directed graph

![alt text](./readme_assets/screenshot_017.png)

- algorithms: Bellman-Ford, Floyd-Warshall
- in a context of finding shortest path, negative cycle is sort of a trap that can never be escaped
- good for detecting arbitrage: cycling trough currencies to get more money

### Strongly connected components

![alt text](./readme_assets/screenshot_018.png)

- algorithms: Tarjan's and Kosaraju

### Traveling salesman problem

![alt text](./readme_assets/screenshot_020.png)

- NP problem
- several important applications
- algorithms: Held-Karp, branch and bound, ant colony optimization

### Bridges

![alt text](./readme_assets/screenshot_019.png)

### Articulation points

![alt text](./readme_assets/screenshot_021.png)

### Minimum spanning tree

![alt text](./readme_assets/screenshot_022.png)
![alt text](./readme_assets/screenshot_023.png)
![alt text](./readme_assets/screenshot_024.png)

- algorithms: Kruskal, Prim, Boruvka
- applications: circuit design, transportation networks, designing least cost network

### Max flow trough flow network

![alt text](./readme_assets/screenshot_025.png)

- algorithms: Ford-Fulkerson, Edmonds-Karp, Dinic's

# Algorithms

### DFS

![alt text](./readme_assets/screenshot_026.png)
![https://codeforces.com/blog/entry/68138](./readme_assets/dfs_animation.gif)

- compute a graphs minimum spanning tree
- detect and find cycles in a graph
- check if a graph is bipartite
- find strongly connected components
- topologically sort the nodes of a graph
- find bridghes and articulation points
- find augmenting paths in a flow network
- generate mazes

### BFS

![alt text](./readme_assets/screenshot_027.png)
![38](./readme_assets/bfs_animation.gif)
![alt text](./readme_assets/screenshot_028.png)
![alt text](./readme_assets/screenshot_029.png)
![alt text](./readme_assets/screenshot_030.png)
![alt text](./readme_assets/screenshot_031.png)

### Topological Sort

- the only type of graph which has a valid topological ordering is a Directed Acyclic Graph.
- situations that can be modelled as graph with directed edges, where some events must occur before others: school class prerequisites, program dependencies, event scheduling, assembly instuctions

##### how to

1. find unvisited nodes **A**
2. do DFS from **A** to unvisited nodes
3. on backtrack, add **A** to the end of a topsort list

![alt text](./readme_assets/screenshot_032.png)
![alt text](./readme_assets/screenshot_033.png)
![alt text](./readme_assets/screenshot_034.png)

### Shortest and longest path on Directed Acyclic Graphs

- SSSP - single source shortest path can be solved in O(V+E) with topsort
- relaxing a edge obeding to better value if shortest path can be obtained using current edge
- for longest path multiply all edges with -1, find shortest path, multiply answer by -1

![alt text](./readme_assets/screenshot_035.png)
![alt text](./readme_assets/screenshot_036.png)

### Dijkstra

-
