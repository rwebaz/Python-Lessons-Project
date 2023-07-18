---
title: Python Classes
layout: default
excerpt: Classes are a fundamental concept of `OOP` = "Object-Oriented Programming" in Python ...
hint: A class is like a "Construction Blueprint" or template that defines the properties (attributes) and behaviors (methods) that objects of the subject "class" possess ...
repo: Python-Lessons-Project
ver_date: 07-17-23
navigation_weight: 8
categories: page
---
{% include toc.md %}

**Note**. The following synopsis is derived from a prompt by the author via GPT-4 at Open AI on July 17th, 2023 [[1](#OPENAI){:.red}].

## Methods versus Attributes

> **Hint**. {{ page.hint }}

## Class Elements

Recuerde! Methods = "Behaviors".

And, Properties = "Attributes".

## Class Creation

The "class" as such provides a way to organize and structure code by grouping related data and functions together.

To create a "class" in Python, the expert Python programmer uses the `class` keyword followed by the name of the "class", as follows:

```python
class MyClass:
    def __init__(self, name):
        self.name = name
    
    def say_hello(self):
        print(f"Hello, {self.name}!")
```

## Discussion

In this example, `MyClass` is the name of the "class".

And, `MyClass` has two main members, as follows:

A. The `__init__` method

And,

B. The `say_hello` method.

### Constructors

The `__init__` method is a special behavior called a "constructor" and is executed when an "object of the class" is created.

The built-in "constructor" function allows the expert Python programmer to initialize and instantiate the new object's attributes.

In this case, the "constructor" takes a `name` parameter and assigns it to the `self.name` attribute.

### Regular Methods

Whereas, the `say_hello` method is simply a "regular" method that belongs to the class.

The now assigned "regular" method `say_hello` takes no parameters except `self` ...

;where `self` refers to the initial instance of the new "class".

### Making Objects

Once a "class" is defined, the programmer may create "objects" aka instances of the "class" ...

;where each object has its own set of attributes and can execute the methods defined in the class.

Creating an object and calling its methods may be illustrated by the following code block, as follows:

```python
obj = MyClass("John")  #Creates an object of the `MyClass` "class"

obj.say_hello()  #Calls the `say_hello` method of the newly formed object
```

### Execution

Finally, the short program prints a greeting using the `self.name` attribute.

When the program is run, the following execution output is rendered to the screen, as follows:

```python
Hello, John ...!
```

## Benefits

In addition to the built-in "constructor" method of `__init__` along with any "regular" methods assigned by the programmer ...

"Classes" can have other members, as well.

For example, "Class" attributes may shared by all and any instance of the "class" along with any methods that have been associated with the "class" itself.

## Conclusion

"Classes" do provide a way to achieve encapsulation, abstraction, inheritance, and polymorphism in Python.

These additional key principles of "Object Oriented Programming" or `OOP` allow the programmer to create reusable code, to organize related data and functions, and to model real-world entities.

## References

1. {:#OPENAI}[What Are Python Classes by GPT-4, July 2023](https://chat.openai.com){:title="Click to Review ..."}{:target="_blank"}

***

{% include flammarion-note.md %}

{% include patreon-link.md %}
