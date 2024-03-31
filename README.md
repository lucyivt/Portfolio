# Projects
**8-bit CPU**
Used logisim to create an 8-bit CPU that supports R-type, I-type, jump, and BEQ instructions. The CPU contains a register file with 8 registers. Instruction and data memory were also implemented using RAM components. A control logic unit was necessary to control the selectors attached to the muxes depedning on the type of instruction that was just fetched from the intruction memory. In the circuit below the instruction memory is located on the left and data memory is located on the right. The register file and ALU are located towards the middle.  

![Subject Observer UML](/images/CPU.png)

**Scheme Interpreter**
Developed a functional interpreter in the programming lanuage called Scheme. After integrating arithmetic, lists, variables, functions, and recursion, a "store" was created to hold memory. Garbage collectors are necessary to implement in programming lanuages to get rid of elements that are no longer needed. The garbage collector used the trace and sweep algorithm (depth first search) to traverse through the values in the store and determine which ones to keep. Any item that wasn't visited during the traversal is removed from the store. 

**Robtic Autonomous Driving**
The goal was to make a robot autonomously navigate a roundabout. The lanes of the roundabout were created by placing tape on the floor. Open-source code found on [github]((https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020)) contains code to detect lanes by utilizing openCV. However, the code only works for lanes that don't have any gaps in them. The yellow lanes (shown below) have a gap when entering/exiting the roundabout. To counter this issue, a sign was placed at the entrance of the roundabout to notify the robot when to stop detecting and instead start rotating. I developed code to detect entrance signs by utilizing odometry.

![Subject Observer UML](/images/roundabout.png)


