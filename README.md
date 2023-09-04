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
### What is Javascript
It is:
- high level (we dont need to worry about memory management)
- Object Oriented (we will store most of the data in the form of objects)
- Multi-Paradigm (we can use different styles of progamming)
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
EXP 3:
```bash
const store = [
		{name: 'rabah1', price: 2},
		{name: 'rabah2', price: 6},
		{name: 'rabah3', price: 6}
		]

const TotalPrice= store.reduce((accumulator, item)=>{return total + item.price}, 0)
console.log(TotalPrice);

// output: 14
```
Here we just have to understand two parameters, accumulator (whose value will be unpdated) and item (This is the each item in the list)
You always have to give the initial value of accumulator.


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

# 07 Advance DOM and Event Handling

### How DOM really works
DOM is nothing its simply an interface to communicate between the Javascript and Web browser.
So we can say that the DOM is very complex API as it has ton of methods and properties.
Always remember everything in HTML document is a node. And each node in JS is represented by an object.
Element, text, comments and even the document is node.
These nodes in html provide the JS the ton of properties such as innerHTML, .remove(), .append() etc. 

Now there is a concept of inheritance where all the children elements have access to their parent elements.
addEventListeners work because of Event Target node which is parent of both node and window (global object node type). So thanks to inheritance with all make this possible interaction.

when we click on an element then the event travel from capturing phase document-->html-->body-->section-->element and once the event is reached to the target state then it bubble back to the document.
this process is called capturing and bubbling
### Method

```bash
getComputedStyle() //this method is used to get the value of the styles added to the elements 

console.log(getComputedStyle(message).color); // rgb(187,187,187);

document.document.style.color.setProptery('--color-primary', 'orangered');
```

- The getBoundingClientRect() method returns the size of an element and its position relative to the viewport.

- The getBoundingClientRect() method returns a DOMRect object with eight properties: left, top, right, bottom, x, y, width, height.

- scrollIntoView() this method is used to scroll the window in the visible area.

```bash
console.log(e.target) //gives the targeted element where e comes from the event function.
console.log(e.currentTarget) //gives the current targeted element where e comes from the event function.
```

- The closest() method searches up the DOM tree for elements which matches a specified CSS selector. The closest() method starts at the element itself, then the anchestors (parent, grandparent, ...) until a match is found. The closest() method returns null() if no match is found.


### Adding JS in HTML
Regular in the head before body.

This is not good cause the browser will start parsing the JS file and user will see nothing and this will load JS before the DOM loading. parsing HTML--> fetch script--> execute-->finishing parsing HTML.
So always put the JS at the end of the body tag. Then the process will look like this parsing complete HTML--> fetch script--> execute.

```bash
<script async src="./script.js">
```
In this the process will look like parsing HTML and fetching script happens at the same time which reduces the loading time of page. but once the script is fetched it will get executed right a way.
process: pasring HTML and fetching (at same time)-->execution-->finishing parsing HTML
This is not good for the large JS files as HTML will be parsed completely but some part of the JS will be load later

```bash
<script defer src="./script.js"> 
```
In this the process will look like parsing HTML and fetching script happens at the same time which reduces the loading time of page. but once the script is fetched it will get executed at the end once the HTML is completely parsed. which is we require.
process pasring complete HTML and fetching (at same time)-->execution

- defer and async dont make sense
- async is used when order doesnt matter
- defer is used when order matters.

# 08 Asynchronous Javascript and AJAX
### Synchronous VS Asynchronous

Synchronous simply means that the code will execute line by line in the same order as we have defined in our code.
Asynchronous code executes after the task finishes in the background.
Asynchronous is non blocking
callback functions does NOT automatically make the code Asynchronous

### what is AJAX?
AJAX stands for Asynchronous javascript and XML. AJAX allows us to communicate with the remote web servers in an Asynchronous way. With AJAX calls we can request data dynamically from the web
servers.

The communication between client and web server happen Asynchronously. Like sending HTTP request to GET, POST, PUT, DELETE Data from the web server. This happens with the help of
web API.

### What is API
Application Programming Interface: In simple words API is a piece of software which is used by another piece of software in order to communicate or talk to each other.
There are several types of Web APISs such as:
DOM API, Geolocation API, Own Class API, Online API

