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

**4. What is PIP?**

PIP is acronym for Python Installer Package which provides a seamless interfacr to install various Python modules. It is a command line tool that can search for packages over the internet and install them without any user interaction.


**5. What are decorators in Python?**

Decorators in Python are essentially functions that add functionality to an existing function in Python without changing the structure of the function itself. They are represented the @decorator_name in Python and are called in a bottom-up fashion. For example:
	
	# decorator function to convert to lowercase
	def lowercase_decorator(function):
	   def wrapper():
	       func = function()
	       string_lowercase = func.lower()
	       return string_lowercase
	   return wrapper
	# decorator function to split words
	def splitter_decorator(function):
	   def wrapper():
	       func = function()
	       string_split = func.split()
	       return string_split
	   return wrapper
	@splitter_decorator # this is executed next
	@lowercase_decorator # this is executed first
	def hello():
	   return 'Hello World'
	hello()   # output => [ 'hello' , 'world']
 
The beauty of the decorators lies in the fact that besides adding functionality to the output of the method, they can even accept arguments for functions and can further modify those arguments before passing it to the function itself. The inner nested function, i.e. 'wrapper' function, plays a significant role here. It is implemented to enforce encapsulation and thus, keep itself hidden from the global scope.

	#decorator function to capitalize names
	def names_decorator(function):
	   def wrapper(arg1, arg2):
	       arg1 = arg1.capitalize()
	       arg2 = arg2.capitalize()
	       string_hello = function(arg1, arg2)
	       return string_hello
	   return wrapper
	@names_decorator
	def say_hello(name1, name2):
	   return 'Hello ' + name1 + '! Hello ' + name2 + '!'
	say_hello('sara', 'ansh')   # output => 'Hello Sara! Hello Ansh!'

**6. What is Garbage collection in Python?**

Garbage collection in automatic memory management technique, is used by programming languages to deallocate memory that is no longer required by the program.

Garbage collector in python locates and releases memory occupied by objects that can no longer be accessed or referenced by the programs code.


