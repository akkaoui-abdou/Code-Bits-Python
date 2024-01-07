# Code-Bits-Python

### Password Validator

```python 
Password validator is a program that validates passwords to match specific rules. For example, the minimum length of the password must be eight characters long and it should have at least one uppercase letter in it. 

A valid password is the one that conforms to the following rules:
 - Minimum length is 5;
 - Maximum length is 10;
 - Should contain at least one number;
 - Should contain at least one special character (such as &, +, @, $, #, %, etc.);
 - Should not contain spaces.
'''
from string import punctuation
def Validator(x):
         
         n = (i for i in range(0,11))
         if ( (" " not in x) and ( len(x) >= 5 and len(x) <= 10)):
             for k in n:
                 if (str(k) in x):
                     for i in punctuation:
                         if i in x:
                            return True
         return False
p = input()
print(f"{p} is a valid password : {Validator(p)}")
        
```

### Password Generator
```python 
import string
from random import *

letters = string.ascii_letters 
digits = string.digits 
symbols = string.punctuation
chars = letters + digits + symbols

min_length = 8
max_length = 16
password = "".join(choice(chars) for x in range(randint(min_length, max_length)))
print(password)
```
## Fix error

### Language: Python
### Task Description: Fix the error in the class child to print '93 93'.
```python 
class Parent:
    def __init__(self, param):
        self.a = param
class Child(Parent):
    def __init__(self, param):
        # Before fixed error
        #super().__init__(self, param)
        super().__init__(param)
        self.b = param
    def __str__(self):
        return f"{self.b} {self.a}"


## Quiz Python
Source: https://realpython.com/quizzes/

obj = Child(93)

print(obj.a, obj.b)
```
