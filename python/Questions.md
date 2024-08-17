# Python questions

**1. What is lambda in Python? Why is it used?**

Lambda is an anonymous function in Python, that can accept any number of arguments, but can only have a single expression. It is generally used in situations requiring an anonymous function for a short time period. 
Lambda functions can be used in either of the two ways:

	Assigning lambda functions to a variable:
	mul = lambda a, b : a * b
	print(mul(2, 5))    # output => 10
	
	Wrapping lambda functions inside another function:
	
	def myWrapper(n):
	 return lambda a : a * n
	
	mulFive = myWrapper(5)
	print(mulFive(2))    # output => 10

**2. What is zip function?**

   In python, zip() function returns a zip object that maps multiple containers identical indexes. It accepts an iterable, trasnform it into an iterator, and aggregates the elements depending on iterables passed. 

**3. What are generators in python?**

   Generators are most important python function that return an iterable collection of items, one at a time, in an organized manner.

**What is PIP?**

PIP is acronym for Python Installer Package which provides a seamless interfacr to install various Python modules. It is a command line tool that can search for packages over the internet and install them without any user interaction.
