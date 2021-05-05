using Scrimba.com to learn Javascript

VARIABLES
You have to declare variables the first time you use/create them with the let function

let firstName = "josh";

you end the line with a ;

you can also log into a console using console.log();



you can do console.log(typeof varabile-name-here) to find out the type of the particular variable

there are all of the standard variable types, numbers (no distinction between float and int), string, boolean, etc
you can comment but you use // instead of #
if you want to do a block comment you can do /* to start it and */ to end it 


you can use math functions directly on variables like below

age = age +1;

you can use + to concatonate multiple pieces of information together like variables and strings


CONSTANTS

you can store information in constants as well, these like symbols in ruby can't be changed.  This is a constant value and cannot be reassigned

STRINGS

you can use string interpolation by using `${}`
NOTE: these are back picks `` not quotes ''
for example:
console.log(`${firstName} ${lastName}`)

string properties:

.length = gives length
.trim() = removes all empty space at the start and end of the string
.split() = breaks a string based on the parameter that you enter in the () into an array so split.(' ') would break the string on each space and listed in an array

NUMBERS

you can use the partseInt() or parseFloat function to get just an int value. 
NOTE: THIS TURNS THEM INTO A STRING IN THE OUTPUT
so console.log(parseInt(example_variable);
console.log(parseFloat(example); 

you can set something to a specific number of decimals using .toFixed()
you put the number of decimals as the argument

so console.log(example.toFixed(1)) gives us 1.1

parseInt and parseFloat only work on strings if the string starts with a number

BOOLEAN

null is a falsey value
undefined is a falsey value
an empty string is a falsey value
a non-empty string is a truthy value
Nan is a falsey value
0 value is falsey

ARRAY

arrays are defined with [1, 2, 3] just like in ruby
you can call specific item in an array by using console.log(example[1]) which will pull the 2nd item inthe array

.push() = add new values to the end of an array
.pop() = pop off the last item in an array

you want to store strings in an array using ""

you can reassign a value by doing example[0] = "new item";

OBJECTS

these are defined by curley brackets {}

let example1 = {
firstName: 'Dylan',
lastName: 'Israel',
address: {
  city: 'Austin',
  state: 'Texas'
},
};

then you can call this object at various points by using the key

console.log(example1.firstName);
Dylan

console.log(example1.address.city);

Austin

you can update object values just like variables

example1.firstName = "Josh"

you can print keys using a .keys function
console.log(Object.values(example1))
console.log(object,keys(example1))

you can check for a key using hasOwnProperty

console.log(object.hasOwnProperty(example1))

ARITHMATIC

+ - * / %

RELATIONAL OPERATORS

== = compares the values only (so a number 10 and string '10' would be the same)
===  = compares value and type
<=
>=
!==

INCREMENTALS

you can use ++ and -- to add or minus itself from the number

1 ++ = 2
1 -- = 0

you can also use += and -= for a specific amount

1 += 5;
= 6
