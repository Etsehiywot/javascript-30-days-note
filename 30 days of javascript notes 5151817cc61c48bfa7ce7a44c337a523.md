# 30 days of javascript notes

### **Javascript**

JavaScript (JS) is a cross-platform, object-oriented programming language used by developers to make web pages interactive. It allows developers to create dynamically updating content, use animations, pop-up menus, clickable buttons, control multimedia, etc. The use of JavaScript can be both on the client-side and server-side. While [HTML and CSS](https://www.simplilearn.com/tutorials/html-tutorial/html-vs-css) languages are used to give structure and style to web pages, JavaScript is used to add interactive elements that engage users. Without JavaScript, 90% of Internet webpages would be static.

javascript is a scripting language that enables us to create dynamically updating content, control multimedia, animate images, and pretty much everything else and it allows client-side script to interact with the user and make dynamic pages.

JavaScript is used ***to add interactivity to websites, to develop mobile apps, desktop applications, games*** and nowadays JavaScript can be used for **server-side programming**, ***machine learning*** and ***AI***. and it is usually embedded directly into HTML pages

### **How to run javascript code?**

first we download node.js then we write small JavaScript code on the browser console(we can open Google Chrome console either by clicking three dots at the top right corner of the browser, selecting *More tools -> Developer tools* or using a keyboard shortcut(`Ctl+Shift+J`)).

**Console.log**

To write our first JavaScript code, we used a built-in function **console.log(),that used to display data.**

We passed an argument as input data, and the function displays the output. We passed `'Hello, World'` as input data or argument in the console.log() function.

`console.log('Hello, World!')`

The **`console.log()`** function can take multiple parameters separated by commas. The syntax looks like :**`console.log(param1, param2, param3)`.**

**comments**

Comments are very important to make code more readable and to leave remarks in our code.

Single Line Comment

`// This is the first comment`

Multiline Comment

`/*
This is a multiline comment  
 Multiline comments can take multiple lines  
 JavaScript is the language of the web  
 */`

**syntax:-** syntax is the structure of statements in a computer language.

**Arithmetics**

we can also do mathematical calculations using JavaScript.

```
console.log(2 + 3) // Addition
console.log(3 - 2) // Subtraction
console.log(2 * 3) // Multiplication
console.log(3 / 2) // Division
console.log(3 % 2) // Modulus - finding remainder
console.log(3 ** 2) // Exponentiation 3 ** 2 == 3 * 3
```

## Adding JavaScript to a Web Page

JavaScript can be added to a web page in three different ways:

- ***Inline script***

Create a project folder on your desktop or in any location, name it first js and create an ***index.html*** file in the project folder. Then paste the following code and open it in a browser

For example:

`<!DOCTYPE html><html lang="en">
  <head>
    <title>first js Script</title>
  </head>
  <body>
    <button onclick="alert('Welcome to java script!')">Click Me</button>
  </body>
</html>`

- ***Internal script***

The internal script can be written in the *head* or the *body*, but it is preferred to put it on the body of the HTML document. First, let us write on the head part of the page

`<!DOCTYPE html><html lang="en">
  <head>
    <title>first js Script</title>
    <script>
      console.log('Welcome to java script!')
    </script>
  </head>
  <body></body>
</html>`

- ***External script***

the external script link can be on the header or body, but it is preferred to put it in the body. First, we should create an external JavaScript file with .js extension. All files ending with .js extension are JavaScript files. Create a file named introduction.js inside your project directory .

`<!DOCTYPE html>
<html lang="en">
  <head>
    <title>first js Script</title>
  </head>
  <body>
   
    <script src="introduction.js"></script>
  </body>
</html>`

- ***Multiple External scripts***

External scripts are **practical when the same code is used in many different web pages**.

```
<!DOCTYPE html><html lang="en">
  <head>
    <title>Multiple External Scripts</title>
  </head>
  <body>
    <script src="./helloworld.js"></script>
    <script src="./introduction.js"></script>
  </body>
</html>
```

### **Introduction to Data types**

Data types describe the characteristics of data.

Data types can be divided into two:

1. Primitive data types
2. Non-primitive data types(Object References)

**Primitive Data Types**

Primitive data types are immutable(non-modifiable) data types. Once a primitive data type is created we cannot modify it. they are compared by its value. it is a single simple data value with no additional properties and methods.

Primitive data types in JavaScript include:

1. Numbers - Integers, floats
2. Strings - Any data under single quote, double quote or backtick quote
3. Booleans - true or false value
4. Null - empty value or no value
5. Undefined - a declared variable without a value
6. Symbol - A unique value that can be generated by Symbol constructor.

Example:

```
let numOne = 3
let numTwo = 3

console.log(numOne == numTwo)      // true

let js = 'JavaScript'
let py = 'Python'

console.log(js == py)             //false
```

**Non-Primitive Data Types**

Non-primitive data types are modifiable or mutable. We can modify the value of non-primitive data types after it gets created. they cannot be compared by value. Even if two non-primitive data types have the same properties and values, they are not strictly equal,because they are being compared by reference instead of value.Two objects are only strictly equal if they refer to the same underlying object.

Non-primitive data types in JavaScript includes:

1. Objects
2. Arrays

Example:

```
let nums = [1, 2, 3]
let numbers = [1, 2, 3]

console.log(nums == numbers)  // false

let userOne = {
name:'Etsehiywot',
role:'student',
country:'Ethiopia'
}

let userTwo = {
name:'Etsehiywot',
role:'Student',
country:'Ethiopia'
}

console.log(userOne == userTwo) // false
```

some types of premitive datatypes:

**Numbers:**

Numbers are integers and decimal values which can do all the arithmetic operations.

Declaring Number Data Types

`let age = 21
const gravity = 9.81  // we use const for non-changing values, gravitational constant in  m/s2
let mass = 72         // mass in Kilogram
const PI = 3.14       // pi a geometrical constant

// More Examples
const boilingPoint = 100 // temperature in oC, boiling point of water which is a constant
const bodyTemp = 37      // oC average human body temperature, which is a constant

console.log(age, gravity, mass, PI, boilingPoint, bodyTemp)`

**Math Object**

In JavaScript the Math Object provides a lots of methods to work with numbers.

```
const PI = Math.PI

console.log(PI)                            // 3.141592653589793

// Rounding to the closest number
// if above .5 up if less 0.5 down rounding

console.log(Math.round(PI))                // 3 to round values to the nearest number

console.log(Math.round(9.81))              // 10

console.log(Math.floor(PI))                // 3 rounding down

console.log(Math.ceil(PI))                 // 4 rounding up

console.log(Math.min(-5, 3, 20, 4, 5, 10)) // -5, returns the minimum value

console.log(Math.max(-5, 3, 20, 4, 5, 10)) // 20, returns the maximum value

const randNum = Math.random() // creates random number between 0 to 0.999999
console.log(randNum)

// Let us  create random number between 0 to 10

const num = Math.floor(Math.random () * 11) // creates random number between 0 and 10
console.log(num)

//Absolute value
console.log(Math.abs(-10))      // 10

//Square root
console.log(Math.sqrt(100))     // 10

console.log(Math.sqrt(2))       // 1.4142135623730951

// Power
console.log(Math.pow(3, 2))     // 9

console.log(Math.E)             // 2.718

// Logarithm
// Returns the natural logarithm with base E of x, Math.log(x)
console.log(Math.log(2))        // 0.6931471805599453
console.log(Math.log(10))       // 2.302585092994046

// Returns the natural logarithm of 2 and 10 respectively
console.log(Math.LN2)           // 0.6931471805599453
console.log(Math.LN10)          // 2.302585092994046

// Trigonometry
Math.sin(0)
Math.sin(60)

Math.cos(0)
Math.cos(60)
```

**Random Number Generator**

The JavaScript Math Object has a random() method number generator which generates number from 0 to 0.999999999...

`let randomNum = Math.random() // generates 0 to 0.999...`

Example for generating a random number between 0 and 10:

```
let randomNum = Math.random()         // generates 0 to 0.999
let numBtnZeroAndTen = randomNum * 11

console.log(numBtnZeroAndTen)         // this gives: min 0 and max 10.99

let randomNumRoundToFloor = Math.floor(numBtnZeroAndTen)
console.log(randomNumRoundToFloor)    // this gives between 0 and 10
```

**Strings**

Strings are texts, which are under ***single*** , ***double***, ***back-tick*** quote. To declare a string, we need a variable name, assignment operator, a value under a single quote, double quote, or backtick quote. Let's see some examples of strings:

```
let space = ' '           // an empty space string
let firstName = 'Etsehiywot'
let lastName = 'Dereje'
let country = 'Ethiopia'
let city = 'Addis Abeba'
let language = 'JavaScript'
let job = 'Student'
let quote = "The saying,'Seeing is Believing' is not correct in 2020."
let quotWithBackTick = `The saying,'Seeing is Believing' is not correct in 2020.`
```

**String Concatenation**

Connecting two or more strings together is called concatenation. Using the strings declared in the previous String section:

`let fullName = firstName + space + lastName; // concatenation, merging two string together.
console.log(fullName);`

**Concatenating Using Addition Operator**

its an old way which is is tedious and error-prone. ES6 template strings are more preferable than it.

**Long Literal Strings**

A string could be a single character or paragraph or a page. If the string length is too big it does not fit in one line. We can use the backslash character (\) at the end of each line to indicate that the string will continue on the next line. **Example:**

`const paragraph = "My name is Etsehiywot Dereje. I live in Ethiopia, Addis Abeba.\
I am a student and I love learning. I learn  HTML, CSS, JavaScript,\
Node.js, Python, Data Analysis  \
I love learning. \
I hope you are enjoying what you learn  too."

console.log(paragraph)`

**Escape Sequences in Strings**

In JavaScript and other programming languages \ followed by some characters is an escape sequence. Let's see the most common escape characters:

- \n: new line
- \t: Tab, means 8 spaces
- \\: Back slash
- \': Single quote (')
- \": Double quote (").

