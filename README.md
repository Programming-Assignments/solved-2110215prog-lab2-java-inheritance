Download Link: https://assignmentchef.com/product/solved-2110215prog-lab2-java-inheritance
<br>
<strong>Lab 2: Java Inheritance </strong>

<strong>Instruction </strong>

<ol>

 <li>Click the provided link on CourseVille to create your own repository.</li>

 <li>Open Eclipse and then “File &gt; new &gt; Java Project” and set project name in this format</li>

</ol>

<strong>2110215_Lab2_2021_1_{ID}_{FIRSTNAME}</strong>

<ul>

 <li>Example:<strong> 2110215_Lab2_</strong>2021<strong>_1_6331234521_Samatcha</strong>.</li>

</ul>

<ol start="3">

 <li>Initialize git in your project directory

  <ul>

   <li>Add .gitignore and set up your git.</li>

  </ul></li>

</ol>

○ Create your remote repository from a given link.

○ Commit and push initial codes to your GitHub repository.

<ol start="4">

 <li>Implement all the classes and methods following the details given in the problem statement file which you can download from CourseVille.

  <ul>

   <li>You should create commits with meaningful messages when you finish each part of your program.</li>

  </ul></li>

</ol>

○ Don’t wait until you finish all features to create a commit.

<ol start="5">

 <li>Test your codes with the provided JUnit test cases, they are inside package <strong>grader</strong>

  <ul>

   <li>If you want to create your own test cases, please put them inside package <strong>student</strong></li>

  </ul></li>

</ol>

○ Aside from passing all test cases, your program must be able to run properly without any runtime errors.

<ol start="6">

 <li>After finishing the program, create a UML diagram and put the result image (UML.png) at the root of your project folder.</li>

 <li>Export your project into a jar file called <strong>Lab2_2021_1_{ID}</strong> and place it at the root directory of your project. Make sure you export all your source (.java) files. You can open the jar file with any zip software to check it.

  <ul>

   <li>Example: <strong>Lab2_2021</strong>_<strong>1_63</strong>3<strong>jar</strong></li>

  </ul></li>

 <li>Push all other commits to your GitHub repository.</li>

 <li>Problem Statement</li>

</ol>

Space is one of the places that we want to go to in our childhood. However, this kind of dream costs us lots of money. Being just a computer geek, we are going to create our own virtual solar system.




<strong>Figure 1: Solar System </strong>

