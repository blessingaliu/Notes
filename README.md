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





# Arrays and Iteration

## What is an array

- collection of data
- an object that stores other objectS
- contain strings, integers, hashes, boolean, symbols
- contain other arrays => nested arrays
- A Ruby class
- mutable - able to modify arrays and their elements

## How to initialize an array

### literal constructor
- create an array using bracket notation 

### class constructor 
- new method
- Array.new

## How to read arrays
- ordered, integer-indexed collection of any object 
- arrays will never change the order of elements 
- items inside of an array are referred to as elements 
- each element has an index number, the index number starts at 0

### Bracket notation
- Can take a single number, a beginning and end, and negative indices(this will start from the end of the array)
- .first and .last, .count, .length, .size

## How to modify arrays
- unshift
- shift
- pop
- sort
- push
- reverse
- << shovel method 


## Iterating over arrays
- enumerators used to iterate elements

- .each => iterate over each element, return value is the original array modified

- .collect/.map return value => a new array with modified elements

- .select => returns array with selected elements



# Intro to Object Orientation

## What is OO Programming?
    - procedural Ruby - does not provide a way to encapsulate, contain and reuse code
    - Abstraction, polymorphism, inheritance, encapsulation => 4 pillar of OO
    - makes for better design and organization of code 

## what does OO look like?
    - class 
    - instantiation => .new
    - instance/object
    - reader/writer => attributes/properties
    - methods/behaviors 

## Classes
 - blueprints for what each object is going to look like
 - what data is going to be contained within each object
 - what behaviors objects have
 - factory
 - car blueprint that can be used to make multiple instances of different cars with different states and behaviours
 - creating classes syntax: class/end keywords && capitalized class name

### Defining a class 

```ruby
class Customer
end
```

## Objects
 - from class blueprints, we can instantiate several objects
 - each object is unique to one another
 - .object_id to check object id
 - Everything in Ruby is an object
 - .new method to instantiate a new object


### Creating an object from a class using the new method 

```ruby
person1 = Person.new
person2 = Person.new
```


### Creating an object from a class using a custom method
```ruby
class Person
   @@no_of_persons = 0
   def initialize(name, address)
      @person_name = name
      @cust_addr = address
   end
end
```


## Methods
    - behaviors/messages/some type of function that objects or classes can perform on their own data
    
    - reusable

    - instance methods - perform on individual instances, behavior belongs to an instance, will need on the actual instance 

    - class methods - perform on class as a whole, behavior that belongs to a class
    will need to be called on the class entirely 


## Variables

    - local variables = scope is the method that it is defined 
    - instance variables = syntax: 1 @ / scope: class 
    - class variables = syntax: 2 @@ / scope: entire class
    - global variable = defined outside of a method/ accessible by entire file

## key words

    - instance
    - instance methods
    - class methods
    - instantiate
    - class variable
    - instance variable
    - objects



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
