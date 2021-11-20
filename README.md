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