Online API: Is simply an application running on web servers which receives requests for data and send data back as response. We also call them API / Web API.

We can build our own APIs. This include the backend development. In order to create any web app you can use the 3rd-Party APIs which you can embed in your own
API to complete your application

### XML
and XML is simple a data format which is widely used to transmit data. In Todays AGE nobody use XML data format to transmit data. Since AJAX is we old term but it still use these days. 
Now most of the Web Servers today use JSON (Javascript object notation) data format. It is simply a javascript object converted into string. Which makes it very easy to use once the data is arrived.


### CORS
Cross-origin resource sharing. Without CORS we cannot share data. It is a browser mechanism which enables controlled access to resources located outside of a given domain.


### JSON. parse()
The JSON. parse() method in JavaScript is used to parse (convert back to) a JSON string which is written in a JSON format and returns a JavaScript object. Parameters: JSON String
- JSON.parse() is used to convert a JSON string into a JavaScript object.
- JSON.stringify() is used to convert a JavaScript object into a JSON string.
- .json() is a method used in certain libraries or frameworks to extract the JSON body from an API response.

### HOW Web works request and response

The client send Http request to the web server and then the web server send the data as response. This whole process is called Request response model or Client-server- Architecture.	
The URL consist of Protocol, Domain name and resourses
Protocol://domain/resources

Domain name is actually NOT the actual address of the server. We convert the domain name into server address by DNS lookup. (DNS stands for Domain name server) DNS is a specail type of server 
with matches our domain name with the real IP address of the server. Once the domain name and IP address is matched. An TCP/IP Socket connection is established between client and web server. They decide how the data will travel accros the web. Its not good Idea to send the whole bunch of data to web server as a request and get the reponse in the same way. TCP/IP organize the way the data will transfer.
TCP = Transmission control protocol and IP= internet protocol. Protocol is simply set of rules with which two parties are allowed to communicate.

HTTP requests contains:

Start-line: HTTP method + req target + HTTP version e.g GET/ rest/v2/HTTP/1.1
HTTP request headers: it contains some info like host, language and browser info etc.
Body: The data we need

HTTP response contains 

Start-line: HTTP version + status code + status message e.g HTTP/1.1 200 OK
HTTP response headers: date, content-type, transfer-encoding
Body: The data we need (JSON OR XML)



The difference between HTTP and HTTPs is that HTTPs is encrypted with SSL and TLS. SSL (Secure Sockets Layer) encryption, and its more modern and secure replacement, TLS (Transport Layer Security) encryption, protect data sent over the internet or a computer network.



### Promise and fetch
```bash
const request = fetch('https://www.webapi.com');
console.log(request) // promise obj
```
fetch is a built in async JS function

### What is PROMISE
Its an ES6 feature
promise is simply an object that is used a placeholder for the future results of an asynchronous operation. OR informally its a container for future value. By future value we simply mean an AJAX call. 

Instead of nesting call back functions we can make a chain of promises for a sequence of asynchronous operations

### Promise LIFECYCLE
Promises work with asynchronous JS so they change their state with time. 

initial status: pending (during this state the promise remains pending and async task is working behind the scene)
Final status: settled (once the async task finishes then the promise will either get fulfilled or rejected)

We can also build promise and consume promise. But in most of the cases we consume promises. We consume the promise by using then() method in which pass a callback function. 
The argument which this callback fucntion takes is the value which will return in the future once the async task has successfuly completed and that return value is called response.
```bash
const getCountryData = function (country) {
  fetch(`https://restcountries.com/v3.1/name/${country}`)
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(err => console.err(err))
};