(https://upload.wikimedia.org/wikipedia/commons/thumb/c/cb/Planets2013.svg/2000pxPlanets2013.svg.png)

Our Solar System consists of many planets orbiting around the Sun. For simplicity, we will choose only two planets: <strong>Earth </strong>and <strong>Saturn</strong>. In addition, the orbit will be simple too because the planet can only orbit around these <strong>4 positions</strong> (shown in <strong>Figure 2</strong>) that far away from the Sun defined by orbit radius (each planet may have different orbit radius).




<strong>Figure 2: Orbit System</strong>

However, the Saturn class is still incomplete. So it’s your task to help fulfill our childhood dream.

For better understanding of this, there is a <strong>SolarSystem </strong>class in package <strong>solarsystem </strong>which will provide the real usage of the planets. The document about how to use it is available as <strong>SolarSystem.pdf</strong>.




<ol start="2">

 <li>Implementation Detail</li>

</ol>

The class-package is summarized below

<strong> </strong>

<strong>Figure 4</strong> Class diagram

<strong>You must write java class Saturn from scratch using UML diagram specified above.</strong>

<strong>* In the following class description, only details of IMPORTANT fields and methods are</strong><strong> given. * </strong>

4.1 Package solar

<h1>Class <em>Coordinate </em>/*Fill Code*/</h1>

<em>Field </em>

&#x25aa; <strong>– int x </strong>– The position of axis X. <strong> </strong>

&#x25aa; <strong>– int y </strong>– The position of axis Y.




<em>Constructor </em>

&#x25aa; <strong>+ Coordinate()</strong> – Set related fields with default values (All field will be set to 0).

&#x25aa; <strong>+ Coordinate(int x, int y)</strong> – Set related fields with the given parameters.

<strong> </strong>

<em>Method </em>

&#x25aa; <strong>+ int getX()</strong> – Return the position of axis X.

&#x25aa; <strong>+ int getY()</strong> – Return the position of axis Y.

&#x25aa; <strong>+ void setX(int x)</strong> – Set the position of axis X equals to x.

&#x25aa; <strong>+ void setY(int y)</strong> – Set the position of axis Y equals to y.




<h1>Class <em>Planet </em>/*Fill Code*/</h1>

<em>Field </em>

&#x25aa; <strong># Coordinate coordinate</strong> – The current coordinate of this planet. <strong> </strong>

&#x25aa; <strong># Coordinate orbitCenterCoordinate</strong> – The orbit center coordinate used for orbiting around.

&#x25aa; <strong># int orbitRadius </strong>– The orbit radius of this planet (the distance from the planet’s coordinate to the orbit center coordinate). <strong> </strong>




<em>Constructor </em>

&#x25aa; <strong>+ Planet()</strong> – Set related fields with default values (coordinate will be set to (1,0) which will correspond to orbitRadius with value 1).

&#x25aa; <strong>+ Planet(int orbitRadius)</strong> – Set related fields with the given parameters; note that the orbitRadius must be at least 1.

<strong> </strong>

<em>Method </em>

&#x25aa; <strong>+ Coordinate getCoordinate()</strong> – Return current coordinate.

&#x25aa; <strong>+ Coordinate getOrbitCenterCoordinate()</strong> – Return orbit center coordinate.

&#x25aa; <strong>+ int getOrbitRadius()</strong> – Return the orbit radius.

&#x25aa; <strong>+ boolean orbit()</strong> – Return true if the orbit can occur. The planet will orbit only to 4 positions (far from center with orbit radius) clockwisely around the center. Otherwise, return false.




<h1>Class <em>Earth </em>/*Fill Code*/</h1>

<em>Field </em>

&#x25aa; <strong>– int wasteLevel</strong> – The Earth’s waste level.




<em>Constructor </em>

&#x25aa; <strong>+ Earth()</strong> – Set related fields with default values. The waste level will be set to zero.

&#x25aa; <strong>+ Earth(int orbitRadius, int wasteLevel)</strong> – Set related fields with the given parameters; note that wasteLevel can’t be below 0.

<strong> </strong>

<em>Method </em>

&#x25aa; <strong>+ int getWasteLevel()</strong> – Return Earth’s waste level.

&#x25aa; <strong>+ boolean orbit()</strong> – Return true if the orbit can occur. For Earth, the orbit can occur only when the Earth’s waste level is less than or equal 5. Otherwise, return false.




<h1>Class <em>Saturn </em>/*Fill Code*/</h1>

<em>Field </em>

&#x25aa; <strong>– int speed </strong>– Number of times that the Saturn will orbit when the orbit command is executed.




<em>Constructor </em>

&#x25aa; <strong>+ Saturn()</strong> – Set related fields with default values. The speed will be set to zero.

&#x25aa; <strong>+ Saturn(int orbitRadius, int speed)</strong> – Set related fields with the given parameters; note that speed can’t be below zero.

<strong> </strong>

<em>Method </em>

&#x25aa; <strong>+ int getSpeed()</strong> – Return Saturn’s speed.

&#x25aa; <strong>+ boolean orbit()</strong> – Return true if the orbit can occur. For Saturn, the orbit can occur only when the speed is more than zero (the number of orbit times will equal to the value of speed eg. speed is 2 means orbits 2 times). Otherwise, return false.

<h1>Class <em>Application </em>/*Fill Code*/</h1>

<em>Field </em>

&#x25aa; <strong><u>– ArrayList&lt;Planet&gt; planets</u></strong> – An ArrayList of Planet.




<em>Constructor </em>

&#x25aa; <strong><u>+ String printPlanet(Planet planet)</u></strong> – Return planet’s specific attribute in the format specified below. If the planet isn’t Earth or Saturn return empty String.

o {PLANET_NAME}’s {SPECIFIC_ATTRIBUTE} is {SPECIFIC_ATTRIBUTE_VALUE}

&#x25aa; eg. “Earth’s Waste Level is 4 ”

&#x25aa; eg2. “Saturn’s Speed is 2 ”

<strong> </strong>

<em>Method </em>

&#x25aa; <strong><u>+ void main()</u></strong> – Create Earth with orbit radius equals 1 and waste level equals 4 and Saturn with orbit radius equals 2 and speed equals 2. Then, add both planets to the ArrayList of Planet. Finally, use printPlanet() to show the specific attribute of each planet (<strong>Note that: toString() method for each planet is forbidden)</strong>.




4.2 Package SolarSystem




Class solarsystem




<em>Field </em>

<ul>

 <li><strong>/*Fill Code*/ </strong><u>+ ArrayList&lt;Planet&gt; planets</u><em> – An ArrayList of planet </em></li>

 <li><em><u>+ </u></em><u>int X_RANGE</u> – range x-axis in solar system.</li>

 <li><u>+ int Y_RANGE</u> – range y-axis in solar system.</li>

</ul>




<u>                </u><em>Method </em>

<ul>

 <li><u>+ void main()</u> – show command menu</li>

 <li><u>+ void addPlanet</u>(Planet planet) – <strong>/*Fill Code*/ </strong>Add planet if the planet does not existed and use printMap() to show solar system.</li>

 <li><u>+ boolean doesPlanetExist</u>(Planet planet) – <strong>/*Fill Code*/ </strong>If planet does existed</li>

</ul>

“print(planet.getClass().toString().split(” “)[1] + ” exists !!!”)”  and return true else return false.

<ul>

 <li><u>+ void printMap()</u> – Show solar system.</li>

</ul>

<em>                                 </em>


