
6A:  Python OOP: Abstract Class & Method Example

##  AIM

To create an **abstract class** named `Shape` with an **abstract method** `calculate_area`, and implement this method in two subclasses: `Rectangle` and `Circle`.

---

##  ALGORITHM

1. **Import ABC module**:
   - Use `from abc import ABC, abstractmethod` to define abstract classes and methods.

2. **Create Abstract Class `Shape`**:
   - Define an abstract method `calculate_area()` with `@abstractmethod`.

3. **Create Subclass `Rectangle`**:
   - Set default values for `length` and `breadth`.
   - Override `calculate_area()` to compute the rectangle area.

4. **Create Subclass `Circle`**:
   - Set default value for `radius`.
   - Override `calculate_area()` to compute the circle area.

5. **Create Objects & Call Methods**:
   - Instantiate `Rectangle` and `Circle`.
   - Call their `calculate_area()` methods.

---

##  Program
```

from abc import ABC
class type_shape(ABC): 
    def area(self):
        pass

class Rectangle(type_shape):
    length = 6
    breadth = 4
    def area(self):
        return self.length * self.breadth

class Circle(type_shape):
    radius = 7
    def area(self):
        return 3.14*self.radius**2
class Square(type_shape):
    length = 4
    def area(self):
        return self.length**2

class triangle(type_shape):
    length = 5
    width = 4
    def area(self):
        return 0.5*self.length*self.width
  
r = Rectangle()
c = Circle() 
s = Square() 
t = triangle() 
print("Area of a rectangle:", r.area())
print("Area of a circle:", c.area()) 
print("Area of a square:", s.area()) 
print("Area of a triangle:", t.area())
```
## Output
<img width="796" height="280" alt="image" src="https://github.com/user-attachments/assets/896771d4-5625-4573-87c2-bdb30a885326" />

## Result
The program successfully demonstrates the concept of abstract classes and method overriding in Python.
The abstract class Shape defines the structure, and the subclasses Rectangle and Circle implement their own versions of the calculate_area() method.


6B:  Python OOP: Encapsulation with Private Members

##  AIM
To implement Encapsulation in Python by defining a class Rectangle with private member variables __length and __breadth.


##  ALGORITHM

1.Define the Class:

Create a class Rectangle with two private attributes: __length and __breadth.
2.Initialize Variables:

Use the __init__() constructor to set initial values for __length and __breadth.
3.Print Values:

Display the private variables from within the class to demonstrate access.
4.Instantiate the Object:

Create an object of the Rectangle class to trigger the constructor.


##  Program
```

class Rectangle:
    __length = 0 
    __breadth = 0
    def __init__(self):
      self.__length = 5
      self.__breadth = 3
      print(self.__length)
      print(self.__breadth)
   
  obj = Rectangle()
```
## Output
<img width="290" height="132" alt="image" src="https://github.com/user-attachments/assets/3df50c49-54d3-4b3e-be8f-056ea7e6cc3b" />

## Result
Thus, the program to implement Encapsulation with Private Members in Python was executed successfully and produced the expected result.


6C:  Method Overriding- Fish and Shark Class Inheritance in Python

AIM:

To write a Python program that demonstrates class inheritance by creating a parent class Fish with a method type, and a child class Shark that overrides the type method.


ALGORITHM:

1.Define the Fish class with a method named type() that prints "fish".

2.Define the Shark class as a subclass of Fish, and override the type() method to print "shark".

3.Create an instance of the Fish class named obj_goldfish.


4.Create an instance of the Shark class named obj_hammerhead.``

5.Use a for loop to iterate over both objects.

6.Within the loop, call the type() method using the loop variable.

7.Output will demonstrate method overriding: printing "fish" and "shark" accordingly.


#Program:
```

class Fish:
    def type(self):
        print("fish")

class Shark(Fish):
	def type(self):
	    print("shark")

obj_goldfish=Fish()
obj_hammerhead=Shark()

obj_goldfish.type()
obj_hammerhead.type()
```

#Output:

<img width="631" height="391" alt="image" src="https://github.com/user-attachments/assets/e9a37dcd-4ef3-47b1-8ad2-ecc3a4b2a39a" />

#Result:

Thus, the program to implement Method Overriding using Fish and Shark Class Inheritance in Python was executed successfully and produced the expected result.


6D:  Python OOP: Operator Overloading (Less Than `<`)


##  AIM:
To write a Python program that overloads the less-than (<) operator using the __lt__() method to compare two objects based on their attributes.

##  ALGORITHM:

1.Start the program.

2.Define a class (e.g., Student).

3.Create a constructor (__init__) to initialize object attributes
(example: marks).

4.Overload the less-than operator by defining the method:
5.Use the < operator to compare the objects.

6.Display the comparison result based on the overloaded method.

7.End the program.
##  PROGRAM:
```

class A:
    def __init__(self,a):
        self.a=a
    def __gt__(self,other):
        return self.a<other.a
ob1=A(200)
ob2=A(30)
if(ob1<ob2):
    print("ob2 is less than ob1")
else:
    print("ob1 is less than ob1")
```
## OUTPUT
<img width="603" height="184" alt="image" src="https://github.com/user-attachments/assets/63d12b29-1b1c-4bd8-ad1d-1e38b6e5b858" />


## RESULT
Thus, the program to implement Operator Overloading (Less Than <) in Python was executed successfully and produced the expected result.


6E:  Python OOP: Polymorphism with Classes

##  AIM

To create two specific classes — `Beans` and `Mango`. Then, create a **generic function** that can accept any object and determine its **type** (Fruit or Vegetable) and **color**, using polymorphism.

---

##  ALGORITHM

1. **Create Class `Beans`**:
   - Define `type()` method that prints `"Vegetable"`.
   - Define `color()` method that prints `"Green"`.

2. **Create Class `Mango`**:
   - Define `type()` method that prints `"Fruit"`.
   - Define `color()` method that prints `"Yellow"`.

3. **Define Generic Function `func(obj)`**:
   - Call `obj.type()` and `obj.color()` — this works with both `Beans` and `Mango` objects, showcasing **polymorphism**.

4. **Create Objects**:
   - Instantiate `Beans` and `Mango`.
   - Pass them to `func()` and execute the program.

---

##  Program
```
class Beans(): 
    def type(self):
         print("Vegetable")
    def color(self):
        print("Green")
class Mango(): 
    def type(self):
         print("Fruit")
    def color(self):
        print("Yellow")
def func(obj): 
        obj.type()
        obj.color()
obj_beans = Beans() 
obj_mango = Mango() 
func(obj_beans) 
func(obj_mango)

```
## Output
<img width="487" height="228" alt="image" src="https://github.com/user-attachments/assets/7deae8b8-16d9-4f8a-8168-55f44a7d2667" />

## Result
The program successfully created two classes, Beans and Mango, and used a generic function to display their details.
