Download Link: https://assignmentchef.com/product/solved-lab-exercise-10-problems
<br>
<ol>

 <li>Write C++ programs</li>

 <li>Compile C++ programs</li>

 <li>Implement programs that use advanced class concepts such as constructors, destructors, and member functions.</li>

</ol>

<h1><a id="user-content-additional-reading" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10#additional-reading" aria-hidden="true"></a>Additional Reading</h1>

This lab exercise requires an understanding of some concepts to solve the problems. You are strongly encouraged to read the following tutorials to help you answer the problems.

<ol>

 <li><a href="https://github.com/ILXL-guides/function-file-organization">Organizing C++ files: function prototypes, implementations, and drivers</a>.</li>

 <li><a href="https://github.com/ILXL-guides/object-parameters-and-return-values">Using objects as parameters and return values in functions</a></li>

 <li><a href="https://github.com/ILXL-guides/arrays-as-parameters">Passing arrays as parameters to functions</a></li>

 <li><a href="https://github.com/ILXL-guides/cpp-file-io">File reading and writing (also includes dealing with arrays)</a></li>

</ol>

<h1><a id="user-content-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10#instructions" aria-hidden="true"></a>Instructions</h1>

Answer the programming problems sequentially (i.e., answer prob01 before prob02). If you have questions let your instructor or the lab assistant know. You can also consult your classmates.

When you answer two programming problems correctly, let your instructor know and wait for further instruction.

<h1><a id="user-content-lab-exercise-guide" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10#lab-exercise-guide" aria-hidden="true"></a>Lab exercise guide</h1>

Here’s a link to the <a href="https://docs.google.com/document/d/1EX01EtrO-pkHNLVPxiq7HNh1f5KnJZnr_dlJcO4T7t0/edit?usp=sharing" rel="nofollow">Lab exercise guide</a> in case you need to review the lab exercise objectives, grading scheme, or evaluation process.

<h1>Digicup</h1>

This program simulates interactions with a <code>Cup</code> object for getting a drink, refilling a drink, emptying a drink, and drinking from it.

<h2><a id="user-content-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#output" aria-hidden="true"></a>Output</h2>

All of the output statements (<code>std::cout</code>) should be in <code>main</code> and are mostly provided for you. You will only need to complete the menu functionality by calling the appropriate member functions from the <code>Cup</code> object. Your member functions are designed to only perform calculations and return values.

The <code>Cup</code> object will be used to ask the user for the type of drink they prefer and the amount they want to drink.

The menu options are shown below for your reference:

<pre><code>D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: Exit</code></pre>

<h2><a id="user-content-the-cup-class" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#the-cup-class" aria-hidden="true"></a>The <code>Cup</code> class</h2>

<h3><a id="user-content-data-members" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#data-members" aria-hidden="true"></a>Data members</h3>

Create a class called <code>Cup</code> with the following member variables:

<ol>

 <li><code>drink_type_</code> which is an <code>std::string</code> that will be the name of the drink.</li>

 <li><code>fluid_oz_</code> which is a <code>double</code> that will be the amount of fluid in the cup.</li>

</ol>

<h3><a id="user-content-constructors" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#constructors" aria-hidden="true"></a>Constructors</h3>

<h4><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#default-constructor" aria-hidden="true"></a>Default constructor</h4>

The default constructor should initialize <code>drink_type_</code> to <code>"Water"</code> and initialize <code>fluid_oz_</code> to <code>16.0</code>

<h4><a id="user-content-non-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#non-default-constructor" aria-hidden="true"></a>Non-default constructor</h4>

The non-default constructor should take in an <code>std::string</code> parameter that will be the name of the drink type and a <code>double</code> parameter that will be the amount of drink in the cup. It should set the passed parameter values to the corresponding data members.

<h3><a id="user-content-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#member-functions" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-drink" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#drink" aria-hidden="true"></a>drink</h4>

Drinking reduces the amount of liquid in the <code>Cup</code> based on a given <code>amount</code> that is passed as a parameter. Take note that <code>fluid_oz_</code> should never be negative such that if you drink an <code>amount</code> that is greater that <code>fluid_oz_</code>, then <code>fluid_oz_</code> should be set to <code>0</code>.

<h5><a id="user-content-refill" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#refill" aria-hidden="true"></a>refill</h5>

Refilling the cup increases the amount of liquid in the <code>Cup</code> based on the given parameter, <code>amount</code>. Assume the cup is bottomless.

<h5><a id="user-content-new_drink" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#new_drink" aria-hidden="true"></a>new_drink</h5>

