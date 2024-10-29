# Projects and Research
Lucy Villalobos Torres

****
**[Meal Mate App](https://github.com/lucyivt/MealMate)** 

*Description*: Meal Mate is an app that lets you save recipes and displays key nutrition facts with total calories.

*Audiance*: Individuals whose goals are to eat healthy and keep track of meals (fitness enthusiasts, home cooks, parents, etc.)

 To create a new recipe, the user must include a list of ingredients. The total calories and nutrition facts are then calculated and added to the recipe by calling the API. [Edamam API](https://api.edamam.com/doc/open-api/nutrition-analysis-v1.yaml) was used to get a full analysis of food recipes. The backend was composed of Java Spring Boot with JDBC Template. 

![UI](/Portfolio/images/ui.png)
The app needs user input for the title, ingredients, and image of recipe.

The project followed the MVC design pattern:

- *Model:* Managed database interactions for recipes, ingredients, and nutrients.

- *View:* Developed and tested API requests using Postman. Used React for the UI.

- *Controllers:* Handled API endpoints for user and recipe functionalities.

- *Services:* Defined CRUD operations and managed the app's business logic.

I worked collaboratively with four other team members to create Meal Mate. We used Trello to distribute the workload by creating tickets. I developed the Ingredient DAO, Recipe Service Layer, testing, and overall organization of the code. 



****
**Developing a Framework for Soft Robot Simulators**

 Differentiable Programming for Physical Simulation (difftaichi) allows optimization efficiency with brute-force gradient descent. We replaced gradient descent with Covariance Matrix Adaptation Evolutionary Strategy (CMA-ES). CMA-ES was designed to optimize single-objective optimization of continuous spaces. It models the sampling distributions of the population as a multivariate normal distribution N(m, C). Where m is the distribution mean vector and C is the covariance matrix. 

The results of optimizing the loss function with CMA-ES are shown in the graphs provided below.
 
![CMA-ES versus gradient descent](images/Figure_2.png)
The median loss functions after 100 evaluations for CMA-ES (green) and gradient descent (yellow) along with their 25th and 75th percentile values. The x-axis shows the number of evaluations and the y axis represents the loss values.
![Whiskerplot](images/Figure_3.png)
The boxplot displays the results of conducting a Mann-Whitney U Test. It shows the median and quartiles at evaluation 100 for CMA-ES and gradient descent. The median value for CMA-ES is -0.539 and for gradient descent, it's -0.502. The p-value was obtained by a two-tailed test and had a value of less than 0.001. The four stars at the top of the boxplot represent the p-value.

****
**8-bit CPU**  

During my Computer Organization course, I utilized logisim to create an 8-bit CPU that supports a variety of MIPS instructions such as R-type, I-type, jump, and BEQ. The instructions support arthmitic, if-statements, and while-loops. 

I also implemented a control logic unit which was necessary to control the selectors attached to the multiplexors. The control logic unit takes in the first 5 bits of the instruction and outputs the type of the current instruction by selecting either 0 or 1 on the multiplexor. The instruction is fetched from the intruction memory.

Instruction and data memory were implemented using RAM components.Logisim has the functionality to take in MIPS assembly code into it's RAM components which is how instructions are fed to the CPU.

In the circuit below the instruction memory is located on the left and data memory is located on the right. The register file and ALU are located in the middle.  

![Subject Observer UML](/Portfolio/images/CPU.png)

****
**Robotic Autonomous Driving**  

The goal of this project was to make a robot autonomously navigate a roundabout. The type of robot was the Turtlebot3 burger which runs on a raspberry pi that contains ROS. 

The lanes of the roundabout were created by placing green and yellow tape on the floor. Open-source code found on this [github page]((https://github.com/ROBOTIS-GIT/turtlebot3_autorace_2020)) contains code to detect lanes by utilizing openCV. The code was designed only for lanes that don't have any gaps in them. 

However, when the robot enters or exits the roundabout, the yellow lanes have a gap. Whenever the robot would get to the entrance of the roundabout it would get confused and drive off course. 

To counter this issue, a sign was placed at the entrance of the roundabout to notify the robot when to stop detecting lanes and instead when to start rotating in the correct direction. To detect the entrance sign, I developed code utilizing odometry. 

![Subject Observer UML](/Portfolio/images/roundabout.png)

****
