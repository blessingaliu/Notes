# Intro to Ruby

## What is Ruby

- backend programming language
- easy to read
- object-oriented programming

- classes vs instances

classes - blueprint for what each object is going to look like/behavior

instances - it is an object that you made using a specific class. An object is an instance of a class, the word 'instance' indicates the relationship of an object to its class.


## Methods

- behaviors 

- puts vs return vs print

- puts = print something out for our user to see / returns nil /
- print = provides output / return nil / 

- return - stores data to memory for possible later usage 

```ruby
def method_name 
   expr..
end
```

Whenever you call the simple method, you write only the method name as follows −
method_name

- Methods can have arguments/parameters 
    - wrapped in paranthesis
    - variables as placeholders

```ruby
def method_name (var1 = value1, var2 = value2)
   expr..
end
```

However, when you call a method with parameters, you write the method name along with the parameters, such as −
method_name 25, 30

    - optional arguments give you the ability to define a method to either accept and argument or omit an argument 
    


## Variables

- what are variables? an id for data values 

- a label on a box that stores some data

```ruby
name = "blessing"
```

## Data Types

- strings = wrapped around with quotes "aysan"
- integers = numbers 1 2 3 
- arrays = [1, 2, 3, "Loren", true, :key] a collection of data
- boolean = true or false values 
- hashes = key/value pair :name => "Momo"/ name: "Momo"
- symbols = :symbol


## Conditionals

conditional statements: if/else statements 
gives code logic
control flow
- execute logic based on a condition met

what do conditions return? boolean values: true or false

```ruby
if conditional
   code...
elsif conditional 
   code...
else
   code...
end
```



## Blocks => times block, loops while & until

- benefit? extra code, repetetive code
- times block allows execution of code a certain amount of times
- repeat a behavior UNTIL a condition is met

+= => logical operator

what it does: adds/increments by the number, then sets value of variable to new value


### While loop

Executes code while conditional is true

```ruby
n = 0
while n < 10
  puts n
  n += 1
end
```
This will print all the numbers from 0 to 9 (10 excluded).


### Until loop

Executes code while conditional is false

```ruby
i = 0
until i == 5
   puts i
   i += 1
end
```
This will print all the numbers from 1 to 4 (5 excluded).


### For loop

It allows a task to be repeated a specific number of times.

```ruby
for i in 1..8 do
    puts i
end
```
This will print all the numbers from 1 to 8.


The do in the for statement is optional, unless the code is placed on a single line:
```ruby
for i in 1..8 do puts i end
```


### The times loop

The times method provides an extremely convenient alternative to the for loop. The times method allows a task to be performed a specific number of times:

```ruby
5.times { |i| puts i }
```



# Object Initialization & Properties

## Key knowledge and vocabulary

- Instance: Unique objects created from a class.
- Instance method: A method which can be invoked on an individual objects.
- Instance variable: A variable which is accessible by all methods in an instance of an object.
- Macro: A method which creates or adds other methods on an object.
- Getter (reader) method: A method which makes object properties readable ‘outside’ of the object.
- Setter (writer) method: A method which assigns properties to an object.
- Object lifecycle: The concept that objects are created, events happen to an object, and it may eventually be destroyed in memory.
- Initialize method: A method which is triggered by a class whenever a new object is instantiated.

## Object Lifecycles

- Every object goes through a lifecyle: Create, Read, Update, Delete

## Initialize Method

- Constructor method
- Allows setting properties upon instantiation(creation)
- Not required!
- Invoked when `.new` is called
- `.new` will pass any arguments to initialize
- Initialize method will still assign attribute values to instance, but can not re-assign

## Setter

- Also knows as a 'writer' method
- Returns the value of instance variables
- Can use `instance_method_set`, but this could pose problems

## Getter

- Also known as a 'reader' method
- Returns the value of instance variables
- Can use `instance_method_get`, but this could pose problems

## Macro

- Abstraction
- A method that returns a method
- Shorter way of writing code
- `attr_accessor`, `attr_writer`, `attr_reader`