Throw out your current drink and replace it with a new drink. The function accepts two parameters. The first is the name of the new drink type and the second is the amount of the new drink type.

<h5><a id="user-content-empty" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#empty" aria-hidden="true"></a>empty</h5>

<em>Empties out</em> the contents of the cup in it’s entirety. <code>fluid_oz_</code> should be set to 0, and <code>_drink_type</code> should be set to <code>"nothing"</code>.

<h5><a id="user-content-accessors" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#accessors" aria-hidden="true"></a>Accessors</h5>

Create the accessors for <code>fluid_oz_</code> and <code>drink_type_</code>.

<h2><a id="user-content-other-information" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#other-information" aria-hidden="true"></a>Other information</h2>

Place the <code>Cup</code> class in <code>cup.hpp</code> and complete the code in <code>main.cpp</code>.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#sample-output" aria-hidden="true"></a>Sample Output</h2>

<pre>What kind of drink can I get you?: <b>Kool Aid</b>How much do you want?: <b>32</b>Your cup currently has 32 oz. of Kool AidPlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>D</b>How much do you want to drink from the cup?: <b>16</b>Your cup currently has 16 oz. of Kool AidPlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>D</b>How much do you want to drink from the cup?: <b>6</b>Your cup currently has 10 oz. of Kool AidPlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>R</b>How much do you want to refill your cup?: <b>2</b>Your cup currently has 12 oz. of Kool AidPlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>E</b>Emptying your cupYour cup currently has 0 oz. of nothingPlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>N</b>What is the new drink you want?: <b>Coke</b>What is the amount you want?: <b>16</b>Your cup currently has 16 oz. of CokePlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>D</b>How much do you want to drink from the cup?: <b>8</b>Your cup currently has 8 oz. of CokePlease select what you want to do with your drink/cup?:D: DrinkR: RefillN: Get a brand new drinkE: EmptyX: ExitSelection: <b>X</b>Thank you for using Digicup!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob01#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>




<h1>Shopping List</h1>

Create a <code>ShoppingList</code> class that has three data members: a <code>std::string*</code> <code>list_</code>, an <code>int</code> <code>num_items_</code>, and an <code>int</code> <code>list_size_</code>.

<h2><a id="user-content-shoppinglist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#shoppinglist" aria-hidden="true"></a>ShoppingList</h2>

<h3><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#default-constructor" aria-hidden="true"></a>Default constructor</h3>

The default constructor should dynamically allocate <code>list_</code> to an array of <code>std::string</code> objects with a size 10, initialize <code>num_items_</code> to 0, and set <code>list_size</code> to 10.

<h3><a id="user-content-non-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#non-default-constructor" aria-hidden="true"></a>Non-default constructor</h3>

The non-default constructor should receive one parameter: an <code>int</code> that is the size of the dynamically-allocated array of <code>std::string</code> assigned to <code>list_</code>. The size from the parameter should also be assigned to <code>list_size_</code> and <code>num_items</code> should be set to 0.

<h3><a id="user-content-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#member-functions" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-accessors" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#accessors" aria-hidden="true"></a>Accessors</h4>

Create accessor functions for <code>num_items_</code> and <code>list_size_</code>.

<h4><a id="user-content-add_item" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#add_item" aria-hidden="true"></a>add_item</h4>

Create a function <code>add_item</code> that receives an <code>std::string</code> and adds it to the first available location in the list.

Adding an item should also increment <code>num_items_</code> which is used to track the total number of items added to the array and, conveniently, stores the index for the next item.

If you attempt to add an item into a full list, you should display an error message <code>Error! Shopping List full!</code>.

<h4><a id="user-content-remove_last" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#remove_last" aria-hidden="true"></a>remove_last</h4>

Create a function <code>remove_last</code> that removes the last item from the list. Specifically, it sets the value of the last element to an empty string <code>""</code> and decrements <code>num_items_</code>.

<h4><a id="user-content-print_list" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#print_list" aria-hidden="true"></a>print_list</h4>

Create a function<code>print_list</code> that prints all elements in the list. It provides the numbering for items. For example, given a list of three items, it might show:

<pre><code>1) Milk2) Eggs3) Flour</code></pre>

<h4><a id="user-content-destructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#destructor" aria-hidden="true"></a>Destructor</h4>

Create a destructor that uses the <code>delete []</code> keyword to delete the list of shopping items. Don’t forget to set the list pointer to <code>nullptr</code> to avoid dangling references.

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Store your <code>ShoppingList</code> class in <code>list.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>list.hpp</code> and implementatiion in <code>list.cpp</code>.

