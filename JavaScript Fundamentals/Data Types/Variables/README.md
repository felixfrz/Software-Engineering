# Variables

Variables are used to store information to be referenced and manipulated in a computer program. They also provide a way of labeling data with a descriptive name, so our programs can be understood more clearly by programmers. It is helpful to think of variables as containers that hold information. Their sole purpose is to label and store data in computer memory. This data can then be used and even changed throughout the lifetime of your program.

## When you finish this reading, you should be able to:

1. declare variables using the `let` keyword
2. assign values to variables using the assignment operator (=)
3. use the shortcuts +=, -=, ++, -- to reassign variables
4. identify undefined as the default value for unassigned variables

## Initializing a variable

To initialize a variable in JavaScript we'll need two new pieces of syntax: `let` and `=`. We can give the variable any name that we wish and assign it a value. Once we initialize a variable, the variable will evaluate to the value assigned:

```javascript
let myName = "Ayodeji Felix Oladoyin";
console.log(myName); // 'Ayodeji Felix Oladoyin'

let birthYear = 2023;
console.log(birthYear); // 2023
```

**Did you know?** JavaScript variables names can contain any alphanumeric characters, underscore (_), or dollar sign ($). However, they cannot begin with a number.

Above are examples of how you'll create variables most of the time, so we'll grow very familiar with the syntax. As a best practice, we should name our variables in a way that is descriptive and concise.

The variable initializations above really consist of two steps: declaration with let and assignment with =. Let's break these two steps down.

## Declaring a variable


In JavaScript, in order to use a variable, we must declare it. Variable declaration is the act of introducing the variable to the environment.

To declare a variable, use the let keyword, followed by a space and then the name of the variable.

let bootcamp;
console.log(bootcamp); // undefined
Once a variable is declared, it will contain undefined as its value. undefined is a common default value in JavaScript, and we'll see it come up in a few different places. You can think of undefined as showing that the variable is empty.

Assigning a variable
Once a variable has been declared, we can assign it a value using single-equals = :

let bootcamp;
console.log(bootcamp); // undefined
bootcamp = "App Academy";
console.log(bootcamp); // 'App Academy'
Manipulating variables
To change the value of a variable, we need to reassign it to a new value with = :

let num = 42;
console.log(num + 8); // => 50
console.log(num); // => 42

num = num + 10;
console.log(num); // => 52
In the code above, num + 8 will evaluate to 50, but it will not change the num variable to 50. If we want to change the num variable, we must reassign to it.

Assignment Shorthand
Changing the value of a number variable is something fairly common in the programming world. Luckily there is some shorthand operators we can use:

let number = 0;
number += 10; // equivalent to number = number + 10
number -= 2; // equivalent to number = number - 2
number /= 4; // equivalent to number = number / 4
number *= 7; // equivalent to number = number * 7
console.log(number); // 14
We also have other shorthand to add or subtract exactly 1 from a variable, the increment (++) and decrement (--) operators:

let year = 3004;
year++;
console.log(year); // 3005
year--;
console.log(year); // 3004
NaN
Now that we have the ability to perform arithmetic with variables, let's take a look at a common programming mistake, getting a result of NaN (not a number):

let num;
console.log(num + 3); // NaN
The above code gives NaN because the unassigned num variable contains undefined; adding 3 to undefined results in NaN. In general, any nonsensical arithmetic will result in NaN. Math operations involving undefined is perhaps the most common mistake:

console.log(undefined + 3); // NaN
console.log("fish" * 2); // NaN
What you've learned
variables are declared with let and will contain the value undefined by default
we can use a single-equals = to assign variables
changing a variable requires a reassignment, for which there are many shortcuts (+=, -=, etc.)