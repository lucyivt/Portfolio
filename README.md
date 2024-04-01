# Lucy Villalbos Torres
****
**8-bit CPU**  

Used logisim to create an 8-bit CPU that supports R-type, I-type, jump, and BEQ instructions. The CPU contains a register file with 8 registers. Instruction and data memory were also implemented using RAM components. A control logic unit was necessary to control the selectors attached to the muxes depedning on the type of instruction that was just fetched from the intruction memory. In the circuit below the instruction memory is located on the left and data memory is located on the right. The register file and ALU are located towards the middle.  

![Subject Observer UML](/images/CPU.png)

****
**Scheme Interpreter**  

Developed a functional interpreter in the programming language called Scheme. After integrating arithmetic, lists, variables, functions, and recursion, a "store" was created to hold memory. Garbage collectors are necessary to implement in programming lanuages to get rid of elements that are no longer needed. The garbage collector used the trace and sweep algorithm (depth first search) to traverse through the values in the store and determine which ones to keep. Any item that wasn't visited during the traversal is removed from the store. 

****
**Robotic Autonomous Driving**  

The goal was to make a robot autonomously navigate a roundabout. The lanes of the roundabout were created by placing tape on the floor. Open-source code found on [github]((https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020)) contains code to detect lanes by utilizing openCV. However, the code only works for lanes that don't have any gaps in them. The yellow lanes (shown below) have a gap when entering/exiting the roundabout. To counter this issue, a sign was placed at the entrance of the roundabout to notify the robot when to stop detecting lanes and instead start rotating. I developed code to detect entrance signs by utilizing odometry.

![Subject Observer UML](/images/roundabout.png)
****

**Summer Research**

Embryonic development was simulated using finite element analysis (FEA) to help improve the hypothesis on s-looping, a significant process during the formation of the heart. FEA represents the change in mechanical components (strain, stress, deformation) caused by differential growth. The values are then plotted on an XY graph for analysis. To acquire deformation values along specific regions of the model, a path of nodes is necessary. A path is defined by selecting a series of nodes. Since the software ABAQUS doesn't always create an efficient path, the goal was to create an algorithm that will always find the shortest path between two nodes. 

A cylindrical model was created in Abaqus. A tetrahedral mesh with a quadratic geometric order was applied to the cylindrical model to better represent the complex geometry and bending deformations. Since elements in tetrahedrons vary in size, the edges between nodes were weighted. 

![Subject Observer UML](/images/tet.png)

That being the case, an algorithm using informed search and non-uniform cost was used to find a solution. By extending Dijkstra’s algorithm with a heuristic estimate h(n), the A* search algorithm was used to find the shortest path between two arbitrary nodes. An adjacency matrix represented the node connectivity in the model (dimensions were 9377 x 9377). 
By specifying two arbitrary nodes, the algorithm successfully generated a path. The calculated path is marginally different than the path created by ABAQUS. Especially near the end of the path where the calculated path has a staircase-like formation.  Overall, the calculated path contains more nodes and appears less smooth. 

![Subject Observer UML](/images/cyl.png)