**Template Literals (Template Strings)**

To create a template strings, we use two back-ticks. We can inject data as expressions inside a template string. To inject data, we enclose the expression with a curly bracket({}) preceded by a $ sign.

Example:

```
console.log(`The sum of 2 and 3 is 5`)              // statically writing the data
let a = 2
let b = 3
console.log(`The sum of ${a} and ${b} is ${a + b}`) // injecting the data dynamically
```

### String Methods

Everything in JavaScript is an object. A string is a primitive data type that means we can not modify it once it is created. The string object has many string methods. There are different string methods that can help us to work with strings:

- ***length***: returns the number of characters in a string included empty space.
- ***Accessing characters in a string***: We can access each character in a string using its index(starting from 0).
- ***toUpperCase()***: this method changes the string to uppercase letters.
- ***toLowerCase()***: this method changes the string to lowercase letters.
- ***substr()*:** It takes two arguments, the starting index and number of characters to slice.
- ***substring()***: It takes two arguments, the starting index and the stopping index but it doesn't include the character at the stopping index.
- ***split()*:** The split method splits a string at a specified place.
- ***trim()*:** Removes trailing space in the beginning or the end of a string.
- ***includes()*:** It takes a substring argument and it checks if substring argument exists in the string. *includes()* returns a boolean. If a substring exist in a string, it returns true, otherwise it returns false.(it is case sensitve).
- ***replace()***: takes as a parameter the old substring and a new substring.
- ***charAt()***: Takes index and it returns the value at that index.
- ***charCodeAt()***: Takes index and it returns char code (ASCII number) of the value at that index.
- ***indexOf()***: Takes a substring and if the substring exists in a string it returns the first position of the substring if does not exist it returns -1.
- ***lastIndexOf()***: Takes a substring and if the substring exists in a string it returns the last position of the substring if it does not exist it returns -1.
- ***concat()*:** it takes many substrings and joins them.
- ***startsWith*:** it takes a substring as an argument and it checks if the string starts with that specified substring. It returns a boolean(true or false).
- ***endsWith***: it takes a substring as an argument and it checks if the string ends with that specified substring. It returns a boolean(true or false).
- ***search***: it takes a substring as an argument and it returns the index of the first match. The search value can be a string or a regular expression pattern.
- ***match***: it takes a substring or regular expression pattern as an argument and it returns an array if there is match if not it returns null. Let us see how a regular expression pattern looks like. It starts with / sign and ends with / sign.
- ***repeat()*:** it takes a number as argument and it returns the repeated version of the string.

