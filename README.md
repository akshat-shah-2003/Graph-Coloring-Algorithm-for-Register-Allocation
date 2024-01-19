# Graph-Coloring-Algorithm-for-Register-Allocation 

##Team Members
- Dhanashree Dharpure ([Dhanshree0802](https://github.com/Dhanshree0802))
- Mrunmayee Kurhade ([mrunmayeek25](https://github.com/mrunmayeek25))
- Akshat Shah ([akshatS2003](https://github.com/akshatS2003))
- Pranav Rathi([pvrPranavRathi](https://github.com/pvrPranavRathi))

When translating a program written in a high-level language (like C or Java) to machine code,the compiler must assign storage locations (registers) to variables. However, a limited number ofregisters are available, and some variables might need to share the same register without causingconflicts. The goal is to efficiently allocate registers for variables in a computer program during compilation using a graph coloring algorithm.

To perform register allocation via graph coloring, there are 4 steps:

● Step 1: Compute the Live Ranges of the virtual registers defined in a basic block

● Step 2: Construct the Interference Graph

● Step 3: Allocate physical registers to the virtual registers using graph coloring approach

● Step 4: If the register allocation is successful, then return, else go for register spilling.


There is a scope for improvement in terms of optimizing the number of registers used and reducing the cost of spilling registers to memory. To get an optimal allocation of colors we train the Deep Learning (DL) network which is based on several layers of Long-Short TermMemory (LSTM) that output a color for each node of the graph. However, the current network may allocate the same color to the nodes connected by an edge resulting in an invalid coloring.To solve this, a Color Correction algorithm is used.


Explanation of the Code:
This code demonstrates the implementation of a neural network-based graph coloring algorithm and includes a color correction phase. Here's a brief summary about the code:

● The program starts by generating a random graph using the rnd_graph function, where the graph has 'n' nodes, and the probability 'p' determines the likelihood of edge creation between nodes. The optimal coloring of the graph is then computed using theopt_coloring function, which employs a greedy algorithm to assign colors to nodes based on their degrees.

● Following that, a simple neural network is trained using a gradient descent algorithm. The network has an input layer with 'n' nodes, a hidden layer with 128 neurons, and an output layer with 'n' nodes. The training involves iterating through the dataset for a specified number of epochs, calculating the mean squared error loss, and adjusting the network's weights and biases to minimize the loss.

● After the neural network training, the code attempts to correct any conflicts in the coloring by introducing a color correction phase. This involves checking for conflicts in the graph and assigning new colors to conflicting nodes.

● The code concludes with the visualization of the colored graph using Matplotlib, where each node is represented as a circle, and edges are plotted between connected nodes. The color of each node reflects the result of the optimal coloring.

● The get_colored_nodes function extracts a dictionary containing the colored nodes from the optimal coloring result, and this dictionary is printed for further analysis. Overall, the code integrates graph theory concepts, neural network training, and visualization to address the graph coloring problem


Output Screenshots of the code:

![Screenshot 2024-01-19 171639](https://github.com/pvrPranavRathi/Graph-Coloring-Algorithm-for-Register-Allocation/assets/99244980/f1654b21-ab7b-47f7-ba2e-e261f6f6153e)
![Screenshot 2024-01-19 171629](https://github.com/pvrPranavRathi/Graph-Coloring-Algorithm-for-Register-Allocation/assets/99244980/8bffea38-cd69-44e5-b616-b3e5e9f95619)
![Screenshot 2024-01-19 171622](https://github.com/pvrPranavRathi/Graph-Coloring-Algorithm-for-Register-Allocation/assets/99244980/5eaf7009-e965-40f4-b654-ad55a1a9db26)
