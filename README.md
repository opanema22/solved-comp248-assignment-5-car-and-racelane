Download Link: https://assignmentchef.com/product/solved-comp248-assignment-5-car-and-racelane
<br>
You will create two classes <em>Car</em> and <em>RaceLane</em>. Your main method will go in <em>RaceLane1</em>.

<ol>

 <li>Define a class <em>Car</em>. All of the below properties/methods should be non static.

  <ol>

   <li>A <em>Car</em> should have five private properties: a String for the model of the car (e.g. Toyota Camry), an int location, an int currentSpeed, a boolean movingForward, and an int maxSpeed. The idea is that the location data member stores where on a number line the <em>Car</em> Make sure the number entered is ≥ 0.</li>

  </ol></li>

</ol>




<ol>

 <li>A default constructor.</li>

</ol>




<ol>

 <li>A constructor that takes as input three things: A String for the model, an int maxSpeed, and an int for an initial location. It should set the model of the <em>Car</em>, the max speed, and initial location appropriately based on the input. The constructor should make it so that the <em>movingForward</em> property should always be initially set to be true. The <em>currentSpeed</em> should always be initially set to be 0.</li>

</ol>




<ol>

 <li>Write three methods called <em>getModel()</em>, <em>getDirection()</em>, and <em>getLocation()</em> that let you retrieve the model, movingForward, and location properties respectively.</li>

</ol>




<ol>

 <li>Write a method <em>go()</em> which sets the currentSpeed of the <em>Car</em> object to be the object’s maxSpeed.</li>

</ol>




<ol>

 <li>Write a method <em>stop()</em> which sets the currentSpeed of the <em>Car</em> object to be 0.</li>

</ol>




<ol>

 <li>Write a method <em>turnAround()</em> which changes the boolean variable <em>movingForward</em> to be the opposite of what it was before. That is, if it was true before, it should be false now. If it was false before, it should now be true.</li>

</ol>




<ol>

 <li>Write a method <em>move()</em> which does the following:</li>

 <li>If <em>movingForward</em> is true, then it <em>adds</em> the currentSpeed to the location property.</li>

 <li>If <em>movingForward </em>is false, it <em>subtracts</em> the currentSpeed from the location property.</li>

</ol>




<ol>

 <li>A method <em>toString()</em> which return a string representation of a <em>Car</em> object in the form of the model of the Car, its current speed, its direction and its location.</li>

</ol>

For example, it might return:

“Toyota Camry: Located at 10, facing forward and moving at 5 speed.” or

“Toyota Camry: Located at 3, facing backwards, not moving”




<ol start="2">

 <li>Once you have defined the class, create a new class <em>RaceLane1</em> and add a main method in which you do the following:</li>

</ol>




<ol>

 <li>First create a <em>Scanner</em> object and use it to read (one at a time) 3 values from the user: A String, an initial location, and a maxSpeed. Create a <em>Car</em> with these 3 properties. Recall that you can use the method <em>nextLine()</em> in the <em>Scanner</em> class to read a String.</li>

</ol>




<ol>

 <li>Next, read 3 more values from the user and initialize a second <em>Car</em> object based on that.</li>

</ol>




<ol>

 <li>Call the <em>toString()</em> methods on each <em>Car</em> to check their states.</li>

</ol>




<ol>

 <li>Determine which car is to the left of the other car based on their location (small numbers mean “left” and large numbers mean “right”) Turn the car on the right around (using the <em>turnAround() </em>) method, so that it is facing the car on the left.</li>

</ol>




<ol>

 <li>Call the <em>toString() </em>methods on each Car to check their states.</li>

</ol>




<ol>

 <li>Use the <em>go()</em> method on each car to set their states to that they are moving.</li>

</ol>




<ol>

 <li>Create a loop. At each step of your loop, you should call the<em> move() </em>method on each car. Then call the <em>toString()</em> methods to check their states. Your loop should stop when the Cars collide: That is, when their positions have switched so that the car that was initially on the right is now on the left or they are both in the same location. Your method should then print “Boom!!”</li>

</ol>







Here is a sample output to illustrate the expected behavior of your program.  <u>Note</u>: user input is surrounded by a black rectangle and is in purple.

<em>            </em><strong> </strong>

<strong><u>Part 2</u>  </strong>

Let’s race J

Add the following to the <em>Car</em> class:

<ol>

 <li>Create a new parametrized constructor for the car class that takes only two parameters:</li>

</ol>

the model of the car and its maximum speed. The rest of the fields should be initialized to: location =0, facing forward, and current speed =0




<ol>

 <li>Add a new method <em>accelerate()</em> to the <em>Car</em> When this method is invoked, the speed of the car is incremented by 1. If the car is already going at its maximum speed, then accelerate should not do anything.</li>

</ol>




<ol>

 <li>Add a new method <em>brake()</em> to the <em>Car</em> When this method is invoked, the speed of the car is decremented by 1. If the car is stopped, then brake should not do anything.</li>

</ol>

Once you have updated the <em>Car</em> class, create a new class <em>RaceLane2</em> and add a main method in which you do the following:

<ol start="7">

 <li>Create an array of a user given number of cars. All cars should start from the same position. All cars should be facing the same direction. Different cars have different speeds. The maximum speed of a car ranges from 2 to 7.</li>

</ol>




<ol>

 <li>When the race starts, all cars keeps accelerating to reach their maximum speed.</li>

</ol>




<ol>

 <li>The length of the race track is 100 units. The user specifies how many laps the race consists of.</li>

</ol>




<ol>

 <li>The race track has only 2 lanes. A crash happens when you have three cars at the same location. As long as all cars are still in the first lap (first 100 units), no crashes may happen. Crash detection starts as soon as a car enters the second lap .When a crash is detected, the three cars should be removed from the race and all cars must stop. Then they start accelerating again.</li>

</ol>




<ol>

 <li>You need to develop a loop. All cars keeps racing until three cars finish the race or all cars have crashed.</li>

</ol>




<ol>

 <li>Your program should display the status of each car in every loop iteration.</li>

</ol>




<ol>

 <li>The three winning cars should be displayed at the end.</li>

</ol>




<ol>

 <li><em>Hint</em>: it may be useful to add a Boolean field crashed to keep track of crashed cars.</li>

</ol>




<ol>

 <li>If all cars got crashed, your program should indicate that.</li>

</ol>




Feel free to add fields and/or methods as you see fit to both classes.

Here are2 sample outputs to illustrate the expected behavior of your program.  <strong>Note</strong>: user input is surrounded by a black rectangle and is in purple.







<strong><u>Sample run 1</u></strong><strong>: </strong>Three cars racing, two laps, different speeds no crash







…

….










<strong><u>Sample run 2:</u></strong> 4 cars racing, two laps, a crash between three cars…




…

…




…

…