## Checking Data Types and Casting

### Checking Data Types

In JavaScript there are 5 different data types that can contain values:

- string
- number
- boolean
- object
- function

There are 6 types of objects:

- Date
- Array
- String
- Number
- Boolean

And 2 data types that cannot contain values:

- **null**: doesn’t have value.

```
let empty = null
console.log(empty) // -> null , means no value
```

- **undefined:** If we declare a variable and if we do not assign a value and if a function is not returning the value, it will be undefined.

```
let firstName
console.log(firstName) //not defined, because it is not assigned to a value yet
```

we can use the typeof operator to find or to check the data type of a JavaScript variable.

Example:

`typeof "Etsehiywot"                 // Returns "string"`

`typeof 3.14                   // Returns "number"`

`typeof NaN                    // Returns "number"`

`typeof false                  // Returns "boolean"`

`typeof [1,2,3,4]              // Returns "object"`

`typeof {name:'Etsehiywot', age:21}  // Returns "object"`

`typeof new Date()             // Returns "object"`

`typeof function () {}         // Returns "function"`

`typeof job                // Returns "undefined" *`

`typeof null                   // Returns "object"`

- we cannot use typeof to determine if a JavaScript object is an array (or a date).

### **Changing Data Type (Casting)**

Casting is Converting one data type to another data type.

- We use *parseInt()*, *parseFloat()*, *Number()*, *+ sign*, *str().*
- When we do arithmetic operations string numbers should be first converted to integer or float if not it returns an error.

### String to Int

We can convert string number to a number. Any number inside a quote is a string number.

We can convert string to number using:

• parseInt():

```
let num = '20'
let numInt = parseInt(num)
console.log(numInt) // 20
```

• Number():

```
let num = '20'
let numInt = Number(num)

console.log(numInt) // 20
```

• Plus sign(+):

```
let num = '20'
let numInt = +num

console.log(numInt) // 20
```

### String to Float

We can convert string float number to a float number. 

- Any float number inside a quote is a string float number.
- We can convert string float to number using :
- parseFloat():

```
let num = '9.81'
let numFloat = parseFloat(num)

console.log(numFloat) // 9.81
```

- Number():

```
let num = '20.82.'
let numFloat = Number(num)

console.log(numFloat) // 20.82
```

- Plus sign(+):

```
let num = '20.82'
let numFloat = +num

console.log(numFloat) // 20.82
```

### Float to Int

We can convert float numbers to integers. We use the following method to convert float to int:

- parseInt():

```
let num = 20.82
let numInt = parseInt(num)

console.log(numInt) // 20
```

### **Boolean**

A boolean data type represents one of the two values:*true* or *false.*

The use of these data types is for comparison operator. Any comparisons return a boolean value which is either true or false.

Example:

```
let truValue = 4 > 3    // true
let falseValue = 4 < 3  // false
```

truth value and false value  used to to make decisions.

### Truthy values

- All numbers(positive and negative) are truthy except zero
- All strings are truthy except an empty string ('')
- The boolean true

### Falsy values

- 0
- 0n
- null
- undefined
- NaN
- the boolean false
- '', "", ``, empty string.

### **variables**

Variables are used to *store* data in a memory location.

When a variable is declared, a memory location is reserved. When a variable is assigned to a value (data), the memory space will be filled with that data. To declare a variable, we use *var*, *let*, or *const* keywords.

A valid JavaScript variable name must follow the following rules:

- A JavaScript variable name should not begin with a number.
- A JavaScript variable name does not allow special characters except dollar sign and underscore.
- A JavaScript variable name follows a camelCase convention(making the first letter of each word capitalized and not using spaces.).
- A JavaScript variable name should not have space between words.

### **Operators**

There  are different types of javascript operator:

- **Assignment Operators** : used to assign values to variables.

                 let firstName = 'Etsehiywot'

- **Arithmetic Operators:** used to perform arithmetic calculations.

                 Addition(+): a + b

                 Subtraction(-): a - b

                 Multiplication(*): a * b

                 Division(/): a / b

                  Modulus(%): a % b

                  Exponential(**): a ** b

- **Comparison Operators:**

used to compare two values and return a boolean value,either true or false.

| Operator | Description | Example |
| --- | --- | --- |
| == | Equal to: true if the operands are equal | 5==5; //true |
| != | Not equal to: true if the operands are not equal | 5!=5; //false |
| === | Strict equal to: true if the operands are equal and of the same type | 5==='5'; //false |
| !== | Strict not equal to: true if the operands are equal but of different type or not equal at all | 5!=='5'; //true |
| > | Greater than: true if the left operand is greater than the right operand | 3>2; //true |
| >= | Greater than or equal to: true if the left operand is greater than or equal to the right operand | 3>=3; //true |
| < | Less than: true if the left operand is less than the right operand | 3<2; //false |
| <= | Less than or equal to: true if the left operand is less than or equal to the right operand | 2<=2; //true |
- **Logical Operators**:

     used to perform logical operations and return a boolean value and also used in decision making         and loops.

- Examples:

       `const check = 4 > 3 && 10 > 5         // true && true -> true`

       `const check = 4 > 3 || 10 < 5         // true  || false -> true`

       `let check = 4 > 3                                    // true`

       `let check = !(4 > 3)                              //  false`

- **Bitwise Operators:** perform operations on binary representations of numbers.

### Incremental  Operator

In JavaScript we use the increment operator to increase a value stored in a variable. 

The increment operator is used as follows:

- var1++ ( Post-increment )
- ++var1 ( Pre-increment )

In the first case (i.e. post-increment) the operator increases the variable var1 by 1 but returns the value before incrementing.

In the second case (i.e. pre-increment) the operator increases the variable var1 by 1 but returns the value after incrementing.

example for pre increment:

```
let count = 0
console.log(++count)        // 1
console.log(count)          // 1
```

example for post increment:

```
let count = 0
console.log(count++)        // 0
console.log(count)          // 1
```

### Decrement Operator

The decrement operator is used as follows:

- var1-- ( Post-decrement )
- -var1 ( Pre-decrement )

