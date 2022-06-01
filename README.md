Q1. What are JavaScript Data Types?
Ans -> There are Two data types 
1.Primitive Data Types
2.Non-Primitive Data Types


Q2. Primitive and Non Primitive data types?
Ans ->
1.Primitive Data Types-
>there are many data types
-string
-boolean
-int
-number
-undefined
-symbol
-null

2.Non-Primitive Data Types.
>there are some data types
-Array
-object
-RegExp

Q3. What is the use of NaN function?
Ans ->
NaN is also Called a Not A Number,basically is called a global scope.
and also NaN returns a true value if value is none and NaN() methods converts the value of number before testing it. 

Q4. What are Undefined and undeclared variable?
Ans ->

1. Undeclared -> It Occurs when a variable hasn't been declared using var,let or const and has been trying to access.
2. Undefined -> It Occurs when a variable has been declared using var,let or const but its not given a value.

Q5. Why JavaScript Called a dynamically typed language?
Ans -> javascript called a dynamic typed language because it dosen't have few dynamic aspects,there are pretty much dynamic variable. and it also given a new variable at
a runtime and also the type of variable determined a runtime. 

Q6. What is the difference between var and let?
Ans -> var => var is a functional scope here,we can redeclare a value.
ex.
input:-

console.log(x); 
var x = 15;
console.log(x);

output:-
>output
 15

let => let is a block scope here, we can not redeclare a value.

input:-

console.log(x); 
var x = 15;
console.log(x);

output:-
>Reference error///

Q7. What is 'this' keyword use in javascript?
Ans -> the 'this' keyword is refers to current object in a method or constructor.
ex.
input:-

const person = {
  firstName: "Aniket",
  lastName : "Vishwakarma",
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
 output:-
>Aniket Vishwakarma

Q8. Explain the difference between "==" and "==="?
Ans -> "==" is used to comparison between two variable irrespective of the datatype variable.
"===" is used to comparisonn between two variable ,but this will check strict type,which means it will check datatype and compared two values.

Q9. What is the significance of, and reason for, wrapping the entire content of a JavaScript source file in a function block? 
Ans -> The purpose of wrapping is to a namespace and control the visibility of member functions. It wraps the code inside a function scope and decreases clashing with other libraries.

Q10.  Discuss possible ways to write a function isInteger(x) that determines if x is an integer?
Ans ->
function isInteger(x){
var is_number = typeof x == "number";
var is_not_a_float = String(x).indexOf('.') == -1;
return is_number && is_not_a_float;
}

Q11. Write a simple function (less than 160 characters) that returns a boolean indicating whether or not a string is a palindrome.
Ans -> function isPalindrome(str) {
  str = str.replace(/\W/g, '').toLowerCase();
  return (str == str.split('').reverse().join(''));
}
For example:

console.log(isPalindrome("level")); // logs 'true'
console.log(isPalindrome("levels")); // logs 'false'
console.log(isPalindrome("A car, a man, a maraca")); // logs 'true'

Q12. What is a “closure” in JavaScript? Provide an example.
Ans -> A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives
you access to an outer function's scope from an inner function.

Q13.  Create a function that, given a DOM Element on the page, will visit the element itself and all of its descendents (not just its immediate children). For each element visited, the function 
should pass that element to a provided callback function.

The arguments to the function should be:

a DOM element
a callback function (that takes a DOM element as its argument)
Ans -> 
function Traverse(p_element,p_callback) {
p_callback(p_element);
var list = p_element.children;
for (var i = 0; i < list.length; i++) {
Traverse(list[i],p_callback); // recursive call
}
}

Q14. How do you add an element at the begining of an array? How do you add one at the end?
Ans -> 
function ArrayOfUnShift (arr,ele){
    arr.unshift(ele);
    return arr;
}
const arr = [10,20,30,40];
console.log(ArrayOfUnShift(arr,50));

Q15. What is the value of typeof undefined == typeof NULL?
Ans -> 
var myVar=null;

if(myVar === null){ //I am null; }

if (typeof myVar === 'undefined'){ //myVar is undefined }

Q16.  What is functional programming?
Ans -> Functional programming is a programming paradigm in which we try to bind everything in pure mathematical functions style.
It is a declarative type of programming style..

Q17. What are the pros and cons of functional programming vs object-oriented programming?
Ans -> FP-prons and cons
* Using clean and transparent functions leads to reliable results without side effects that deliver and return exactly what you expect.

* It uses a more declarative style that focuses more on what needs to be done and less on how to do it, with an emphasis on efficiency and optimization.

- It is a relatively new paradigm and sometimes it is not so easy to find documentation or information compared to Object-oriented Programming.

– Sometimes it may not become illegible due to a very large number of functions compared to Object-oriented Programming.

Objects and methods are very clear and understandable.

Use an imperative style, in which the code is read like a simple set of instructions, just like a computer would read it.


Q18. What are two-way data binding and one-way data flow, and how are they different? 
Ans -> 
1. one-way data binding -> in one-way binding the flow is one-directional.this means that the flow of code is from JS file to HTMl file..

2. two-way data binding -> In a two-way binding, the flow is two-directional.This means that the flow of code is from JS file to Html file as well as from Html file to JS file.

Q19. What is asynchronous programming, and why is it important in JavaScript?
Ans -> Asynchronous programming makes it possible to express waiting for long-running actions without freezing the program during these actions. JavaScript environments typically implement this style of programming using callbacks, 
functions that are called when the actions complete.
