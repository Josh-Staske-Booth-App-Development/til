---
layout: post
title: Josh Basics Review Day
---

Going to review the basics and keep notes to myself here today.


key string methods

.upcase #goes all uppercase
.downcase #goes all lower case
.gsub("Thing you want to replace", "what you want to replace it with") #to replace things, use in combination with / / regularal expressions i.e. regex for advanced string filtering
.length
.reverse
.swapcase
.chomp #removes the /n new line character at the end
.strip #removes any whitespace at the end
.capitalize gives you back a string with just the first character capitalized

.to_s #changes to a string
.to_i #changes to an integer
.to_f #changes to a float

.split #splits a string into an array THIS IS AN IMPORTANT TOOL

.include?()

get a string from a user input by using gets, strip out whitespace on the end with gets.chomp

interprolate a string with #{} inside the string to call variable or do math for example "One plus three is equal to #{1 + 3}"


#INTEGERS

+ - * / % are all mathmatical operators on integers
and int is and int not a float. They have a decimal at the end i.e. 2.2 instead of the integer 2

.odd?
.even?

rand(n) #calls a random number between 0 and n - 1

#FLOATS

.round 

#Date

Ruby has a built in class for dates so you don't have to use any kind of string to store it!

date.parse() lets you put dates in a written format and it should be able to figure out what you mean i.e. "October 3rd 2021"

#Time

There is also a class of Time

Time.now

#IF STATEMENTS AND CONDITIONALS

if (insert arguments here)

else

do this thing

end

you can use else and you can use elsif to add more layers

so

if if blank is blank
do this

elsif blank is blank2
do this

elsif blank is blank3
do this

else
if none of those are truthy then do this

end

DON'T FOR THE "END" AT THE END

for comparisons

< less than
> greater than
== equal to
!= not equal to
<= less than or equal to
>= greater than or equal to

and and or

&& for and arguments (gotta satisfy both criteria)
|| for or arguments (gotta only satisfy one or more )

#ARRAY

creating an array is as simple as names = Array.new

push new values into the array with names.push("Josh")
names.push("Megan")
names.<<("Steve")
<< is the same as push

#you can also create arrays like this 

names = ["Josh", "Megan", "Steve"]
[] are arrays
{} are hash tables with keys

ARRAY METHODS
.at is a method for arrays since they are numbered you can retrieve values with names.at(0)
instead of .at you can also use shorthand .[] so names.[](2) and it will give you the 3rd value

.first and .last give you the values you would expect so names.first and names.last

.index gives it the number that value resides at within the array so names.index("Josh") = 0

as a reminder string.split will turn it into an array based on spaces or based on the value you highlight

"This is a string example".split = ["This", "is", "a", "string", "example"]

"so,is,this".split(",") = ["so", "is", "this"] it will split based on the "," value because that is what was highlighted

"Josh".split("") is splitting on nothing so it will give you ["J", "o", "s", "h"]

.count will give you a total number of items in that array or you can call it on a specific item like list_of_names.count("Josh") and it will see how many times "Josh" is listed

.include? does it include whatever value you give
.exclude? same deal but exclusion
.reverse
.sort
.shuffle
.sample
.min
.max
.sum


#LOOPS

no, not fruit loops, data operations loops.

If is a conditional that does a singluar action

using a while: loop you can continue an action or ste of actions until some criteria is met

while XYZ criteria

do XYZ actions

end

so what you can do with that is use a counter method. Create a variable, assign it a numarical value typically 1 or 0 and then have it count up a certain number of times
as it loops through whatever set of actions you want to take

counter = 0

while counter < 10
  print "Josh, the counter is at  #{counter}"
  
  counter = counter + 1
 end
 
 this is going to loop through and add a counter +1 each time, then when the counter variable has surpassed 10 it will stop
 
 alternatively you could use 
 
 the .times method so and the action do
 
 counter = 1
 
 10.times do
  p mississippi.to_s + " Mississippi"
  
  counter = counter + 1
 
 other methods
 
 1.upto(5)
 11.downto(3)
 10.step(1, -6)

#BLOCK VARIABLES

this is another way of looping

first you have to have an array

array = []

array.push(1, 2, 3)

array.each d |n|

n = n + 10
end

another alternative is to use "for"

for fruit in fruits
  p "The name of this fruit is #{fruit}"
end

#HASH

very similar to an array but it is not indexed by a nubmer but instead has a key value paring

another difference is that we have P{} instead of [].  Respect the curley brackets.

we can use .store to add key value pairs to a hash for example

fruits = { :banana => yellow, :apple => red, :orange => orange}
fruits.store{ :pear => yellowish}

.fetch is the equivalent of .at for an array.  
you can use shorthand [] just like with arrays
so you could use either
fruits.fetch(:banana)

or you could do fruits[:banana]

.keys can be used on a hash table to get a list of keys

fruits.keys will give you [:banana, :apple, :orange, :pear]

#Symbols

symbols are like strings

"String"
:symbol

:symbols are used when developers need to label something.  They don't have a ton of methods like .reverse or .capitalize

#CLASS

you define classes with capital letters such a Fruits

if you have a multi word class you have to do CamelCase so VeryImportantPerson

with classes you can give them attributes using attr_accessor

so for fruits we could do 

class Fruits
  attr_accessor :color
  attr_accessor :shape
  attr_accessor :flavor
end

you can then make a variable, define it's class, then assign the available attributes

banana = Fruits.new
banana.color = "yellow"
banana.shape = "bendy cylinder"
banana.flavor = "banana flavored"

now we can call what values we have on that particular variable using the .attribute method

p banana.color
prints out "yellow"
p banana.shape = "bendy cylinder"
prints "bendy cylinder"

p banana.class 
prints Fruits with a capital F and no quotes because it is a class not a string as the attributes are

#DEFINING INSTANCE METHODS

firstly, you define a method by using 

def INSERT_NAME_OF_METHOD
  return put the code here you want to have happen
end

so, now that we know how to do that you can do it within a class so that each class can have it's own methods

so we have something like this, notice the indentations and the double ending.  the first end is for the instance method, the second is for the class itself

class FancyPants
  attr_accessor :color
  attr_accessor :fancy_details
  
  def show_off_fancy_pants
    return "Look at my fancy pants! Can't you see the self.color + ' ' + self.fancy_details?"
   end
 end
 
 #DEFINING CLASS METHODS
 
 so class methods are a little different then instance methods