getCountryData('Pakistan');
```


here the response is come with JSON method which is also an async function which will also return a promise so we need to handle that promise too. So in order to handle that promise we call another callback function. Catch() method is used to handle the error.
You must remember that catch itself returns a promise.

### .finally()
This method will run either the promise is fulfilled or rejected



### Throw custom errors
```bash
const getCountryData = function (country) {
  fetch(`https://restcountries.com/v3.1/name/${country}`)
    .then(response => response.json())
    .then(response => if (!reponse.ok) throw new Error (`Country not found ${response.message})`);
	return response.json()
};
```


### Asynchronous Event Loop
If JS is a single thread language then how it is able to run multiple task at a time? How can Asynchronous code can be executed in a non blocking way?
The answer is that the asynchronous code runs in web API environment instead of call stack where it could block the code. Once the task is completed on the backend the callback function lies in callback queue its simply a queue like a to do list which has to be done in future. For example you set a timer of 5 sec. After the 5 sec the function will move from web API to callback queue. If theres no anyother callback function waiting for execution then our timer code will be executed this means that our 5 sec timer doesnt mean that this function will run right after 5 sec.
No we are not sure. But we are sure that this function will not run before 5 sec. So this all depends on the state of callback queue.
IMP point to note that callback queue also contains DOM events. Despite having the fact that the DOM events are not Async but still they use callback queue for their execution.

This means JS have no sense of time. If theres any async code then this code will not execute in the browser engine it will execute in the run time who manages all the async behaviour and its event loop who decide which callback will be executed next.

There is another queue called microtasks queue. This queue is for promises cause promises donot go to callback queue instead they go to microtasks queue.

Microtask queue have greater pirority than callback queue.This means eventloop will first check microtasks queue then callback queues
Never forget that the callbacks of promises always execute first due to micro tasks queue.

### Trick guess the output of Asynchronous code
The trick is that the synchronous code will always be executed first and will be executed line by line. But the Async code will not execute simply as we thought. In case of promises the promises will be executed frist after that the other callback functions will be executed included the DOM event.
```bash
console.log('Test Start');
setTimeout(()=> console.log('0 sec timer'), 0);
promise.resolve('Resolved Promise 1').then(res => console.log(res));

promise.resolve('Resolved Promise 1').then(res => {
for (let i=0; i<1000000; i++) {}
console.log(res)});
console.log('Test End');

// Test Start
// Test End
// Resolved Promise 1
// Resolved Promise 2
// 0 sec timer
```


### Exp2
```bash
console.log('Test Start');
setTimeout(()=> console.log('0 sec timer'), 0);
function myfunc() {Promise.resolve('Resolved Promise 1').then(res => console.log(res))
setTimeout(()=> console.log('0 sec timer 2'), 0)}

function myfunc2() {Promise.resolve('Resolved Promise 2').then(res => {
for (let i=0; i<10000000000; i++) {}
console.log(res)})};
myfunc();
myfunc2();
console.log('Test End');

// Test Start
// Test End
// Resolved Promise 1
// Resolved Promise 2
// 0 sec timer
// 0 sec timer 2
```

Explanation: As we can see that the promise 2 contains a large time taking task but no matter the promises will be executed first than anyother callback functions. Therefore, we can see the time given to the settimer function has no value over promises. Ideally 0 sec timer should be log first as it takes only 0 sec to execute but this was not the case as Async code runs on pirority principle which is decide by the event loop. Again The trick is that the synchronous code will always be executed first and will be executed line by line. But the Async code will not execute simply as we thought. In case of promises the promises will be executed frist after that the other callback functions will be executed included the DOM event.


### Building our own promises

Promises are special kind of JS objects
we can create promises as shown below:
```bash
const promise1 = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('foo');
  }, 300);
});

promise1.then((res) => {
  console.log(res);
  // Expected output: "foo"
});

console.log(promise1);
// Expected output: [object Promise]
```

Its important to note that in case of successful event the value of response would be the same value return the function on which this method is called.

Resolve and reject methods are used to immediately resolve or reject the promise. These two are also the arguments of the constructor function which create a new promise as mentioned code above.
In reject function we mostly create new error 

### Promisify
In JavaScript, promisify is a common technique used to convert asynchronous functions that follow the traditional callback pattern into functions that return promises. 
for example:

```bash
const getPosition = function () {
  return new Promise(function (resolve, rejected) {
    navigator.geolocation.getCurrentPosition(
      position => resolve(position),
      err => console.error(err)
    );
  });
};
```



### Creating async function
```bash
const whereAmI = async function(country) {
  const res = await fetch(`https://restcountries.com/v3.1/name/${country}`);
  console.log(res);
}

