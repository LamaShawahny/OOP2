
# Directed Weighted Graph - Assignment 2
====================================================================

![image](https://user-images.githubusercontent.com/74476764/146073024-e2fe4f91-cb05-403d-9115-0cbd6098e3f2.png)


Task:
------
Creating and Implementing Directed Weighted Graph Theory in Java.

Design:
-------
The project has 2 main classes 

#### directed_weighted_graph Class

This class represents a directed weighted graph
that can contain a very large amount of vertices and for that, it is necessary to maintain efficient running time.
To do so we need data structures where all vertices can be accessed efficiently. 
Therefore, the appropriate data structure for performing operations on a very large list of nodes is HashMap. 
1.HashMap for nodes 
2.HashMap for edges where the key is String that contains the src and dest of the edge ...

methods:
getNode-Return vertex by key ,complexity O(1)
getEdge -Return edge between 2 vertices - performed by checking the existence of one vertex in the list of neighbors .
addNode -Adding (to each HashMap) is in complexity O(1).
addEdge .
connect - connects an edge with weight w between node src to dest .
nodeIter , edgeIter- Iterators for nodes and edges in class.
edgeIter(node_id)-Iterator for edges getting out of given node .
removeNode , removeEdge  in complexity O(1).
getters of nodesize ,edgeSize ,getMc.

#### DWG_Algo :
This class represents the algorithms of Graph Theory (directed weighted graph).
Some of the algorithms implemented using dijkstra algorithm.
```
. Dikstra Algorithm loop:
   * As long as there are any unvisited vertices:
   * Mark the X vertex as visited. (current vertex. In the first iteration this is the vertex of the source S)
   * For each vertex Y which is a neighbor of X and we have not yet visited it:
        Y is updated so that its distance is equal to the minimum value between two values: between its current distance,
        and the weight of the edge connecting X and Y plus the distance between S and X.
   * Select a new vertex X as the vertex whose distance from the source S is the shortest (at this point) from all the
     vertices in the graph we have not yet visited.
 The algorithm ends when the new vertex X is the destination or (to find all the fastest paths) when we have visited all the vertices.

Complexity of this algorithm is : O(v+e) where v=vertices, e=edges of the graph.
```

The Main  functions  performed:
init : Initializes the class .
copy: Deep copy to graph - In this method the implementation made using copy constructor on directed_weighted_graph Class.
Check if the graph is connected- in this function we used BFS Algorithm.
 shortest path :A function that returns the length of the  shortest path.
shortestPathDist: It returns the vertices of the shortest path,In this function we used the dijkstra algorithm.
tsp :Computes a list of consecutive nodes which go over all the nodes in cities.
Save the graph as to an json file.
Load the graph from an json file.







#### Sources:
-------------------------------------

1). https://github.com/matiassingers/awesome-readme

5).  Assignment 0 

  
