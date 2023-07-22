# About: Javascript_guide
I have created this repo. This repository covers almost all topics of JavaScript along with explanation and examples. Bonus: This repo also includes an explanation about how JavaScript works behind the scenes which most of the developers dont event know. Check it out this guide and standout yourself from other JavaScript developers. Its FREE for all developers. This took me +100 hours to write. If this find you helpful give it a star. 

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch
```bash
  git checkout -b feature/AmazingFeature
```
3. Commit your Changes 
```bash
  git commit -m 'Add some AmazingFeature'
```
4. Push to the Branch 
```bash
  git push origin feature/AmazingFeature
```
5. Open a Pull Request

# 01 Fundamentals 1

### Linking the JS file:
To write javascript directly in html file we use script tag before head tag.
BUT to link the JS file to the html file we use script tag but in the body section at last
```bash
<script src="./script.js"></script>
```
## Varaibles and values
The values are simply values like even string is a value
whereas variable creates a real variable in the computer memory where they store that value.
asssume variable as a box

### Data Types
In javascript the value not have a type variable. There are two data types in javascripts in which we can store values
1. permitive values (number, strings, boolean, undefined, null, symbol and bigInt) //here symbol is value that is unique and cannot be changed
2. Objects

"type of" keyword is used to check the datatype of a value

### Let const and var 
let and const are modern javascript wherease the var is the old way.
let values are mutable, let also used for defining the empty variables
its okay with let to reassign a new value....like if let age = 30 in future  it can be 31 its totally fine. but cannot do this with const. Once assigned it cannot mutate. as const is immutable. Moreover we cannnot declare empty const variable.

#### BEST PRACTICE: 
Always use const as best practice and only use let when you are sure that this value is gonna change somewhere in future. and var variable should be avoided

Let and const are block scope
var is function scope. 

#### IMP: If you will create a variable without defining its type then JS will not create this variable in the currrent scope instead JS will create a property on global object.

### Basic operations

we can console.log more than one value at a time.
```bash
x++    => // x = x+1;
```
comparison operators return the boolean values 

### Operator Precedence 
In precedence there is a concept of performing opertion whether from right to left or left to right.
for that you have to see the table from MDN docs precedence table. Higher the precedence the more operation is supposed to be perform first	

### Strings

for multiple lines for printing we use "\n\"

OR you can use `` instead of single or double quote

### Type conversion

number() function is used to convert varaibles into numbers
sring() function used to convert any varaible into string
and this function return a new value it donot modify the original one

### Type coersion
in this process we deal with two types of different variable and in the back end one variable is converted into other type to perform the opertion
e.g adding string to number. Here number will converted into the string and will contatinate into the string this happens due to the + operator in case of - sign the action would be reversed. (string will convert to number)

### Truthy and Falsy value
Truthy are those values which will return a true value when we will convert them into Boolean() there are several type of truthy values, e.g ({} this will return a true value)
whereas falsy are those which will return a false value when we will convert them into Boolean(). There are only 5 falsy values (0 , '', undefined, null, NaN)