whereAmI('pakistan')
console.log('First')
```

async function is a function which executed async behind the scenes until its code is executing at back end.

await keyword is just another way of consuming promises. In actual old school way we simply call an async function which returns a promise and we have to deal with that promise by using then method. Moreover If we apply .json() method on the response we again get a promise and again we have to use then() method to deal with that promise. 

In the modern way we use async await to handle the promise we use await keyword and stores its value in a variable that value will be count as the response of that promise.

Async await is nothing just a different syntax for promises and its handeling. This syntax is literally a blessing this syntax prevent the formation of callback hell. Due to which the code is easy to debug, reuse and maintainable.

### Handling Errors with Try Catch
```bash
try {

} catch (err) {
	console.error(`${err.message}`)
}
```


### Getting value from async function

since we all know that async function do not run immediately. But what if we pass function as a value and then call it?
in this way you will get a promise (as we all know async function returns a promise). but if we pass that function as a value and then execute it. It will return a promise pending in console.
```bash
console.log("start")
const cool = whereAmI()
cool()
console.log("end")

//start
// promise <pending>
// end
```

Here above we have passed function as a value and then executed it. Remember is an async function


Now simply direct calling the async function
```bash
console.log("start")
whereAmI().then(res => console.log(res); 
console.log("end")

// start
// end
// response
```

**NOTE:** never run an async function without try and catch block

### Runnig async functions in parallel
you can several async functions by async await method but if the functions are dependent then the rejection of each promise will to the rejection of all promise. Therefore we often say promises are shortcicrcuits.

- promise.all() function get shortcircuit on faliure of any promise.
- whereas promise.allSettled() do not get short circuit on rejection of an event
- promise.any() this function returns a first true promises only.  

### await keyword only works on async function
this statement is true. Cause await keyword pause the execution. And this is only possible for async code/function. Remember our fetch function is built in async function.

Examples:
```bash
function myfunc(){
  for(i=0; i<100; i++){
    console.log(i);
  }
}

async function main() {
  console.log('innner above');
  await myfunc(); // here await is useless cause myfunc is not an async function
  console.log('innner below');
}

console.log('outer 2');

main();
function myfunc2(){
  console.log('function 2')
}

myfunc2();

console.log('outer 3')
```

#### Explanation:

In JavaScript, asynchronous functions are executed differently from synchronous functions. When you call an asynchronous function, it starts executing, but it doesn't block the execution of the rest of your code. Instead, it allows the code following the asynchronous function call to continue running while the asynchronous function completes its tasks.

- In your code, the function `myfunc()` is an asynchronous function, and it contains a loop that logs the values of `i`. However, since there is no asynchronous behavior within `myfunc()`, it runs synchronously and logs the values from 0 to 99.

- The `main()` function is also an asynchronous function. When you call `main()`, it starts executing, and the first line inside `main()` is to log "inner above" to the console. Then, the `await myfunc()` line is encountered.

- The `await` keyword pauses the execution of the `main()` function until the promise returned by `myfunc()` is resolved. In this case, since `myfunc()` doesn't return a promise explicitly, the JavaScript engine wraps its return value (which is `undefined`) into a resolved promise. This allows the execution of `main()` to continue.

- While `main()` is waiting for the completion of `myfunc()`, the code outside the `main()` function continues to execute. That's why you see "outer 2" being logged to the console.

- Once the loop in `myfunc()` completes logging the numbers, the execution returns to the `await myfunc()` line inside `main()`, and it proceeds to log "inner below" to the console.

- After that, the code continues to execute outside the `main()` function. Hence, you see "outer 3" being logged to the console.

To summarize, the output order is as follows:
1. outer 1
2. outer 2
3. inner above
4. 0
5. 1
6. 2
...
97. 97
98. 98
99. 99
100. inner below
101. function 2
102. outer 3

Note that the `console.log()` statement inside `myfunc2()` is executed immediately when called, so "function 2" is logged before "outer 3".


### Example 2:
```bash
async function myfunc(){
  const data = await fetch('https://restcountries.com/v3.1/name/portugal')
  console.log(data)
  for(i=0; i<100; i++){
    console.log(i); 

  }
}

async function main() {
  console.log('innner above');
  await myfunc();
  console.log('innner below');
}

console.log('outer 2');

main();
function myfunc2(){
  console.log('function 2')
}

myfunc2();

console.log('outer 3')
"
```

# 09 Best Practices to write Javascript

### General Rules to have good code:
- Use DRY principle (Do not repeat)
- Do NOT pollute global namespace
- Do NOT use var
- Use strong type check (=== and !==)

### For Functions

- Functions should do only ONE thing.
- Don't use more than 3 parameters
- use default parameters whenever possible.
- return same data type as received
- use arrow functions when they make code more readable
- Dont use arrow functions as methods as they do not have their own this keyword.


### Avoid Nested CODE:
- use early returns (guard clauses)
- Use ternary or logical operators (cause they do not create code block )instead of IF
- use multiple if instead of if/ else-if
- Avoid for loops instead use array methods
- Avoid callback-based async APIs


### Async code

- Consume promises with async  await for best readability
- whenever possible run promises in parallel (promise.all)
- Handle errors and promise rejections

### Functional Programming
- try to avoid data mutation
- Use built in methods dont produce side effects
- for data transformation use methods map, filter and reduce

### Declarative syntax
- Use array and object destructuring.
- use spread operator (...)
- use ternary (conditional) operator 
- user template literals

# 10 Closure
**Its the HARDEST Javascript concept xD**

To understand closure you must an idea about execution context, Call Stack and scope chain.
**DEFINITION:**
Closure is a closed over Execution context. Every function always have access to the variable environment of the execution context in which the function is created even
after that execution context is gone".

We do NOT create closures manually or explicitly but the they happens automatically in certain situations and we just need to recognize those situations.
Closure is strang. CLosure makes a function remember all the varaibles that existed at the functions birth place.
```bash
const secureBooking = function() {
	let passengerCount = 0;
	
	return function() {
	
	passengerCount++;
	console.log(`${passengerCount} passengers`)}
}
}