In the first case (i.e. post-decrement) the operator decreases the variable var1 by 1 but returns the value before decrementing.

In the second case (i.e. pre-decrement) the operator decreases the variable var1 by 1 but returns the value after decrementing.

example for Pre-decrement:

```
let count = 0
console.log(--count) // -1
console.log(count)  // -1
```

example for Post-decrement:

```
let count = 0
console.log(count--) // 0
console.log(count)   // -1
```

### Ternary Operators

Ternary operator allows to write a condition. Another way to write conditionals is using ternary operators.

It is the only JavaScript operator that takes three operands:

- A condition followed by a question mark (?),
- Then an expression to execute if the condition is truthy followed by a colon (:), and
- Finally the expression to execute if the condition is false. This operator is frequently used as an alternative to an if...else statement.
- Example:

```
let number = 5
number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
number = -5

number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`)
```

**output:**

5 is a positive number
-5 is a negative number

### Operator precedence

**Operator precedence** determines how operators are parsed concerning each other. Operators with higher precedence become the operands of operators with lower precedence.

If  A and B have different precedence levels , the operator with the higher *precedence* goes first and associativity does not matter.

Example:

`console.log(3 + 4 * 5); // 3 + 20
// Expected output: 23`

`console.log(4 * 3 ** 2); // 4 * 9
// Expected output: 36`

`let a;
let b;`

`console.log(a = b = 5);
// Expected output: 5`

Output:

> 23
36
5
> 

### **Window Methods**

**Window alert() method**

 Alert() method displays an alert box with a specified message and an OK button. It is a builtin method and it takes on argument.

`alert(message)`

**Window prompt() method**

prompt methods display a prompt box with an input on your browser to take input values and the input data can be stored in a variable. The prompt() method takes two arguments. The second argument is optional.

`prompt('required text', 'optional text')`

**Window confirm() method**

The confirm() method displays a dialog box with a specified message, along with an OK and a Cancel button. A confirm box is often used to ask permission from a user to execute something. Window confirm() takes a string as an argument. Clicking the OK yields true value, whereas clicking the Cancel button yields false value.

```
const agree = confirm('Are you sure you like to delete? ')
console.log(agree) // result will be true or false based on what you click on the dialog box
```

### **Date Object**

In JavaScript current time and date is created using JavaScript Date Object. The object we create using Date object provides many methods to work with date and time.The methods we use to get date and time information from a date object values are started with a word *get* because it provide the information. values are:

- ***getFullYear()**: get the year as a four digit number(yyyy).*

```
const now = new Date()
console.log(now.getFullYear()) // 2023
```

- ***getMonth():** get the month as a number (0-11).*

```
const now = new Date()
console.log(now.getMonth()) // 6, because the month is January,  month(0-11)
```

 ***getDate():**get the day as a number (1-31).*

```
const now = new Date()
console.log(now.getDate()) // 4, because the day of the month is 4th,  day(1-31)
```

 ***getDay():**get a weekend as a date (0-6).*

```
const now = new Date()
console.log(now.getDay()) // 6, because the day is Saturday which is the 7th day
//  Sunday is 0, Monday is 1 and Saturday is 6
// Getting the weekday as a number (0-6)
```

***getHours():** get the hour(0-23).*

```
const now = new Date()
console.log(now.getHours()) // 0, because the time is 00:56:41
```

***Getting minutes:***

```
const now = new Date()
console.log(now.getMinutes()) // 56, because the time is 00:56:41
```

***Getting seconds:***

```
const now = new Date()
console.log(now.getSeconds()) // 41, because the time is 00:56:41
```

**Getting time:**

This method give time in milliseconds starting from January 1, 1970. It is also know as Unix time. We can get the unix time in two ways:

1. Using *getTime()*

```
const now = new Date() //
console.log(now.getTime()) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41
```

1. Using *Date.now()*

```
const allSeconds = Date.now() //
console.log(allSeconds) // 1578092201341, this is the number of seconds passed from January 1, 1970 to January 4, 2020 00:56:41

const timeInSeconds = new Date().getTime()
console.log(allSeconds == timeInSeconds) // true
```

when we format to a human readable time format. **Example:**

`const now = new Date()
const year = now.getFullYear() // return year
const month = now.getMonth() + 1 // return month(0 - 11)
const date = now.getDate() // return date (1 - 31)
const hours = now.getHours() // return number (0 - 23)
const minutes = now.getMinutes() // return number (0 -59)

console.log(`${date}/${month}/${year} ${hours}:${minutes}`) // 4/1/2020 0:56`

### Conditionals

Conditional statements are used for make decisions based on different conditions. 

Conditional statements are implemented when we need to perform different actions based on different conditions By default , statements in JavaScript script executed sequentially from top to bottom. If the processing logic require so, the sequential flow of execution can be altered in two ways:

- Conditional execution: a block of one or more statements will be executed if a certain expression is true
- Repetitive execution: a block of one or more statements will be repetitively executed as long as a certain expression is true. In this section, we will cover *if*, *else* , *else if* statements. The comparison and logical operators we learned in the previous sections will be useful in here.

at all In JavaScript, the conditional statements that we have are:

- if,
- else if,
- else,
- switch statements and
- ternary operator.

### **IF**

The key word *if* is to used check if a condition is true and to execute the block code. To create an if condition:

```
// syntax
if (condition) {
  //this part of code runs for truthy condition
}
```

**Example:**

`let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
}
//  3 is a positive number`

### **If Else**

If condition is true the first block will be executed, if not the else condition will be executed.

```
// syntax
if (condition) {
  // this part of code runs for truthy condition
} else {
  // this part of code runs for false condition
}
```

**Example:**

`let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  3 is a positive number

num = -3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  -3 is a negative number`

**If Else if Else**

Use the `else if` statement to specify a new condition if the first condition is false.

```
// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code

}
```

**Example:**

`let a = 0
if (a > 0) {
  console.log(`${a} is a positive number`)
} else if (a < 0) {
  console.log(`${a} is a negative number`)
} else if (a == 0) {
  console.log(`${a} is zero`)
} else {
  console.log(`${a} is not a number`)
}`

### Switch

