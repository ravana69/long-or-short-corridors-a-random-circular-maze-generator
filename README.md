# Long or short corridors? A random circular maze generator

A Pen created on CodePen.io. Original URL: [https://codepen.io/ccprog/pen/rNPoNxP](https://codepen.io/ccprog/pen/rNPoNxP).

The maze is generated with one of three choosable [algorithms](https://en.wikipedia.org/wiki/Maze_generation_algorithm):

- **Depth first** has a low branching factor and contain many long corridors,
- **Prim's algorithm** generates a minimal spanning tree with corridors and connections as short as possible,
-  **Wilson's algorithm** of loop-erased walks generates an unbiased sample from the uniform distribution over all mazes.

The spanning tree is recorded while walking by linking each step to the next. From that, walks from one point in the tree to another can be easily reconstructed to find the solution.

Fun detail: the walls are actually full circles and lines. The removed segments are realized with a complex `stroke-dasharray`.