const booker = secureBooking();
// EXPECTED OUTPUT:
booker(); // 1 passengers
booker(); // 1 passengers
booker(); // 1 passengers
booker(); // 1 passengers

//ACTUAL OUTPU:
booker(); // 1 passengers
booker(); // 2 passengers
booker(); // 3 passengers
booker(); // 4 passengers
```


OH DAMNNN how is this even possible. How booker function is able to access the passengerCount variable and remeber its value despite having  the fact that its
out of the scope of secureBooking. How this function is able to update the variable 
despite having the fact that the execution of booker has finished. When ever we call booker function we call it and it get executed and then finised immediately but how
is it even possible that our next call remember the state of the previous call?

**ANSWER:** In order to understand the answer to this big question is the concept of closure. Closure makes a function to remember all the variables that existed at the function birth place. But how?

the booker function is created in global environment and added in a call stack. The secureBooking is also declared in global scope. but the function within the secureBooking 
function is not global scope. The secret is that "Every function always have access to the variable environment of the execution context in which the function is created even
after that execution context is gone".

In this case the booker was created in execution context of the secureBooking function therefore, the booker function has access to the variable environment of secureBooking. And the function which is within the secureBooking is also created in the execution of secureBooking therefore it also have access to the variable environment of secureBooking moreover the function within the secureBooking is also in the scope chain of secureBooking.

So now we can think that Closure is variable environment attached to the function, exactly as it was at the time and place the function was created.

JS engine gives greater priority to the closure as compared to scope chain. Thats why all such stuff happened.


A closure gives a function to access all the variables of its parent function, even after that 	parent function has returned. The function keeps reference to its outer scope, which 
preserves the cope chain throughout the time.

Thanks to closure which make sure thet the connection between the function and variable which existed at the functions birth place do not loose.

A closure is like a bag pack which function always keep with it where ever it goes. This Bagpack has all the variables that were present in the environment where the function was created.

To see the internal property of Closure we can use:
```bash
console.dir(booker) //closure function
```

now go to scope section of this result.

whenever you see double bracket in console.dir this means its an internal property we cannot access them.

Moreover, it not always the situation that the closure will happen only when there is a function returning another function. This wont be the case everytime.

# 11 Premitives and Objects

### Premitives
Premitives are numbers, boolean, strings, undefined, null, symbol, BigInt etc.  Permitive types are store in execution context.

When we declare a variable in call stake an identifier of the name of that variable, an address and its value are stored. When we re-assign the varibale to the another variable the newly created
variable will also point towards the same address. But when we assign a variable a new value then a completely new address along with new value is stored in the call stack.

### Objects (reference type)
Objects literal, Arrays, Functions and Many more etc. They are store on HEAP of JS Engine. 
In case of objects. when the objects are created the identifier, address are created but in value column there is reference of memory (heap). Now in Heap the reference along with the keys and values of objects are stored in HEAP. This is how objects are store because objects can be larger they cannot store in call stack therefore, they are stored in HEAP memory. In short call stack keep track where is object in heap and it will call when it is necessary.

**IMPORTANT** the values declared by the const are also mutable. This is true for the case of objects not for permitive values.
Changing values in Heap doesn't affect by let or const. The only thing which is affect by let and const is the values in call Stack. We cannot change values in call stack declared by const.
To Create a new copied object we can use:
```bash
copiedObj = Object.assign({}, myObj}
```

**REMEMBER** object.assign() only creates a shallow copy not a deep clone. Means it would copy only at the first level like if there is a nested object then the inner object wont have different
address that will remain same. For deep cloning we have to use external libraries such as loadash
```bash
b = JSON.parse(JSON.stringify(a))
```

# 12 Scoping in JS
### Scoping
Scoping means how our JS code will be oraganised and accessed by JS engine. where do varaibles live and where we can access them or not?

Scope is an environment or place where a certain variable is declared
1. Global Scope (Declared outside of any function and block and can be accessed everywhere throughout the document.
2. Function scope (Also called local scope. Functions create their own region and variables are declared in that region are only accessible inside the function NOT outside the function
3. Block scope (anything inside the curly braces will create it region. This is only true for let and const variables As let and const are block scoped. Block scope is not apply for var variables as var is function scope)

### Scope Chain:
variable in the child scope can access the variable declared in its parent scope. Note that all parent elements are children of global scope.
Inner variables can access the variables of outer variables but outer variables cannot access the inner variables. In short children can access from their parents but parents cannot access from their children.
Scope of Variable: In short its a region of our code where a certain variable is accessed.
Scope and scope of a variable both are different things.
Sibling elements cannot have access to the variables of eachother  The scope chain works upwards. neither downward nor sideway
When the code is executed first the global objects are executed then the functions (or only when they are called)
functions are also blocked scoped but only in case of strict mode

# 13 'THIS' Keyword

This keywords is a special variable points to the owner of the function. its value is not static its not always the same. It depends how the function is actually called. 
And its value will be only assigned when the function is called.

There are four ways of calling a function
1. As method (In this case the this keyword will point towards the object on which this method is called.)
2. Simple function call (In this case the this keyword will simply be undefined. Only when the strict mode is on. If the strict mode is off then this 	 keyword will point toward the windows global      object
3. Arrow function (Arrow functions donot have its own this keyword. But if you would do this then this keyword will simply point towards the this keyword of its parent element and parent element could also be global windows)
4. EventListner (in this case this keyword will point toward the DOM element that the handler function is attached to.)


This will never point the function in which we are using it. and This keyword will never point to the environment variables of the function.

**IMPORTANT:**
- Never Ever use arrow functions inside objects (means dont use them as method)
- Always use let and const instead of var.
- It doesnt mean that under which function or object the this keyword is declared it will always point toward that object. NO its not true. Actually it will point toward the object which is calling the method.

For example:
```bash
const jonas = {
  year : 1991,
  calcAge: function() {
    console.log(this);
    console.log(2037-this.year);
  }
}