Switch is an alternative for **if else if else else**. The switch statement starts with a *switch* keyword followed by a parenthesis and code block. Inside the code block we will have different cases. Case block runs if the value in the switch statement parenthesis matches with the case value.

```
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

to use conditions in the cases

`let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}`

### Ternary Operators

Another way to write conditionals is using ternary operators. 

**Example:**

`let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')`

### **Arrays**

- An array is a collection of different data types which are ordered and changeable(modifiable).
- An array allows storing duplicate elements and different data types.
- In contrast to variables, an array can store *multiple values*. Each value in an array has an *index*, and each index has *a reference in a memory address.*
- An array can be empty, or it may have different data type values.

### **How to create an empty array?**

It is very common to use *const* instead of *let* to declare an array variable. If you ar using const it means you do not use that variable name again.

In JavaScript, we can create an array in different ways:

- **Using Array constructor**

`// syntax
const arr = Array()
// or
// let arr = new Array()
console.log(arr) // []`

- **Using square brackets([])**

`// syntax
// This the most recommended way to create an empty list
const arr = []
console.log(arr)`

### How to create an array with values?

Array with initial values. We use *length* property to find the length of an array.

```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] // array of numbers
const fruits = ['banana', 'orange', 'mango', 'lemon'] // array of strings, fruits
const vegetables = ['Tomato', 'Potato', 'Cabbage', 'Onion', 'Carrot'] // array of strings, vegetables
const animalProducts = ['milk', 'meat', 'butter', 'yoghurt'] // array of strings, products
const webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] // array of web technologies
const countries = ['Finland', 'Denmark', 'Sweden', 'Norway', 'Iceland'] // array of strings, countries

// Print the array and its length

console.log('Numbers:', numbers)
console.log('Number of numbers:', numbers.length)

console.log('Fruits:', fruits)
console.log('Number of fruits:', fruits.length)

console.log('Vegetables:', vegetables)
console.log('Number of vegetables:', vegetables.length)

console.log('Animal products:', animalProducts)
console.log('Number of animal products:', animalProducts.length)

console.log('Web technologies:', webTechs)
console.log('Number of web technologies:', webTechs.length)

console.log('Countries:', countries)
console.log('Number of countries:', countries.length)
```

- Array can have items of different data types

`const arr = [
    'Etsehiywot',
    21,
    true,
    { country: 'Ethiopia', city: 'Addis abeba' },
    { skills: ['HTML', 'CSS', 'JS', 'React', 'Python'] }
] // arr containing different data types
console.log(arr)`

### Creating an array using split

we can split a string at different positions, and we can change to an array.

```
let js = 'JavaScript'
const charsInJavaScript = js.split('')

console.log(charsInJavaScript) // ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]

let companiesString = 'Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon'
const companies = companiesString.split(',')

console.log(companies) // ["Facebook", " Google", " Microsoft", " Apple", " IBM", " Oracle", " Amazon"]
```

### Accessing array items using index

We access each element in an array using their index.

Example:

`const fruits = ['banana', 'orange', 'mango', 'lemon']`

```
secondFruit = fruits[1]
console.log(secondFruit) // orange
```

Example:

```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]  // set of numbers

console.log(numbers.length)  // => to know the size of the array, which is 6
console.log(numbers)         // -> [0, 3.14, 9.81, 37, 98.6, 100]
console.log(numbers[0])      //  -> 0
console.log(numbers[5])      //  -> 100

let lastIndex = numbers.length - 1;
console.log(numbers[lastIndex]) // -> 100
```

### Modifying array element

An array is mutable(modifiable). Once an array is created, we can modify the contents of the array elements.

```
const numbers = [1, 2, 3, 4, 5]
numbers[0] = 10      // changing 1 at index 0 to 10
numbers[1] = 20      // changing  2 at index 1 to 20

console.log(numbers) // [10, 20, 3, 4, 5]
```

### Methods to manipulate array

There are different methods to manipulate an array these are:*Array, length, concat, indexOf, slice, splice, join, toString, includes, lastIndexOf, isArray, fill, push, pop, shift, unshift*

### **Array Constructor**

```
const arr = Array() // creates an an empty array
console.log(arr)

const eightEmptyValues = Array(8) // it creates eight empty values
console.log(eightEmptyValues) // [empty x 8]
```

### **Creating static values with fill**

fill: Fill all the array elements with a static value.

```
const arr = Array() // creates an an empty array
console.log(arr)

const eightXvalues = Array(8).fill('X') // it creates eight element values filled with 'X'
console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']

const eight0values = Array(8).fill(0) // it creates eight element values filled with '0'
console.log(eight0values) // [0, 0, 0, 0, 0, 0, 0, 0]

const four4values = Array(4).fill(4) // it creates 4 element values filled with '4'
console.log(four4values) // [4, 4, 4, 4]
```

### **Concatenating array using concat**

concat:To concatenate two arrays.

```
const firstList = [1, 2, 3]
const secondList = [4, 5, 6]
const thirdList = firstList.concat(secondList)

console.log(thirdList) // [1, 2, 3, 4, 5, 6]
```

### **Getting array length**

Length:To know the size of the array

`const numbers = [1, 2, 3, 4, 5]
console.log(numbers.length) // -> 5 is the size of the array`

### **Getting index an element in arr array**

indexOf:To check if an item exist in an array. If it exists it returns the index else it returns -1.

`const numbers = [1, 2, 3, 4, 5]

console.log(numbers.indexOf(5)) // -> 4
console.log(numbers.indexOf(0)) // -> -1
console.log(numbers.indexOf(1)) // -> 0
console.log(numbers.indexOf(6)) // -> -1`

### **Getting last index of an element in array**

lastIndexOf: It gives the position of the last item in the array. If it exist, it returns the index else it returns -1.

`const numbers = [1, 2, 3, 4, 5, 3, 1, 2]

console.log(numbers.lastIndexOf(2)) // 7
console.log(numbers.lastIndexOf(0)) // -1
console.log(numbers.lastIndexOf(1)) //  6
console.log(numbers.lastIndexOf(4)) //  3
console.log(numbers.lastIndexOf(6)) // -1`

- check if an item exist in an array. If it exist it returns the true else it returns false.

