# Projects
Lucy Villalobos Torres

****
**[Meal App](https://github.com/lucyivt/MealMate)** 

Developed an app that enables users to save recipes and displays key nutrition facts with total calories.

![UI](/Portfolio/images/ui.png)
Users can personalize each recipe by providing a custom title, specifying the ingredients, and adding their own image.

The project followed the MVC design pattern:

- *Model:* Managed database interactions for recipes, ingredients, and nutrients.

- *View:* Developed and tested API requests using Postman. Used React for the UI.

- *Controllers:* Handled API endpoints for user and recipe functionalities.

- *Services:* Defined CRUD operations and managed the app's business logic.

Worked collaboratively with a four-person team, using Trello to organize tasks and manage workload through tickets. I was responsible for developing the Ingredient DAO, building the Recipe service layer, writing tests, and helping maintain overall code organization.

****
**8-bit CPU**  

Utilized logisim to create an 8-bit CPU that supports arthmitic, if-statements, and while-loops. 

Implemented a control logic unit which was necessary to control the selectors attached to the multiplexors. The control logic unit takes in the first 5 bits of the instruction and outputs the type of the current instruction by selecting either 0 or 1 on the multiplexor. The instruction is fetched from the intruction memory.

Instruction and data memory were implemented using RAM components. Logisim has the functionality to take in MIPS assembly code into it's RAM components which is how instructions are fed to the CPU.

In the circuit below the instruction memory is located on the left and data memory is located on the right. The register file and ALU are located in the middle.  

![Subject Observer UML](/Portfolio/images/CPU.png)

****
**Robotic Autonomous Driving**  

The project aimed to have a TurtleBot3 Burger robot autonomously navigate a roundabout, using a Raspberry Pi with ROS. 

The lanes of the roundabout were created by placing green and yellow tape on the floor. Open-source code found on this [github page]((https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020)) contains code to detect lanes by utilizing openCV. The code was designed only for lanes that don't have any gaps in them. 

However, when the robot enters or exits the roundabout, the yellow lanes have a gap. Whenever the robot would get to the entrance of the roundabout it would get confused and drive off course. 

To counter this issue, a sign was placed at the entrance of the roundabout to notify the robot when to stop detecting lanes and instead when to start rotating in the correct direction. To detect the entrance sign, I developed code utilizing odometry. 

![Subject Observer UML](/Portfolio/images/roundabout.png)

****
