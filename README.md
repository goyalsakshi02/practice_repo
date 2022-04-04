# Java Script Learning Module 
## Variables
- Variables are stored in a memory .
- Variables hold reusable data in a program and associate it with a name.
There are three types of variables:-
- ** var **   : Used in the previous versions of ES6.
- ** let **   : let is the preferred way to declare a variable when it can be reassigned
- ** const ** : It is the preferred way to declare a variable with a constant value.
## Functons 
### Definition of Funtion 
 A function is a reusable block of code that groups together a sequence of statements to perform a specific task.
 ### Function Declarations
 In Javascript one way to create a function is by using a function declarations, a function declaration binds a function to a name, or an identifier.
 A function declaration consist of :
 - The function keyword.
 - The name of the function, or its identifier, followed by parentheses.
 - A function body, or the block of statements required to perform a specific task, enclosed in the function’s curly brackets.
 #### For example 
 ```
 function greetWorld() {
  console.log('Hello, World!');
}

greetWorld(); // Output: Hello, World
```
### Calling a Function 
A function declaration does not ask the code inside the function body to run,  it just declares the existence of the function.The code inside a function body runs, or executes, only when the function is called. one can call function as many times it needed. 
#### For Example 
``` 
function sayThanks() {
  console.log('Thank you for your purchase! We appreciate your business.')
}
sayThanks()
sayThanks()
sayThanks() 
```
#### Output
>- Thank you for your purchase! We appreciate your business.
 - Thank you for your purchase! We appreciate your business.
 - Thank you for your purchase! We appreciate your business.
### Parameters and Arguments 
#### Parameters 
Functions can take inputs and use the inputs to perform a task. While declaring a function, we can specify its parameters. Parameters allow functions to accept input(s) and perform a task using the input(s). We use parameters as placeholders for information that will be passed to the function when it is called.
#### Arguments
When calling a function that has parameters, we specify the values in the parentheses that follow the function name. The values that are passed to the function when it is called are called arguments. Arguments can be passed to the function as values or variables.
### For Example
```
function sayThanks(name) {
  console.log('Thank you for your purchase ' + name + '! We appreciate your business.');
}

sayThanks('Cole'); 
```
#### Output
> - Thank you for your purchase Cole!.
   - We appreciate your business.
### Default Parameters 
In ES6 we can use default parameters. Allow parameters to have a predetermined value in case there is no argument passed into the function.
#### For Example
``` 
function greeting (name = 'stranger') {
  console.log(`Hello, ${name}!`)
}
 
greeting('Nick')
greeting()
```
>  - Hello, Nick!
   - Hello, stranger!
### Return 
The return keyword is powerful because it allows functions to produce an output. We can then save the output to a variable for later use.
### For Example
```
function rectangleArea(width, height) {
  if (width < 0 || height < 0) {
    return 'You need positive integers to calculate area!';
  }
  return width * height;
}
rectangleArea(3 , 4)
```
#### Output 
> 12
### Helper Function
Using a return value of a function inside a another function are reffered to as helper function .
#### For Example
If we wanted to define a function that converts the temperature from Celsius to Fahrenheit, we could write two functions like:
```
function multiplyByNineFifths(number) {
  return number * (9/5);
};
 
function getFahrenheit(celsius) {
  return multiplyByNineFifths(celsius) + 32;
};
 
getFahrenheit(15);
```
### Output 
> 59
### Function Expressions 
#### To define a function inside an expression 
In a function expression, the function name is usually omitted. A function with no name is called an anonymous function. A function expression is often stored in a variable in order to refer to it.
```
const calculations = function(width , height) {
    const area = width * height;
    return area;
} 
```
### Arrow Functions 
In ES6 a shorter way to write a function by using a <mark>fat arrow () =></mark> . It remove the need to type the keyword function.
#### For Exmaple
```
const rectangleArea = (width, height) => {
  let area = width * height;
  return area;
}; // function returns area 
```
Refactoring the other function to :
```
const squareNum = num => num * num;
```
Changes that follows in the above code are:
-The parentheses around num have been removed, since it has a single parameter.
-The curly braces { } have been removed since the function consists of a single-line block.
-The return keyword has been removed since the function consists of a single-line block.