`const numbers = [1, 2, 3, 4, 5]

console.log(numbers.includes(5)) // true
console.log(numbers.includes(0)) // false
console.log(numbers.includes(1)) // true
console.log(numbers.includes(6)) // false`

### **Checking array**

Array.isArray:To check if the data type is an array

```
const numbers = [1, 2, 3, 4, 5]
console.log(Array.isArray(numbers)) // true

const number = 100
console.log(Array.isArray(number)) // false
```

### **Converting array to string**

toString:Converts array to string

```
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.toString()) // 1,2,3,4,5

const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']
console.log(names.toString()) // Asabeneh,Mathias,Elias,Brook
```

### **Joining array elements**

join: It is used to join the elements of the array, the argument we passed in the join method will be joined in the array and return as a string. By default, it joins with a comma, but we can pass different string parameter which can be joined between the items.

`const numbers = [1, 2, 3, 4, 5]
console.log(numbers.join()) // 1,2,3,4,5`

### **Slice array elements**

Slice: To cut out a multiple items in range. It takes two parameters:starting and ending position. It doesn't include the ending position.

```
  const numbers = [1,2,3,4,5]

  console.log(numbers.slice()) // -> it copies all  item
  console.log(numbers.slice(0)) // -> it copies all  item
  console.log(numbers.slice(0, numbers.length)) // it copies all  item
  console.log(numbers.slice(1,4)) // -> [2,3,4] // it doesn't include the ending position
```

### Splice method in array

Splice: It takes three parameters:Starting position, number of times to be removed and number of items to be added.

  `const numbers = [1, 2, 3, 4, 5]
  numbers.splice()
  console.log(numbers)                // -> remove all items`

### Adding item to an array using push

Push: adding item in the end. To add item to the end of an existing array we use the push method.

```
const numbers = [1, 2, 3, 4, 5]
numbers.push(6)
console.log(numbers) // -> [1,2,3,4,5,6]

numbers.pop() // -> remove one item from the end
console.log(numbers) // -> [1,2,3,4,5]
```

### Removing the end element using pop

pop: Removing item in the end.

```
const numbers = [1, 2, 3, 4, 5]
numbers.pop() // -> remove one item from the end
console.log(numbers) // -> [1,2,3,4]
```

### Removing an element from the beginning

shift: Removing one array element in the beginning of the array.

```
const numbers = [1, 2, 3, 4, 5]
numbers.shift() // -> remove one item from the beginning
console.log(numbers) // -> [2,3,4,5]
```

### Add an element from the beginning

unshift: Adding array element in the beginning of the array.

```
const numbers = [1, 2, 3, 4, 5]
numbers.unshift(0) // -> add one item from the beginning
console.log(numbers) // -> [0,1,2,3,4,5]
```

### Reversing array order

reverse: reverse the order of an array.

`const numbers = [1, 2, 3, 4, 5]
numbers.reverse() // -> reverse array order
console.log(numbers) // [5, 4, 3, 2, 1]

numbers.reverse()
console.log(numbers) // [1, 2, 3, 4, 5]`

### Sorting elements in array

sort: arrange array elements in ascending order. Sort takes a call back function, we will see how we use sort with a call back function in the coming sections.

```
const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB'
]

webTechs.sort()
console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]

webTechs.reverse() // after sorting we can reverse it
console.log(webTechs) // ["Redux", "React", "Node", "MongoDB", "JavaScript", "HTML", "CSS"]
```

### Array of arrays

Array can store different data types including an array itself. Let us create an array of arrays

`const firstNums = [1, 2, 3]
const secondNums = [1, 4, 9]

const arrayOfArray =  [[1, 2, 3], [1, 2, 3]]
console.log(arrayOfArray[0]) // [1, 2, 3]

 const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
 const backEnd = ['Node','Express', 'MongoDB']
 const fullStack = [frontEnd, backEnd]
 console.log(fullStack)   // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]
 console.log(fullStack.length)  // 2
 console.log(fullStack[0])  // ["HTML", "CSS", "JS", "React", "Redux"]
 console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]`

### **Loops**

loops are used to carry out repetitive task.

It is used **to execute a group of instructions or a block of code multiple times, without writing it repeatedly**. The block of code is executed based on a certain condition.

- There are different kinds of loops:

### **for Loop:-**

```
// For loop structure
for(initialization, condition, increment/decrement){
  // code goes here
}
```

Example:

`for(let i = 0; i <= 5; i++){
  console.log(i)
}

// 0 1 2 3 4 5`

Example:

```
or(let i = 0; i <= 5; i++){
  console.log(`${i} * ${i} = ${i * i}`)
}
```

`0 * 0 = 0
1 * 1 = 1
2 * 2 = 4
3 * 3 = 9
4 * 4 = 16
5 * 5 = 25`

Adding all elements in the array

```
const numbers = [1, 2, 3, 4, 5]
let sum = 0
for(let i = 0; i < numbers.length; i++){
  sum  = sum + numbers[i]  // can be shorten, sum += numbers[i]

}

console.log(sum)  // 15
```

Creating a new array based on the existing array

`const numbers = [1, 2, 3, 4, 5]
const newArr = []
let sum = 0
for(let i = 0; i < numbers.length; i++){
  newArr.push( numbers[i] ** 2)

}

console.log(newArr)  // [1, 4, 9, 16, 25]`

### **while loop**

The while loop is similar to the for loop because it also runs *while* a condition is true. The difference between them is that we would use a for loop when we already know how many times we want the loop to be executed. A while loop is used when we are unsure about how many times the loop wants to run.

```
let i = 0
while (i <= 5) {
  console.log(i)
  i++
}

// 0 1 2 3 4 5
```

### **do while loop**

Do While loop executes the condition after the fact.

`let i = 0
do {
  console.log(i)
  i++
} while (i <= 5)

// 0 1 2 3 4 5`

### for of loop

We use for of loop for arrays. It is very hand way to iterate through an array if we are not interested in the index of each element in the array.

```
for (const element of arr) {
  // code goes here
}
```

```
const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
const newArr = []
for(const country of countries){
  newArr.push(country.toUpperCase())
}

console.log(newArr)  // ["FINLAND", "SWEDEN", "NORWAY", "DENMARK", "ICELAND"]
```

### break

