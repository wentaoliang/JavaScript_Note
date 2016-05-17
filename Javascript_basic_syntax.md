# Javascript

## Basic Syntax

### Remove elements

> .pop()

The pop method **removes the last element** from an array and returns that value to the caller. 

	//Example 
	var ourArray = [1,2,3];
	var removedFromourArray = ourArray.pop();
	//removeFromourArray now equals 3, and our Array equals [1,2]
	
	//Setup
	var myArray = [["John", 23], ["cat", 2]];
	var removedFromMyArray = myArray.pop();
	//removedFromMyArray now equlas ["cat",2], and myArray equals ["John", 23]

<br>

> .shift()

The shift method **removes the first element** 

	//Example 
	var ourArray = ["Stimpson", "J", ["cat"]];
	removedFromourArray = ourArray.shift();
	//removedFromourArray now equals "Stimpson" and ourArray now equals ["J", ["cat"]]


### Add elements

> .push()

.push() takes one or more parameter and "pushes" it onto the **end of the array**.

	//Example 
	var ourArray = ["Stimpson", "J", "cat"];
	ourArray.push(["happy","joy"]);
	//ourArray now equals ["Stimpson","J","cat",["happy","joy"]]

<br>

> .unshift()

.unshift adds the element **at the beginning** of the array.

	//Example 
	var ourArray = ["Stimpson", "J", "cat"]
	ourArray.shift(); //ourArray now equals ["J", "cat"]
	ourArray.unshift("Happy");
	//ourArray now equals ["Happy", "J", "cat"]
 
<hr>

### Shopping List

Creat a shopping list in the variable **myList**. The list should be a multi-dimensional array containing several sub-arrays.

The first element in each sub-array should contain a string **the name of the item**. The second element should be a **a number representing** the quanity i.e. 

> ["Chocolate Bar", 15]

There should at least 5 sub-arrays in the list. 

	//Example
	var myList = [["Milk",5],["Apple",6],["Orange",10],["Beef",1],["Pork",20]];

<hr>

### Function

#### Write Reusable JavaScript with Functions

In JavaScript, we can divide up our code into reusable parts called *functions*.

> function functionName () {
	console.log ("Hello World");
  }

You can call or invoke this function by using its name followed by parenthese, like this :

> functionName ();

Each time the function is called it will print out the message **"Hello World"** on the dev console. All of the 
code between the {} will be executed every time the function is called. 


#### Passing Values to Functions with Arguments

*Parameters* are varibales that act as placeholders for values that are to be input to a function when it is called. When a function is defined, it is typically defined along with one or more parameters. The actual values that are input (or "passed") into a function when it is called known as *arguments*.

> function testFun(param1, param2) {
	console.log(parm1, param2);
 }
Then we can call **testFun**:
	testFun ("Hello", "World");


#### Global Scope and Functions

In JavaScript, *scope* refers to the visibility of variables. Variables which are defined outside of a function block have _**Golal**_ scope. This means, they can be seen everywhere in your JavaScript code. 

Vairbales which are used without the *var* keywords are automatically created in the *global* scope. This can create unintended consequences eleswhere in your code or when running a funciton aggin. **You should always declare your variables wit** _**var**_. 
 
	Local scope:
	//Example
	//code here can not use carName
	function myFunction() {
	    var carName = "Volvo";
	//code here can use carName
	}
	
	Global scope:
	//Example
	var carName = "Volvo";
	//code here can use carName
	function myFunction() {
	//code here can use carName
	}
	
	Automatically Global: 
	//Example
	//code here can use carName
	function myFunction() {
	    carName = "Volvo";
	    //code here can use carName
	}

#### Local Scope and Functions

**Local scope** means parameters are only visible within the function.

	//Example
	function myTest() {
	    var loc = "foo";
	    console.log (loc);
	}
	myTest(); //"foo"
	console.log(loc); //"undefined"

#### Global vs Local Scope in Functions

It is possiable to have both *local* and *global* variables with the same name. When you this, *local* variable takes **precedence over** the *global* variable. 

	//Example 
	var someVar = "Hat";
	function myFun() {
	    var someVar = "Head";
	    return someVar;
	}
	//myFun will return Head because local version of the variable is present


#### Return a Value from a Function with Return

Use a **return** statement to send a value back out of a function 

	//Example 
	function plusThree(num) {
	    return num + 3;
	}
	var answer = plusThree(5); 
	//pluseThree takes an argument for num and returns a value equal to num + 3 

#### 