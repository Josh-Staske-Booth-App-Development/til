CONDITIONALS
You should tab out the command after the conditional

if (example === 6 && true == true)
  {then we should do something about that 6 year old causing problems};
 
use if to set up a conditional

else if, the next level of conditional

else

&& for and

if(1 ==1 && true == true)

or = ||

if (josh === "tired" || time === "9:00 pm")
  {console.log(josh should go to sleep)};
  
  
SWITCH STATEMENTS

similar to conditionals but you pass in a value, check to see if it matches any of the specific cases, YOU HAVE TO HIS BREAK TO MOVE TO THE NEXT 'CASE'
you can set a default value with default: which is the same as an "else" ending conditional.  no need to break on the default

let studentAnswer = 'A';

switch(studentAnswer) {
  case 'A':
    console.log('A is wrong');
    break;
  case 'B':
    console.log('B is wrong');
    break;
   case 'C':
     console.log('C is correct.');
     break;
   default:
    console.log('Not a real answer.);
    
    
 FOR LOOPS
 
 first create a variable, then tab and in {} put what you want to have happen
 
 let total = 0;
 
 for (let i = 0; i< 5; i++) {
  total += i;
 }
 
 console.log(total);
 
 let numArray = [1, 2, 3, 4, 5]
 for (let i = 0; i < numArray.length; i++) {
  total += numArray[i];
 }
 
 WHILE LOOPS
 
 you run these and it will go until the values is equal to true
 if the statement is initially false it will never ever run not even once
 
 let count = 0;
 while (count < 20) {
 
 DO WHILE
 exactly the same as a while loop but will run one time
 
 let count = 0;
 
 do {
    count++;
  
    if(count ==='Dylan') {
    break;
    }
 }
 
while(false)

FUNCTIONS
you create a function by using function and then put the name of the function with parenthasis

function add() {
  console.log('add');
}

you can call a function by using it directly

add();

you can also add in multiple parameters

function add(num1, num2) {
  return num1 + num2;

}

console.log(add(10, 6));

this would produce 16