Break is used to interrupt a loop.

`for(let i = 0; i <= 5; i++){
  if(i == 3){
    break
  }
  console.log(i)
}

// 0 1 2`

### continue

We use the keyword *continue* to skip a certain iterations.

`for(let i = 0; i <= 5; i++){
  if(i == 3){
    continue
  }
  console.log(i)
}

// 0 1 2 4 5`

### Function

Functions are blocks of code that can be called by other code, by itself, or by a variable that refers to that function object. Usually when you call a function, it takes in one or multiple arguments and it can optionally return a value.

A function is a reusable block of code or programming statements designed to perform a certain task.

It is declared by a function key word followed by :

a name, followed by parentheses (). A parentheses can take a parameter. If a function take a parameter it will be called with argument. A function can also take a default parameter. To store a data to a function, a function has to return certain data types. To get the value we call or invoke a function. 

A function can be declared or created in couple of ways:

- *Declaration function*
- *Expression function*
- *Anonymous function*
- *Arrow function*

### **Function Declaration**

```
//declaring a function without a parameter
function functionName() {
  // code goes here
}
functionName() // calling function by its name and with parentheses
```

### Function without a parameter and return

Function can be declared without a parameter.

**Example:**

`// function without parameter,  a function which make a number square
function square() {
  let num = 2
  let sq = num * num
  console.log(sq)
}

square() // 4

// function without parameter
function addTwoNumbers() {
  let numOne = 10
  let numTwo = 20
  let sum = numOne + numTwo

  console.log(sum)
}

addTwoNumbers() // a function has to be called by its name to be executed`

### **Function returning value**

```
function addTwoNumbers() {
      let numOne = 2
      let numTwo = 3
      let total = numOne + numTwo
      return total

  }

console.log(addTwoNumbers())
```

### Function with a parameter

In a function we can pass different data types(number, string, boolean, object, function) as a parameter.

```
// function with one parameter
function functionName(parm1) {
  //code goes her
}
functionName(parm1) // during calling or invoking one argument needed

function areaOfCircle(r) {
  let area = Math.PI * r * r
  return area
}

console.log(areaOfCircle(10)) // should be called with one argument

function square(number) {
  return number * number
}

console.log(square(10))
```

### Function with two parameters

```
// function with two parameters
function functionName(parm1, parm2) {
  //code goes her
}
functionName(parm1, parm2) // during calling or invoking two arguments needed
// Function without parameter doesn't take input, so lets make a function with parameters
function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo
  console.log(sum)
}
sumTwoNumbers(10, 20) // calling functions
// If a function doesn't return it doesn't store data, so it should return

function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo
  return sum
}

console.log(sumTwoNumbers(10, 20))
function printFullName(firstName, lastName) {
  return `${firstName} ${lastName}`
}
console.log(printFullName('Etaehiywot', 'Dereje'))
```

### Function with many parameters

`// function with multiple parameters
function functionName(parm1, parm2, parm3,...){
  //code goes here
}
functionName(parm1,parm2,parm3,...) // during calling or invoking three arguments needed

// this function takes array as a parameter and sum up the numbers in the array
function sumArrayValues(arr) {
  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum = sum + arr[i];
  }
  return sum;
}
const numbers = [1, 2, 3, 4, 5];
    //calling a function
console.log(sumArrayValues(numbers));

    const areaOfCircle = (radius) => {
      let area = Math.PI * radius * radius;
      return area;
    }
console.log(areaOfCircle(10))`

### **Function with unlimited number of parameters**

Sometimes we do not know how many arguments the user going to pass. 

Passing arguments to a function can be tricky, especially when we are not certain about the number of those arguments.

Therefore, we should know how to write a function which can take unlimited number of arguments. The way we do it has a significant difference between a function declaration(regular function) and arrow function

### Unlimited number of parameters in regular function

A function declaration provides a function scoped arguments array like object. Any thing we passed as argument in the function can be accessed from arguments object inside the functions. Let us see an example

```
// Let us access the arguments object

function sumAllNums() {
 console.log(arguments)
}

sumAllNums(1, 2, 3, 4)
// Arguments(4) [1, 2, 3, 4, callee: ƒ, Symbol(Symbol.iterator): ƒ]
```

```
// function declaration

function sumAllNums() {
  let sum = 0
  for (let i = 0; i < arguments.length; i++) {
    sum += arguments[i]
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173
```

### Unlimited number of parameters in arrow function

Arrow function does not have the function scoped arguments object. To implement a function which takes unlimited number of arguments in an arrow function we use spread operator followed by any parameter name. Any thing we passed as argument in the function can be accessed as array in the arrow function.

**Example:**

```
// Let us access the arguments object

const sumAllNums = (...args) => {
 // console.log(arguments), arguments object not found in arrow function
 // instead we use a parameter followed by spread operator (...)
 console.log(args)
}

sumAllNums(1, 2, 3, 4)
// [1, 2, 3, 4]
```

`// function declaration

const sumAllNums = (...args) => {
  let sum = 0
  for (const element of args) {
    sum += element
  }
  return sum
}

console.log(sumAllNums(1, 2, 3, 4)) // 10
console.log(sumAllNums(10, 20, 13, 40, 10))  // 93
console.log(sumAllNums(15, 20, 30, 25, 10, 33, 40))  // 173`0

### Anonymous Function

Anonymous function or without name

```
const anonymousFun = function() {
  console.log(
    'I am an anonymous function and my value is stored in anonymousFun'
  )
}
```

### Expression Function

Expression functions are anonymous functions. After we create a function without a name and we assign it to a variable. To return a value from the function we should call the variable.

Example:

```
// Function expression
const square = function(n) {
  return n * n
}

console.log(square(2)) // -> 4
```

### Self Invoking Functions

Self invoking functions are anonymous functions which do not need to be called to return a value.

```
(function(n) {
  console.log(n * n)
})(2) // 4, but instead of just printing if we want to return and store the data, we do as shown below

let squaredNum = (function(n) {
  return n * n
})(10)

console.log(squaredNum)
```

### Arrow Function

Arrow function is an alternative to write a function, however function declaration and arrow function have some  differences.

Arrow function uses arrow instead of the keyword *function* to declare a function. Example for  both function declaration and arrow function.

