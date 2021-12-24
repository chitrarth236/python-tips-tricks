## 3 Types of Variables in OOP Python
1. Instance Variable (Object Level)
2. Static Variable (Class Level)
3. Local Varibale (Method Level)


### 1. Instance Variable

- ####  How to Declare:
  - Using object variable (Outside the class)
  - Using self (Inside the constructor and instance method)

- #### How to Access:
  - Using object variable (Outside the class)
  - Using self (Inside the constructor and instance method)

- #### How to Delete:
  - Using del keyword with object variable, Outside the class(ex. del objectname.variablename)
  - Using del keywork with self within a class (ex. del self.variablename)
  
### 2. Static Variable

- ####  How to Declare:
  - Directly within class but outside on any method and constructor
  - Using class name within in any method(instance, static, class)/constructor using class name
  - Using cls variable in class method
  
- #### How to Access:
  - Using self or class name inside instance methods/constructor
  - Using cls variable or class name inside class and static methods
  - Using object variable or class name outside the class

- #### How to Modify:
  - Using class name inside or outside the class
  - Using cls variable in class method
  
- #### How to Delete:
  - Using del keyword with class name, Outside the class(ex. del classname.variablename)
  - Using del keyword with cls var inside a class method(ex. del cls.variablename)
  
### 3. Local Variable
	
  - Local variables are created and used inside the method
  - they are not accessible outside the method



## 3 Types of Methods in OOP Python
1. Instance Method
2. Static Method 
3. class Method 

### 1. Instance Method

  - Uses Instance variables inside the method
  - Uses self variable to point the current object
  - self is used to for instance variable manipulation inside Instance method
  - Accessible via object reference variable

### 2. Class Method

  - Uses static variables inside the method
  - @classmethod decorator is used to declare it
  - uses cls variable to point the current class
  - Accessible via classname or object reference

### 3. Static Method
  - No Instance or Static variable is used inside these method
  - @staticmethod decorator is used to declare it
  - Accessible via classname or object reference
	
	
## Overloading	

### 1. Constructor Overloading
  - Constructors having same name but different arguments
  - Not supported in Python
  - If you have multiple constructors with different arguments, only **constructor defined at last will be considered**

### 2. Method Overloading
	- Methods having same name but different arguments
	- Not supported in Python
	- If you have multiple methods with different arguments, only **method defined at last will be considered**

### 3. Operator Overloading



## Inheritance

### Types of Inheritance in Python
	- Single Inheritance
	- Multi Level Inheritance
	- Hierarchical Inheritance
	- Multiple Inheritance (Yes, Python supports multiple inheritance, using **MRO** and **C3** algorithm)
	- Hybrid Inheritance

### 1. Constructor Overriding

### 2. Method Overriding