In <code>main.cpp</code>, create a <code>ShoppingList</code> object using the non-default constructor where you pass it the value of 10. Add items to the shopping list according to the output below. Call the <code>print_list</code> function to display all items. The values are hard-coded and do not need to be retrieved from the user (no need for <code>std::cin</code>). See <code>main.cpp</code> for more details.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre><code>Shopping List:1) Milk2) Eggs3) Flour4) Sugar5) Cocoa Powder6) Vanilla</code></pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob02#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>list.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp list.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>




<h1>Player</h1>

Create a <code>Player</code> class with the following data members to represent a game character: <code>xpos_</code> that is an <code>int</code> representing their x position, <code>ypos_</code> that is an <code>int</code> representing their y position, <code>name_</code> that is an <code>std::string</code> representing the player’s name, and <code>health_</code>, <code>strength_</code>, and <code>defense_</code> which are all <code>int</code>s representing the character’s attributes.

<h3><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#default-constructor" aria-hidden="true"></a>Default Constructor</h3>

Create a default constructor that initializes the following values to your data members: <code>0</code> for the x position, <code>0</code> for the y position, <code>Ash</code> for the name, <code>10</code> for the health, <code>5</code> for the strength and <code>2</code> for the defense.

<h3><a id="user-content-non-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#non-default-constructor" aria-hidden="true"></a>Non-Default Constructor</h3>

Create a non-default constructor that takes in 6 values: the name, the health, the strength, the defense, the x position, and the y position respectively. These should be used to initialize the corresponding data members.

<h3><a id="user-content-accessors--mutators" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#accessors--mutators" aria-hidden="true"></a>Accessors &amp; Mutators</h3>

Create accessors and mutators for all data members

<h3><a id="user-content-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#member-functions" aria-hidden="true"></a>Member functions</h3>

<h4><a id="user-content-display_stat" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#display_stat" aria-hidden="true"></a>display_stat</h4>

Create a member function called <code>display_stat</code> that takes in no parameters and does not return anything. This member function should display the name of the player, the player’s health, the player’s strength, the player’s defense, and the player’s coordinates (x and y position). Look at the output provided below for an example.

<h4><a id="user-content-player_move" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#player_move" aria-hidden="true"></a>player_move</h4>

Create a member function called <code>player_move</code> that takes in no parameters and does not return anything. This member function should increment the x position and the y position by a value of 1.

<h4><a id="user-content-is_player_dead" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#is_player_dead" aria-hidden="true"></a>is_player_dead</h4>

Create a member function called <code>is_player_dead</code> that takes in no parameters and returns a <code>bool</code> value. This member function should check the player’s health. If the player’s health is equal to 0, then return <code>true</code>, otherwise return <code>false</code>.

<h4><a id="user-content-take_damage" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#take_damage" aria-hidden="true"></a>take_damage</h4>

Create a member function called <code>take_damage</code> that takes in an <code>int</code> value for the damage taken and returns nothing. This member function should display a statement saying that the player took damage, and decrease the player’s health based on the damage taken.

If the damage taken is greater than the player’s current health, set the player’s health to 0 (the player cannot have negative health). This member function should call the <code>is_player_dead</code> function to check whether the player survives the attack. If the player is dead, display a statement saying that the player is dead. Look at the output provided below for an example.

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#other-instructions" aria-hidden="true"></a>Other instructions</h2>

Place the <code>Player</code> class inside <code>player.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>list.hpp</code> and implementatiion in <code>list.cpp</code>.

The <code>main</code> function is already provided for you. Do not edit the <code>main.cpp</code> file.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#sample-output" aria-hidden="true"></a>Sample output</h2>

<pre><code>Player: AshHealth: 10Strength: 5Defense: 2At position: (10, 10)Player: LesHealth: 20Strength: 10Defense: 6At position: (0, 0)Ash took 25 damageAsh is deadPlayer: AshHealth: 0Strength: 5Defense: 2At position: (10, 10)</code></pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob03#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>player.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp player.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Advanced Student Class</h1>

Create a <code>Student</code> class that has four data members: an <code>std::string</code> <code>name_</code>, an <code>int</code> <code>id_</code>, an <code>int[]</code> <code>grades_</code>, and an <code>int</code> <code>num_grades_</code>. The grades array will have a capacity of 10 elements.

Create a default constructor that sets <code>name_</code> to “Stu Dent”, <code>id</code> to 123456789, <code>grades_</code> empty, and <code>num_grades_</code> to 0.