`// This is how we write normal or declaration function
// Let us change this declaration function to an arrow function
function square(n) {
  return n * n
}

console.log(square(2)) // 4

const square = n => {
  return n * n
}

console.log(square(2))  // -> 4

// if we have only one line in the code block, it can be written as follows, explicit return
const square = n => n * n  // -> 4`

### Function with default parameters

Sometimes we pass default values to parameters, when we invoke the function if we do not pass an argument the default value will be used.

 Both function declaration and arrow function can have a default value or values.

Example for function decleration:

```
function generateFullName(firstName = 'Asabeneh', lastName = 'Yetayeh') {
  let space = ' '
  let fullName = firstName + space + lastName
  return fullName
}

console.log(generateFullName())
console.log(generateFullName('Etsehiywot', 'Dereje'))
```

**Example for arrow function:**

`const greetings = (name = 'Peter') => {
  let message = name + ', welcome to 30 Days Of JavaScript!'
  return message
}

console.log(greetings())
console.log(greetings('Asabeneh'))`

### **Function declaration versus Arrow function**

**Regular functions created using function declarations or expressions are constructible and callable**. Since regular functions are constructible, they can be called using the new keyword. However, the arrow functions are only callable and not constructible, i.e arrow functions can never be used as constructor functions.

### Scope

It  determines the accessibility (visibility) of variables,Variable is the fundamental part in programming.

To declare a variable we use the key word *var*, *let* and *const*. A variable can be declared at different scope.

Variables scopes can be:

- Global
- Local
- 

**Global scope**

The global scope in JavaScript refers to the context in which variables and functions are defined outside of any function or block MEANS can be accessed every where in the same file. Variables and functions defined in the global scope are accessible from anywhere in the code.

Here is an example of a variable defined in the global scope in JavaScript:

```
let message = "Hello, world!";

function greet() {
    console.log(message);
}

greet(); // logs "Hello, world!"

```

### Local scope

A variable declared as local can be accessed only in certain block code.

- Block Scope
- Function Scope

```
//scope.js
let a = 'JavaScript' // is a global scope it will be found anywhere in this file
let b = 10 // is a global scope it will be found anywhere in this file
// Function scope
function letsLearnScope() {
  console.log(a, b) // JavaScript 10, accessible
  let value = false
// block scope
  if (true) {
    // we can access from the function and outside the function but
    // variables declared inside the if will not be accessed outside the if block
    let a = 'Python'
    let b = 20
    let c = 30
    let d = 40
    value = !value
    console.log(a, b, c, value) // Python 20 30 true
  }
  // we can not access c because c's scope is only the if block
  console.log(a, b, value) // JavaScript 10 true
}
letsLearnScope()
console.log(a, b) // JavaScript 10, accessible
```

### Window Global Object

Without using console.log() open your browser and check, you will see the value of a and b if you write a or b on the browser. That means a and b are already available in the window.

A global object is **an object that always exists in the global scope**. In JavaScript, there's always a global object defined. In a web browser, when scripts create global variables defined with the var keyword, they're created as members of the global object.

```
//scope.js
a = 'JavaScript' // declaring a variable without let or const make it available in window object and this found anywhere
b = 10 // this is a global scope variable and found in the window object
function letsLearnScope() {
  console.log(a, b)
  if (true) {
    console.log(a, b)
  }
}
console.log(a, b) // accessible
```

### Objects

In JavaScript, almost "everything" is an object.

- Booleans can be objects (if defined with the new keyword)
- Numbers can be objects (if defined with the new keyword)
- Strings can be objects (if defined with the new keyword)
- Dates are always objects
- Maths are always objects
- Regular expressions are always objects
- Arrays are always objects
- Functions are always objects
- Objects are always objects

All JavaScript values, except primitives, are objects.

**Creating an empty object**

To create an object literal, we use two curly brackets.

An empty object

`const person = {}`

### Creating an objecting with values

Now, the person object has firstName, lastName, age, location, skills and isMarried properties. The value of properties or keys could be a string, number, boolean, an object, null, undefined or a function.

```
const rectangle = {
  length: 20,
  width: 20
}
console.log(rectangle) // {length: 20, width: 20}

const person = {
  firstName: 'Etsehiywot',
  lastName: 'Dereje',
  age: 21,
  country: 'Ethiopia',
  city: 'Addis Abeba',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js'
  ],
  isMarried: true
}
console.log(person)
```

### Getting values from an object

We can access values of object using two methods:

- using . followed by key name if the key-name is a one word
- using square bracket and a quote

Example:

`const object1 = {
a: 'somestring',
b: 42,
c: false
};`

`console.log(Object.values(object1));
// Expected output: Array ["somestring", 42, false]`

### Setting new key for an object

An object is a mutable data structure and we can modify the content of an object after it gets created.

Setting a new keys in an object

```
// program to add a key/value pair to an object

const person = {
    name: 'Etsehiywot',
    age: 21,
    gender: 'female'
}
```

### Object Methods

There are different methods to manipulate an object. Let us see some of the available methods.

*Object.assign*: To copy an object without modifying the original object.

```
const person = {
  firstName: 'Etsehiywot',
  age: 250,
  country: 'Ethiopia',
  city:'Addis abeba',
  skills: ['HTML', 'CSS', 'JS'],
  title: 'Student',
  address: {
    
    city: 'Addis abeba'
  },
  getPersonInfo: function() {
    return `I am ${this.firstName} and I live in ${this.city}, ${this.country}. I am ${this.age}.`
  }
}

//Object methods: Object.assign, Object.keys, Object.values, Object.entries
//hasOwnProperty

const copyPerson = Object.assign({}, person)
console.log(copyPerson)
```

### Getting object values using Object.values()

*Object.values*:To get values of an object as an array

```
const values = Object.values(copyPerson)
console.log(values)
```

### Getting object keys and values using Object.entries()

*Object.entries*:To get the keys and values in an array

```
const entries = Object.entries(copyPerson)
console.log(entries)
```

### Checking properties using hasOwnProperty()

*hasOwnProperty*: To check if a specific key or property exist in an object

`console.log(copyPerson.hasOwnProperty('name'))
console.log(copyPerson.hasOwnProperty('score'))`