### === vs ==
= means assignment operator 
=== means strict assignment operator (it donot perform the type coersion and will return true only when both the values are exactly the same) 18 === 18 ---> // true
== loose equality operator (it performs type coersion and will return true value '18' == 18 ----> // true.

### Boolean operations
NOT operator has greater precedence than OR(||) and AND (&&) operator

### Switch Case 
This will return that code block which will meet the value of expression with case
Switch case do strict equality comparison // expression === n

```bash
switch(expression) {
  case n:
    code block
    break;
  case n:
    code block
    break;
  default:
    default code block
}
```

### Difference between expression and statements
Statements represent an action or command e.g print statements, assignment statements. Expression is a combination of variables, operations and values that yields a result value.

expression => is a piece of code that produces a value.

statement => it is actually a bigger value of code which donot produces any value and it ends with a semi colon.


### Ternary operator
```bash
condition ? 1st code  block : 2nd code block
```


### Production
For production we use Babel to polyfill and transpile your code (ensure every browser compatibility for all users and convert code into ES5 respectively)
A polyfill tries to emulate specific methods, so you can use them as if they were already supported by the browser (or node engine), on the other hand, A transpiler will modify your code and replace code by other code that does the same, which can then be executed in old browsers.

# 02 Fundamentals 2

### Function
A variable can store single line of code wherease a function can store a stack of code.
```bash
// The below is called constructor function
function Person(firstName, lastName) {
  this.firstName = firstName;
  this.lastName = lastName;
}
```
we cannot call constructor fucntion as regular function. otherwise we will get undefined

### Function Declaration and function expression
if you simply defines a function then this will be a function on the other hand if you define a function and you assign it to a variable then this will called as function expression.

```bash
// This is called function declaration
function ageCalc(birthYear) {
return 2037- birthYear;
}
```
The difference is that in function declaration we can call function even before its declaration. But in case of function expressions you cannot call the function before its declaration.
you first have to declare that function and then after that you can call it.

```bash

//This will called function expression
const calcAge2 = function (birthYear) {
return 2037- birthYear;
}
```

In arrow functions you dont event write return statement explicitly only when the function is one liner
In case of multiple lines you have to write return.
Arrow functions donot take "this" keyword.

### Arrays (data structures)

Alternative way of defining array

```bash
const myArray = new Array(1991,1992,1993)
console.log(myArray)
```

we can mutate the array even they are declared with const. But we cannot replace the whole array declared with const.
like we cant do this:
```bash
const myArray =[1,2,3]
const myArray = [4,5,6]
// ERROR
```

- Arrays can hold different data types all at the same time.
- Arrays can also hold other arrays.
- We cannot do number minus Array

### Arrays basic Operations
- push(anyValue) method returns the length of array. This methods add elements at the end of array.
- unshift(anyValue) method it add the element at the start of array
- pop() method removes the last element and it returns the removed element
- shift() method removes the first element of array and returns that removed element.
- indexOf(anyValue) this method returns the index of the passed element as an argument	
- includes() this element returns boolean value.	(it compares the value using strict operator i.e ===)


### Objects
In arrays we cannot give names to the values. we can only access them by their index number. In order to solve this problem we use objects. it includes key value pair. Each key will called as property.
arrays used for more strcutured data whereas objects used for unstructured data.
we can access data in obj by dot or [] notation

```bash
myObj = {
name: rabah,
agr: 20}

conosle.log(myObj.name);
console.log(myObj['name']; // in bracket notation we can also write some expression (an opertation which returns some value).
```

both will return rabah

## Obj method
Obj can also hold function. And any function attached to the obj is called method. we cannot declare function in an obj but we can write function as an expression in the obj.
```bash

myObj = {
calcAge: function (birthYear) {
return 2037-birthyear}}
// calling it

console.log(myObj.calcAge(1995));
console.log(myObj.['calcAge'](1995));
```

This keyword in obj is equivalent to object itself. This means we can access any property and method in an object by this keyword e.g this.birthYear;

### Continue and break in loops
continue keyword will let the loop to complete its iterations even when the condition is met.
whereas the break keyword will exit the loop immediately once the condition is met.

### While loop
while loop is not dependent on counter.
Use while loop when you are not sure about the number of iterations
```bash
let rep = 1
while (rep<11){
consolse.log(`I have done ${rep} reps`)
rep++};
```

# Javascript in DOM and Events Fundamentals

DOM is used to interact with the elements of the web page.
It is basically a structured representation of HTML page.
DOM is tree structure.

Document is a special object that is the enrty point to the DOM. e.g document.querySelector();
This means query selector method is available on document object.
DOM is not a part of JS.
DOM methods and props are actually the part of Web APIs.

Any thing we get as an input from the user we get it as a string.

```bash
.querySelectorAll() //method returns a node list.
```

```bash
.querySelector() //methods require CSS selectors which are classes and id.
```

you can also add or remove CSS properties like classes by using .classList() method	

### Handling keyboard events
- keyup: event will occur when the key is leave after press.
- keydown: event will occur when the key is pressed
- keypress: press and holding a key

keyboard events are global events that we listen on the whole document therefore we write:

```bash
//listening event on whole document instead on an element.
document.addEventListener('keydown', function (e) {
  if (e.key == 'Escape') {
    modal.classList.add('hidden');
    overlay.classList.add('hidden'); 
  }
});
```

Here e is an event object which will be returned automatically when the event will occur. To see the info about the pressed key you can console.log(e) and object containing a lot of information will be returned.

### Accessing image
```bash
document.querySelector('.dice').src = `dice-${dice}.png`;
```

# 03 How Javascript works behind the scenes
### High Level Language:
In low level languages like C. User have to manually manage the memory. like even while creating varaible. On the other hand High level langugaes like python and Javascript there is a built in 
alogrithm (garbage collector) and we dont need to worry about memory. Low level languages are much faster and optimized as compared to high level languages.

### Garbage collector:
Its a built in algorithm in javascript which is responsible for cleaning the unused objects from memory. Therefore we donot need to worry about memory management.

### Iterpreted or run in time:
Comveting code into machine language. This interpretation happens inside the Javascript engine.

### Multi-paradigm:
Different techinques to approach a solution of a problem.
three famous paradigms are given below:
1. procedural programming
2. OOP
3. Funtioncal Programming

### Prototype-based Object oriented:
like built in methods they are all on blue print we use them from there.

### First-Class functions:
In JS Functions are treated like regular variables.


### Dynamic:
NO need to define the type of variable they will be known at run time. Data type of variable will automatically changed on re-assigning

### Concurrency Model:
How javascript engine handle multiple tasks at the same time.
JS is a single thread non blocking concurrency model. 
Actually thread means a set of instructions. JS execute one instruction at a time. Then how it manage multiple tasks at a time?

This happened by using:
### EVENT LOOP :
This means the JS take long running tasks and execute them in background and once they are completed JS put them into a thread.

### JS Engine
Its simply a program that executes javascript code.
Every JS engine have 2 components
1. Call Stack (Where our code get executed)
2. HEAP (An unstructured memory pool where our objects are stored)


### Difference between Compilation and interpretation
As we know that our computer processor only understand zeros and one.
Compilation: All code is converted into machine code at once and stored in a binary file which can executed by the computer.

```bash
Source Code -----> Compilation (Portable file)-------> Execution
```

Interpretaion: It runs through the source code and execute line by line
```bash
Source Code -------> Line by Line Execution
```
interpreted languages are very slower than compiled languages

People think JS is interpreted language.

BUT now its not true
JS used a combination of interpretation and compilation which is called just in time compilation (JIT). This complied the code into machine code at once and then execute it immediately.
```bash
Source Code -----> Compilation (No Portable file)-------> Execution
```

### Whats going on in JS Engine:
First the code is parse to the engine and the it is converted to AST (Abstract syntax tree) Code then send to Call Stack where this code is get executed (machine code).
To save time the unoptimized version is sent first and then its is resend back to the compilation multiple times to get the optimized version but code wont stop. This make JS engine very fast.
```bash
Parding-------> Compilation -----> Execution (Call Stack)--> |
                        ^                                    |
			|____________________________________|
```

### RUNTIME:
JS Engine and Web APIS(DOM, Timer, Fetch API) are the part of Runtime. Its simply a container.
Web APIs are not the part of JS but they provide features to JS engine accessible on window object.

### Execution Context:
An enviroinment in which the code is executed. It stores all the necessary information to execute the code.
There are three components of execution context:
1. Variable environment (Which stores all the informatin of variables declared).
2. Scope chain (The references of the varaibles which are outside the function).
3. this keyword. 
Now we can say that call stack cotains multiple execution context which keep track on top on each other in order which function is to be executed and when.

(side INFO: Arrow functions do not have arguments and this key word


### SUMMARY of this Section:
The JS code is executed in execution context which is in the Call Stack.
In the context of JavaScript, the process of compiling and interpreting code happens together within the JavaScript engine when running a script or a web application. Let's break down the process step by step:

1. **Parsing**: When you load a JavaScript file or execute a script on a web page, the first step is the parsing phase. During this phase, the JavaScript engine reads the source code and converts it into a data structure known as the Abstract Syntax Tree (AST). The AST represents the hierarchical structure of the code, making it easier for the engine to understand and work with.

2. **Compilation**: After parsing the code into an AST, the JavaScript engine performs various optimizations on the AST to improve the performance of the code. This includes identifying patterns, removing dead code, and optimizing certain constructs for better execution speed. The engine then generates intermediate code, often in the form of bytecode or machine code, which is more efficiently executable than the original source code.

3. **Execution**: Once the intermediate code is generated, the JavaScript engine begins interpreting the code. Interpretation involves executing the intermediate code line by line and performing the actions specified in the code. The engine reads each instruction and performs the corresponding operations, updating variables, invoking functions, and interacting with the program's environment.

It's important to note that modern JavaScript engines, like V8 (used in Chrome and Node.js) and SpiderMonkey (used in Firefox), often use a technique called "Just-In-Time" (JIT) compilation to further optimize the execution process. JIT compilation combines elements of both interpretation and traditional compilation:

- **Interpretation**: Initially, the JavaScript engine may start by interpreting the code directly to quickly get the application up and running.

- **Profiling**: While interpreting the code, the engine keeps track of which parts of the code are executed frequently (hot code paths) and identifies areas that could benefit from further optimization.

- **Compilation**: When the engine identifies hot code paths, it applies a more advanced optimization technique called "dynamic compilation" or "JIT compilation." It recompiles those hot code paths into highly optimized machine code, tailored to the specific environment and runtime conditions. This machine code can then be executed much faster than the interpreted code.

The combination of interpretation and JIT compilation allows JavaScript engines to strike a balance between quick startup times (using the interpreted code) and fast execution speeds (using the compiled machine code). As a result, JavaScript has become significantly faster over the years, enabling developers to build more complex and performant web applications.

# 04 Data Structures, Modern Operators and Strings:

### Destructuring
Its simply unpacking or dividing a data structure into smaller data structure like variables.
We can switch variables easily.
We can get more than one value return from the function
For Arrays:
```bash
const [x,y,z] = [2,3,4] // 2 3 4
```
We can easily switch variables
```bash
[z,y,x] = [x,y,z] // 4 3 2
```
### Nested array
```bash
const nested = [2, 4,[5, 6]]

let [i, ,[j , k]] = [2, 4,[5, 6]]
console.log(i , j , k)  // 2 5 6 
```

```bash
[p, q, r] = [1,2]
console.log( p,q,r) // 1, 2, undefined
```

### Objects destructuring
```bash
//syntax: 
({original name: alias} = object);
dont forget these round brackets
```
```bash
const {name: restaurantName,
	openingHours: hours,
	categories: tag } = restaurant; // where restaurant is an object containing info about restaurant
console.log(restaurantName, hours, tag)
```
```bash
//For parameters which are not in your object but you want to give them a default value you can do below:
const {menu = [], name: restaurantName, openingHours: hours, categories: tag } = restaurant; // here menu is added
```



### Spread operator (...)
This operator is used to spread the arrays or merge one array into another
```bash
const arr= [1,2,4]
const arr2 = [5,6]
arr12 = [5,6,...arr]
//values separated by comma are only acceptable when passing arguments to the function or making a new array
console.log(`${...arr}) this is not acceptable 
```


### REST operator opposite to spread operator
```bash
const [a,b,...other] = [1,2,3,5,6,8,9]

const add =  function(...num){
let sum=0;
for(i=0; i<num.length; i++){
 sum+=num[i]
console.log(sum) }
}

```
```bash
add(2,3,4)
add(10,12,13,15,1,1,1,1,1,9) // as many arguments you want

x= [12,54,68,9,8,74,4]

add(...x);
```

### SHORT circuiting
The result of OR and AND operator is not always a boolean value.
Properties of Boolean operators:
1. They can use any DATA TYPE.
2. They can return any DATA TYPE.
3. They can do short circuiting. (In case of OR operator if the first value is a truthy value it will return that value JS will not even look at the second value. There can be
   multiple values for OR opertar it will see one by one from left to right as the truthy value is found it will return that and will ignore the rest of the variables. In case of all falsy it will return the last one)

In case of AND operator it is exactly opposite of the OR operator it will return falsy value and will ignore the rest values. In case of all truthy it will return the last one

### Nullish Operator

it works on the prinicple of nullish values instead of falsy values. Nullish values are null and undefined.

it returns non- nullish values.
```bash
console.log(0 ?? null) // 0 as zero is non-nullish value
```

### For of loop:
This loop is more like pythons for loop
```bash
const menu = ['applie', 'protein', 1,2,3,4,5,6,7,8,9,10]

for (items of menu) {
	console.log(items);
}
```

### ES6 obj literals
1. if you have key and values both have same values you can go with one name for exp:
{hour: hour} instead you can do thi {hour} both are exactly same.

2. If there is a function expression in an object you can also use new easy syntax that is:
```bash
const obj = {
order: function (){
consolse.lolg('Your order has placed');
}
};

instead you can do this
const obj = {
order(){
consolse.lolg('Your order has placed');
}
};
```

### Optional Chaining
```bash
syntax: property.? 
```

This is useful when we dont know whether the property in a object currently exist or not or whether in the future there will be that property or not.
so for example
```bash
console.(restaurant.openHours.monday?.open);
```

Here we are not sure about the monday that our restaurant is open on monday or not? if it is true then it will proceed otherwise it will return undefined instead of giving us an error.

### LOOP on Objects (which are not iterable)
```bash
const entries = Object.entries(openingHours) 
for ( [day , {open , close} ] of entries) {
	console.log(`Our shop is get open on ${day}` from ${open} to ${close}`)
}
```
here first we extrated array from Objects and then we applied loop on it.

### Sets
```bash
const arr = [1,2,2,3]
const mySet = new set(arr)
```
We can convert an array into set using set() method
Sets are also iterable (means we can apply loop on them) but they do not repeat any content.
We cannot use index on sets.
- set uses .size() method instead of .length() (it do not count repeated objects)
- set uses .has() method instead of include() method
- set uses .add() method instead of push() method
- set uses .delete() method instead of push() method
- .clear() method is used to delete all the objects
- arrays use .length() method
- spread operator work same for sets

### Map
Map objects are collections of key-value pairs. A key in the Map may only occur once; it is unique in the Map 's collection. A Map object is iterated by key-value pairs — a for...of loop returns a 2-member array of [key, value] for each iteration.
```bash
// Creating Map object Method 1
const myMap = new Map();
myMap.set(key,value)  //here set keyword actually modify the myMap or on which it is applying
```

```bash
// Creating Map object Method 1
const myMap = new Map([key1, value1], [key2, value2]);

.get() method is use dto retrieve the value

```

### Data structure
4 Basic Built-In
1. Arrays
2. Objects
3. Set
4. Map

### Non-BUilt-in
- Stacks
- Queues
- Linked lists
- Trees
- Hash Tables


### When to use which
1. Arrays (When you need an ordered list may contain duplicates and when you need to manipulate data) 
2. Set (When you need an order UNIQUE list, high performance as searching elements in sets are 10x faster than arrays, removes duplicate from arrays
3. Objects (More traditional, easy to write and access data value with . and [], when you used funcitons as values, when working with JSON (can convert to Map))
4. Map (Better perfromance, can have any data type, Easy to iterate, Easy to compute size)  

### Strings
We can get any Alphabet by simply using index on strings
Strings are immutable.

Slice method is used to extract specific portion from an existing string. It returns that extracted value not modify the string as we know strings are immutable.
Behind the scenes JS convert string into an object thats why we are able to apply methods on them.
Slice(start, end) method take two arguments starting and ending index. if you wont give the ending index and only give the starting index it will start and go each by each to the ending 
index like loop.
```bash
console.log('apple'.toUppercase.slice(1))  //aPPLE
```

```bash
anySentence.replace(string to be replaced, new string)
```

This will only replace the first occurance of that word in the sentence. In order to change all the occurance one must have to you a special syntax as given below:
for exp we want to replace all door words in the sentence with gate so do as below:
```bash
anySentence.replace(/door/g, gate)  // here g stands for global
```

### Split Method
The split() method is used to split the given string by provided symbol and it returns an array.
```bash
console.log('An+Apple'.split('+')); // ["An", "Apple"]
```
```bash
console.log(['MR.', 'Mukhesh'.toUpperCase, 'Gahlot'].join('---')); //Mr.---MUKHESH---Gahlot
```

# 05 Advance Functions
### Default Parameters
These default parameters are the values which are passed to the function in case we donot provide them.
for example:
```bash
const shopping = function(fruitName,  size='standard', fruitPrice = 85){
    
	console.log(`The price of ${size} size ${fruitName} is $${fruitPrice}`);
};
shopping('Apple' , undefined , 99); //The price of standard size Apple is $99
// this is how you skip the in between argument as default.
```

Here we didnt provide any 2nd argument and the function took the default value of size that is 'standard'

### Passing by values or Passing by function

Javascript always pass by value although it seems like it pass by reference but actually thats not the case cause that ref is ultimately an address of the value stored in HEAP (memory).
So actually we pass reference to function not pass BY reference.

### Frist class functions and Higher order functions.

- Functions are another objects and values on which we can call methods
- Functions are simply values which a getting return on some action.
- Storing function in a variable, passing function as an argument to the other functions, return functions from functions, calling methods on functions
All examples of first class function (Simply a function)

### Higher order function:
Function that receive another function or return a new function (call-back function) are called higher order function

### JavaScript Abstraction
An abstraction is a way of hiding the implementation details and showing only the functionality to the users. In other words, it ignores the irrelevant details and shows only the required one.
```bash
element.addEventListener('click', clickHandler());
// We just passed function as a value instead of writing the whole functionality here this kind of hidding techniques are called JS Abstractions.
```


### Function returning a function

```bash
const greet = function(greeting) {
	return function(name) {
		console.log(`${greeting} ${name}`)
}
};

//OR // writing arrow function of above

const greetArrow => greeting => name => console.log(`${greeting} ${name}`)

const greetHello = greet('hello');
greetHey('Waaqqah')

// hello waaqqah

//OR

greeting('hello')('Waaqqah');  //hello Waaqqah
```

### Call and apply method

As we know that this keyword depends on how a function is called.
As we also know in regular calling function the this keyword is undefined (when strict mode is ON).
So if there is a funciton is in an object and that function contains this key word then it would be find if we call that function on an object. But this wont be work if we call that function
as regular function the reason on calling regular function the function dont know what this keyword is. 

So this problem can be solve if we tell the function what this keyword is. So we can do that by using call
```bash
// Syntax:
anyfunction.call(object_where_we_are_point_our_this_keyword, other aurguments which function receive)
```

```bash
const menu = {
lulu : 'candy',
dish: 'fish',
book(fruit, price){
	console.log(`${this.lulu}, ${this.dish} ${fruit} ${price} `);
}
}
const book = menu.book;
book('Apple' , 87) // here we are calling book as regular function this will give use an error

```

#### Correct WAY
```bash
book.call(menu, 'Apple' , 87); // Here menu is an object and apple and 87 are arguments
```

### Apply method
It is exactly same as call but the difference is that it takes an array of arguments instead of separate arguments

```bash
myList = ['Apple' , 87]
const book = menu.book;
book.call(menu, myList); // Here menu is an object and myList is an array and passing as an argument.
```



### Bind function
This function also have the same purpose to solve the this keyword problem.
The difference is that this bind function returns a new function (that new function is already integrated with this keyword) on which we can pass our arguments
```bash
const book = menu.book;
const newFunc = book.bind(menu); // here menu is an object 
newFunc('Apple' , 87);
```

### Immediately invoked function Expressions (IIFE)
These are the function expresion which are executed once will never be executed again. They will immediately disappear after their execution.
An IIFE (Immediately Invoked Function Expression) is a function that runs the moment it is invoked or called in the JavaScript event loop. Having a function that behaves that way can be useful in certain situations. IIFEs prevent pollution of the global JS scope.

```bash
(() => console.log('I am IIFE'))();
```
# 06 Advance Arrays and Methods
### Array Methods
### slice() Method
The slice() method returns selected elements in an array, as a new array (not modify the original one). 
The slice() method selects from a given start, up to a (not inclusive) given end.
```bsah
//slice(start, end)
.slice(-1) means the last element
console.log(arr.slice(2)) //[c, d, e]
```
this method can also be used to create a copy of an array.

###Splice Method
--------
```bash
.splice(start, end)
```
work same as slice but it modifies/mutate the original array. used to remove the elements

### reverse() method

this method reverse the elements but it mutate the original array 

### concat() method
this method returns a new array and used to merge 2 arrays
```bash
const combo = arr1.concat(arr2);
console.log(combo);
```


### join() method

join method is used to join the elements 
```bash
const arr =[a,b,c]
console.log(arr.join('-')) // a-b-c
```


### forEach method
This method is used to loop over each item and receives a function as an argument to what to do with each item

```bash
const arr =[1, 2, 3]
arr.forEach(function(items){
	console.log(items*2)
}) // 2 4 6
```


### forEach on MAP and SET
```bash
//syntax:
myMap.forEach(callback, value, key, thisArg)
```

```bash
const myMap = new Map([['name', 'Larry Wheel'], ['skill', 'Wheeler'], ['age' ,'67']]);
myMap.forEach(function(value, key, map){
console.log(`${key}:${value}`)}); 

// name:Larry Wheel
   skill:Wheeler
   age:67
```


### forEach on SET
```bash
const mySet = const myMap = new Map(['name', 'Larry Wheel', 'skill', 'Wheeler', 'age' ,'67']);
mySet.forEach(function(value, _, map){
console.log(`value}:${value}`)}); 
```



### MAP, FILTER, REDUCE
forEach method is also used for side effects (means doing some work without returning any value)
ALl these method loop over an array.
- Map method is same as foreach method but the difference is that it returns a new array.
```bash
const arr = [1,2,3]
const arr2 = arr.map(function(items){
	 return items*2}
console.log(arr2); //[2,4,6]
```

- Filter method also return a new array only containing those elements which passed the given test via function.
```bash
syntax: .filter((value, index, array)=>{call back function})
```
```bash
const arr = [-1,2,3,-4,-9]
const arr2 = arr.filter(function(items){
	 return items<0}
console.log(arr2); //[-1, -4, -9];
```

- Reduce method is used to reduce a whole array into one single value e.g, adding all the elements of the array etc.it includes and accumulator and a current value. Each value is get added to
accumulator. Assume accumulator as snow ball which gets bigger and bigger as its roll down the hill.

```bash
const arr2 = arr.reduce(function(accumulator, current){
	 return accumulator + current;) , 0 }; //here 0 is the of accumulator it could be any thing even an empty object
```
EXP2: 
```bash
const array = ["pacs1", "pacs2", "pacs3"];
// console.log(array);

const data = array.reduce((acc, curr) => {
  acc.push({ key: curr, value: curr })
  return acc;
}, []);

console.log(data);

[{key: 'pacs1', value: 'pacs1'},
{key: 'pacs2', value: 'pacs2'},
{key: 'pacs3', value: 'pacs3'}]

```

### Chaining method
In this technique we apply one method on another method and so on.

Example CODE:
```bash
const interest = movements
    .filter(mov => mov > 0)
    .map(deposit => (deposit * 1.2) / 100)
    .filter((int, i, arr) => {
      console.log(arr);
      return int >= 1;
    })
    .reduce((acc, int) => acc + int, 0);
  labelSumInterest.textContent = `${interest}€`;
};
calcDisplaySummary(account1.movements);
```

### Find() method
This method also accepts a condition (in terms of call back function) and return only first value which satisfy the condition it do not return a new array. It is very similar to filter method. The fundamental difference is that find method only return the first element and do not return a new array whereas filter method returns all the filtered elements and return a new array.
```bash
const arr = [1,2,-6,5,-10]
const firstElement = arr.Find(item => item<0);
console.log(firstElement) //-6
```

### findIndex() and IndexOf()

Both methods are almost same but the major difference is that in indexof method we simply provide the value whether it exist in the array or not if yes then return the index of that value. 
on the other hand in findindex we can perform a complex condition which will return either true or false value and will return the index of the value.

### Some method
Some method returns a boolean value. This method is almost same as include method but the difference is that it checks the availabilty of the item in an array by a condition specified
by a user using call back function.

### Every method
Every method also returns a boolean value. This method is almost same as some method but the difference is that it returns true only when all the elements of an array satisfies the given condition
via callback function


### Flat and FlatMaP
- Flat method is used to flaten the array. If there is a nested array you can make a single non nested array using this function and it do not require any call back function.
But it flatens only one level of nest...it do not completely flat a deeper nested array. In order to flated a deeper level of nested array you must have to specify the deepness of the array

for example:
```bash
const arr = [[[1,2],3],4,[5,6,[7]],8]

console.log(arr.flat(2)) // [1,2,3,4,5,6,7,8]
```

###flatMap
This method is simply a combination of flat and map methods
you first simple map the array and then flat it
it receive exactly the same call back function as map method

### sort method

This method is used to sort the array. This method mutates the original array.
sort method sorts the elements on the basis of string. First it converts everything to string and then it does sorting on the basis of alphabetical order.
in case of numbers converted to string -ve values would be come first and order will numerical like 1 2 3 ascending.
in order to truely make the array sorted in which numbers are converted to string we have to do something like that
// remember if return < 0, A,B (keep order)
// if return > 0, B,A (switch order)

```bash
//Ascending
arr.sort((a,b) => {
if (a>b) {
return 1
}
if (a<b) {
return -1}
}
```
```bash
//Descending
arr.sort((a,b) => {
if (a>b) {
return -1
}
if (a<b) {
return 1}
}
```

### Fill method
This method is used to progammatically fill the arrays
```bash
syntax: array.fill(value, start, end)
```

```bash
const arr = [1,2,3,4,5]

console.log(arr.fill(5, 1, 3) // [1,5,5,4,5] 

```

### From method
This method returns a new array and used to create arrays
it receives two arguments one is length of the array and second is map function

```bash
const arr = Array.from({length : 7}, (_,i)=> { return i+1});
console.log(arr) // [1,2,3,4,5,6,7]
```

### Assign method
Assign method is used to merge two objects. Here we are merging an empty obj with our existed Obj to create a clone
```bash
const deepClonedObj = object.assign({}, myobj); // but its value will change
//but this problem can be solve by using loadash module
```


### Object.freeze(myObj)
This method is used to make the arrays and object immutable

### Object.values(myObj)
This method returns an array of values of objects

# 07 Arrays Summary and which to use when
