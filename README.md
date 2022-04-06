# Java Script Learning Module 
## Variables
- Variables are stored in a memory .
- Variables hold reusable data in a program and associate it with a name.
There are three types of variables:-
- ** var **   : Used in the previous versions of ES6.
- ** let **   : let is the preferred way to declare a variable when it can be reassigned
- ** const ** : It is the preferred way to declare a variable with a constant value.
```
const y = 10
console.log(y) // 10
y = 20 
console.log(y) // 10
```
```
let x = 10
console.log(x) // 10
x = 20 
console.log(x) // 20
```
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
 - Thank you for your purchase! We appreciate your business.
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
- Thank you for your purchase Cole!.
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
   - Hello, Nick!
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
#### Detailed Example 
```
function convertString(word) {
    let part = word.slice(1)
    let firstLetter = word[0].toUpperCase()
    console.log(`${firstLetter}${part}` )
}
let word = 'i love dog'
const outPrint = convertString(word)
console.log(outPrint)
```
#### Output
I love dog
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
### Example 2
```
const reverseNumFunc = () => {
let num = 1234
let reversedNum = 0
while (num != 0 ) {
    digit = num % 10
    reversedNum = reversedNum * 10 + digit
    num = Math.floor(num / 10) 
}
return reversedNum
}
console.log(reverseNumFunc())
```
#### Example 3
```
const noOfVowels = string => {
  let vowels = 'aAeEiIoOuU'
  let vowelCount = 0
  for (let i=0 ; i< string.length ; i++){
    
    for (let j=0 ; j< vowels.length ; j++){
      
      if(string[i] === vowels[j]){
        vowelCount += 1
      }
    }
  }
  return vowelCount
}

console.log(noOfVowels('Dont let fear interfere')) // output : 8
```
Refactoring the other function to :
```
const squareNum = num => num * num;
```
```
const cubeOfnum = num => num * num *num ;
console.log(cubeOfNum(8)) // output : 512
```
Changes that follows in the above code are:
- The parentheses around num have been removed, since it has a single parameter.
- The curly braces { } have been removed since the function consists of a single-line block.
- The return keyword has been removed since the function consists of a single-line block.
## Scope
Scope determines the accessibility (visibility) of variables.

JavaScript has 3 types of scope:

  - Block scope : Variables declared inside a { } block cannot be accessed from outside the block
  ```
  const bird = {
    let Bird1 = 'Sparrow'
  }
  ```
  The bird variable inside a block is referred to as block scope
  - Function scope : Variables defined inside a function are not accessible from outside the function.
  
  ```
  function myFunction() {
    var carName = "Volvo";   // Function Scope
  }
  ```
the carName variable referred to as Function Scope
  - Global scope : A variable declared outside a function, becomes GLOBAL
```
  let carName = "Volvo";
// code here can use carName

function myFunction() {
// code here can also use carName
}
```
  the global variable can be accesses anywhere in the code.
### Arrays 
An array is a special variable, which can hold more than one value
```
const cars = [volvo, swift, Hondacity]

```
### Use of Array 
An array can hold a collection of data in a single variable which can be accessed very easily by reffering to an index number.
Array element can be accessed by reffering to the index number:
```
const cars = ["Saab", "Volvo", "BMW"];
console.log(cars[0]); // output : Saab 
```
### Replacing an Element in Array 
We can replace any element in array with the new value easily 
```
const cars = ['swift', 'Hondacity', 'Baleno']
cars[0] = Nexa
console.log(cars) // Output : Nexa, Hondacity, Baleno
```
### Array properties 
by built in properties and methods its very easy to access array 
- The length property : This property returns the length of the array 
``` 
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.length;
console.log(length) // 4
```
- Accessing last element of array 
```
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits[fruits.length - 1];
console.log(fruit) // output : 3
```
- Push and Pop : using these properties can easily remove and insert array elements 
Example for push : 
```
const chores = ['wash dishes', 'do laundry', 'take out trash'];
chores.push('item3', 'item4')
console.log(chores) // output :  ['wash dishes', 'do laundry', 'take out trash', 'item3''item4']
```
Example for Pop :It only remove the last element of the array 
```
const chores = ['wash dishes', 'do laundry', 'take out trash', 'cook dinner', 'mop floor']
chores.pop()
console.log(chores) // Output : ['wash dishes', 'do laundry', 'take out trash', 'cook dinner']
```
- More inbuilt methods : shift, unshift, slice, indexOff
```
const groceryList = ['orange juice', 'bananas', 'coffee beans', 'brown rice', 'pasta', 'coconut oil', 'plantains'];

groceryList.shift();

console.log(groceryList);

groceryList.unshift('popcorn');

console.log(groceryList);

console.log(groceryList.slice(1, 4));

console.log(groceryList);

const pastaIndex = groceryList.indexOf('pasta');

console.log(pastaIndex);
```
#### Output
>   
    ['bananas', 'coffee beans', 'brown rice', 'pasta', 'coconut oil', 'plantains']
  
    ['popcorn','bananas', 'coffee beans', 'brown rice', 'pasta', 'coconut oil', 'plantains']

    [ 'bananas','coffee beans', 'brown rice']

    4
      

- Looping Array Element : Using for loop in an array.
``` 
const fruits = ["Banana", "Orange", "Apple", "Mango"];
const fl = fruits.length
let text = "<ul>"
for (i=0; i< flen; i++) {
text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";
console.log(text) 
```
#### Output
>  
   - Banana
   - Orange
   - Apple
   - Mango
#### Iterators



    