const matilda = {
  year : 2017,

  }


  matilda.calcAge = jonas.calcAge //borrowing the method

  matilda.calcAge() //Answer would be 20 here as matilda is calling the method therefore this keyword will point towards matilda object not jonsa

```

- var creates variable in windows global object and function declared by var donot have arguments keyword.

- A regular function have arguments keywordS

# 14 Hoisitng in Javascript
**Hoiting means:** Variables lifted at top of their scope.
**Behind the scenes:** Before execution the whole code is scanned and a new property for each new variable is created in variable environmental object.

**Functions are hoisted:** Means we can use function declaration even before they are declared.
var variables are also hoisted: but if you will use var declaration even before they are declared you will get undefined. 				Its not very useful due to its weird behaviour.
let and const are not hoited (but techincally yes): if you will use var declaration even before they are declared you will 						    get uninitialized. Its not very useful due to its weird behaviour.

**Function expressins are NOT hoisted:** Means we cannot use function expression even before they are declared.


variables created with var creates porperty in window object. Whereas let and const dont

### TDZ (Temporal Dead Zone)
This makes it easier to catch error: accessing variables before declaration is a bad practice and should be avoided.
it makes the variables to work as they are actually supposed to.
As const cannot re-assigned

# 15 Modern Javascript and Development 
In actual we do not write a whole script and send to browser for the production. Instead we use modules our own custom build modules or 3rd party modules which we download with the help of Node package manager. Once our project is ready we make bundle of our code. Which is also done by some 3rd part open source frame works or libraries such as parcel. Parcel is JS bundler which bundle our code and also with the help of babel we convert it back to ES5 for all browser compatiblity. The whole process is called build process in which we make package.json file which keep record of all the modules used in our project. 

### Module
Its a reusable piece of code. It basically a stand alone file. Its not always the same case. 
Whatever we export from the module is called public API. Whatever we import in the module is called dependencies without which our code is dead. One can work on a single component/module of a project without knowing that how the whole app work. This help teams to work in easy way


### Difference between ES6 module and Script

There is a lot of difference between them:
1. In Modules top level variables are Scoped to modules whereas in script these variables are global.
2. ES6 module defualt mode is strict whereas in script the default mode is sloppy mode.
3. This keyword is undefined in ES6 module, whereas this keyword is window object in script
4. Imports exports are allowed in ES6 in script NO.
5. HTML link the type is module. For script HTML are simple linked.
6. Files are downloaded asynchronously in ES6 whereas in script it down.

### BTS of Import export

Modules are imported sychronously. First all the imports are known before the execution of code. This makes bundling and dead code elimination easier. The downloading of the module happen asynchronously afer downloading the import is connected with export. 

You cannot access the variable of any other module into your module until you export them from the export module and import them from in the import module.

### Module pattern

In this pattern you simply return the variables defined within the scope of the function to the Immediately invode function so that these variables can also be accessed outside the function.
for example:
```bash
const ShoppingCart = function(){
const cart = 20;
const shippingCost =50;
console.log("I am a function");
return {
	cart,
	shippingCost
}
}
console.log(ShoppingCart().cart);
```


Here you can see the cart object is out of scope but still we have accessed it by the help of module pattern. Actually we have returned it in the function

### CommonJS is simply a standard to have common pattern in all JS around the world
like importing variales using require this will only work with node.
This wont work in browsers
```bash
const {addToCart} = require("./shoppinCart.js");
```


### NPM

To manage our dependencies in a good way we can use NPM 


### Imperative VS Declarative Code Paradigms
In Imperative we explain computer "how to do" things. We explain computer every single step it has to follow to achieve a result.

In declarative: We tell "what to do"

Functional programming is also declarative and modern way in which we write the program by using many pure functions, avoiding side effects and mutating data.
Pure function is a function which have no side effects and its not depened on any other variable and always return the same value on same input. A side effect is when a function relies on, or modifies, something outside its parameters to do something.


### Parcel Bundling and deployment in JS
**NOTE:** also remove the type="module" from the script tag in index.html file
```bash
npm install parcel --save-dev
```
or 
```bash
sudo npm install parcel
```
```bash
npx parcel index.html 
```
This will make the bundle behind the scene and this also work as live-server.

now go to package.json and write in start: "parcel index.html"
```bash
build: "parcel build index.html --dist-dir ./dist"
```


and set main to default as below:
```bash
"default" : "index.html"
```

now run the below:
```bash
npm run build
```

then push it to gitHub

parcel automatically use babel so we dont have to need worry about polyfil and transpile. But recently babel has strated recommending another library for polyfilling that is cors-js which make sure that the specific code is supported by the browser or not.


