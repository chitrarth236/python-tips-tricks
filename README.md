# Advanced Python Tricks and Tips - Notes

### [Python Object Oriented Programming Tips/Tricks](https://github.com/chitrarth236/python-tips-tricks/tree/main/Python_OOP_tips_tricks_notes)

- ### Modifiying the value of static variable
If you try to modify the value of static variable by using either self or object variable, then the value of static variable won't be changed, instead just a new instance variable with the same name will be added to that object.

```python
class Demo:
    #static variable s with initial value 5
    s = 5
    def __init__(self):
        #instance variable i = 10
        self.i = 10

d1 = Demo()
print("d1.s: "+str(d1.s)+", d1.i: "+str(d1.i))
d2 = Demo()
print("d1.s: "+str(d2.s)+", d1.i: "+str(d2.i))

#trying to modify s using object variable,
#but instead it will create new instace variable in the object
d1.s = 7

print("d1.s: "+str(d1.s)+", d1.i: "+str(d1.i))
print("d1.s: "+str(d2.s)+", d1.i: "+str(d2.i))
print("Demo.s: "+str(Demo.s))

#Output:

#initial values of s and i
#d1.s: 5, d1.i: 10
#d1.s: 5, d1.i: 10
#after modification new instance variable s=7 is created in d1,
#and value of static variable s=5 is there in other object
#d1.s: 7, d1.i: 10
#d1.s: 5, d1.i: 10
#Demo.s: 5 

```