Create a non-default constructor that receives an <code>std::string</code> and an <code>int</code> for the student’s name and id, respectively. Remember to set <code>num_grades_</code> to 0 as well.

Create accessor and mutator functions for <code>name_</code>, <code>id_</code>, and <code>num_grades_</code>.

Create a function called <code>add_grade</code> that receives an <code>int</code> and adds it to the <code>grades_</code> array if there is space. The grade should not be added to the array if it exceeds 10 and displays the error message: <code>Array full, unable to add grade</code>.

Create another function called <code>calculate_grade</code> that returns the average of the grades as a <code>double</code>. Take note that if the user added fours grades, then the function should return the average of those four grades only.

Finally create a function called <code>print_student</code> that prints the student’s name and all their grades.

The <code>main.cpp</code> has already been created for you. It creates a <code>Student</code> object, adds grades to it, calls the <code>print_student</code> function, then prints the student’s total grade. You do not need to modify <code>main.cpp</code>.

Place your class in <code>student.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>student.hpp</code> and implementation in <code>student.cpp</code>.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob04#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre><code>Lonnie Hansen 965137824Test Grades:9588927784Total grade = 87.20</code></pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob04#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob04#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>student.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp student.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Find Number</h1>

Create a class called <code>Numbers</code>. Create two data members, an <code>int*</code> <code>values_</code> that points to a dynamically allocated array of numbers and an <code>int</code> <code>capacity_</code> that stores the total number of elements that the array can hold.

<h2><a id="user-content-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#default-constructor" aria-hidden="true"></a>Default Constructor</h2>

Create a default constructor that initializes (sets) the value of 10 to <code>capacity_</code> and initializes a new dynamically allocated array with a capacity of 10. It should call the <code>init</code> function inside the body of the constructor.

<h2><a id="user-content-non-default-constructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#non-default-constructor" aria-hidden="true"></a>Non-default Constructor</h2>

Create a non-default constructor that accepts an <code>int</code> parameter that is assigned to <code>capacity_</code> that is used as the capacity of the dynamically allocated array. It should also call the <code>init</code> function inside the body of the constructor.

<h2><a id="user-content-destructor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#destructor" aria-hidden="true"></a>Destructor</h2>

Create a destructor that deletes the dynamically allocated array and initializes the pointer to <code>nullptr</code>.

<h2><a id="user-content-accessor" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#accessor" aria-hidden="true"></a>Accessor</h2>

Create an accessor for <code>capacity_</code>.

<h2><a id="user-content-member-functions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#member-functions" aria-hidden="true"></a>Member functions</h2>

<h3><a id="user-content-init" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#init" aria-hidden="true"></a>init</h3>

The implementation of the <code>init</code> member function is already provided for you. You only need to create it’s function prototype in <code>find_number.hpp</code>. This function should be a <strong>private</strong> member function that sets initial values of your dynamically allocated array according to the capacity.

<h3><a id="user-content-display_array" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#display_array" aria-hidden="true"></a>display_array</h3>

Create a member function <code>display_array</code> that displays the contents of the array, as shown in the output below.

<pre><code>2 4 6 8 10 12 14 16 18 20</code></pre>

<h3><a id="user-content-find_number" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#find_number" aria-hidden="true"></a>find_number</h3>

Create a member function <code>find_number</code> that takes in an <code>int</code> parameter representing the number you want to find. It should check to see if the array contains the number that is passed. If the number is present, then display a statement saying that the number is in the array as shown in the the output below.

<pre><code>2 is in the array</code></pre>

<h2><a id="user-content-other-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#other-instructions" aria-hidden="true"></a>Other instructions</h2>

The main function is already given to you. Do not edit <code>main.cpp</code>, but place your <code>Numbers</code> class in <code>find_number.hpp</code>. Member functions that take more than five lines or use complex constructs should have their function prototype in <code>find_number.hpp</code> and implementation in <code>find_number.cpp</code>.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#sample-output" aria-hidden="true"></a>Sample Output</h2>

<pre><code>2 4 6 8 10 12 14 16 18 202 is in the array10 is in the array16 is in the array</code></pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Created function prototype and stored in <code>.hpp</code> file.</li>

 <li>Created function implementation and stored in <code>.cpp</code> file (see <a href="https://github.com/ILXL-guides/function-file-organization">reference</a>).</li>

 <li>Call function in the driver</li>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_10/prob05#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code saved in <code>find_number.cpp</code> and <code>main.cpp</code>, and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp find_number.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<pre><code>make all</code></pre>