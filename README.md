# Quick-Union--Disjoint-set
Time Complexity
Union-find Constructor	Find	Union	Connected
Time Complexity	O(N)O(N)	O(N)O(N)	O(N)O(N)	O(N)O(N)

Note: NN is the number of vertices in the graph. In the worst-case scenario, the number of operations to get the root vertex will be HH where HH is the height of the tree. Because this implementation does not always point the root of the shorter tree to the root of the taller tree, HH can be at most NN when the tree forms a linked list.

The same as in the quick find implementation, when initializing a union-find constructor, we need to create an array of size NN with the values equal to the corresponding array indices; this requires linear time.
For the find operation, in the worst-case scenario, we need to traverse every vertex to find the root for the input vertex. The maximum number of operations to get the root vertex would be no more than the tree's height, so it will take O(N)O(N) time.
The union operation consists of two find operations which (only in the worst-case) will take O(N)O(N) time, and two constant time operations, including the equality check and updating the array value at a given index. Therefore, the union operation also costs O(N)O(N) in the worst-case.
The connected operation also takes O(N)O(N) time in the worst-case since it involves two find calls.
Space Complexity
We need O(N)O(N) space to store the array of size NN.
