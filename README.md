# Style Guide for IGIS Data Lab Python Code

* author -- Sang Il Bae
* version -- 1.0.0
* created -- 2022.06.02
* last edit -- 2022.06.02

## Introduction

<p>

This document provides coding convention for IGIS Data Lab Python codes. This style is meant to  prevent __unreadable__ codes that Python users mostly face. Most styles are directly implemented from PEP 8. This documents tackles other specific things. Mainly, this document is trying to say: please keep it readable and simple.

</p>


#### Constants

<p>

Please store global constant on a different file. Constants will use all capital letters with underscores separating words like so

```python
MAX_OVERFLOW = 32
```

Constants will not take calculated values or function-returned values. Following is a wrong example

```python
NOT_CONSTANT = 32 + 10
ALSO_NOT_CONSTANT = foo()
```

Also store constant on a separate file from the main script. 

```python
# c.py
# only stores constant
STO_CONS = 1


# main.py
# import it like so
import c as const

print(const.STO_CONS)
```

</p>


#### Comments

<p>

Please, please be sure to comment your work. PEP 8 says something about in-line comment and separated line comment, but ICG(IGIS Code Guide) couldn't care less.

```python
def foo():
    # comment here is fine
    return 42  # comment here is also fine
```

However, be sure to add 2 blank spaces when you put in-line comment. Also, comment with "#" between script, ICG recommends you start your comment with lower cases. Follwing is a __wrong example

```python
def bar():
    # This is wrong example
    return 42
```

</p>


#### Length of Single Line

<p>

Please put in your effort to limit your code's maximum length to 79 characters. Limiting your code's maximum length enables coders to put and compare their code side by side. However, 79 characters will not include in-line comments. 

```python
# this is wrong
def foo(arg1: int, arg2: int, arg3: int, arg4: str, arg5: set):
    ...

# this is correct
def foo(arg1: int, 
        arg2: int, 
        arg3: int, 
        arg4: str, 
        arg5: set):
    # looks odd but this is correct
    ...
```

</p>


#### Functions

<p>

I'm not implementing Variable Annotaion, introduced in PEP 526, which tends to make each code line longer. Instead, in function, I'm implementing argument type annotaion. Every function that takes an arguments should be written like so. Also, every function that returns a value should explicitly write their data type like so.

```python
# this is right
def foo(arg1: str):
    pass

def bar(arg1: str) -> str:
    return 'bar'

# this is wrong
def foo(arg1):
    pass

def foo(arg1: str):
    return 'bar'
```


</p>


#### Project Should Have...

<p>

All projects in the repository should have the followings. (The Exact file name)

* README.md
* CHANGELOG.md

```
## CHANGE LOG

### [Unreleased Version] - YYYY - MM - DD

<p>

Write your change here. - This line will also be your commit message

</p>

##### Added

<p>

</p>

##### Changed

<p>

</p>

##### Fixed

<p>

</p>
```


* LICENSE - mainly MIT LICENSE

```
The MIT License (MIT)

Copyright (c) 2016 Purpleworks

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```


</p>


#### Dictionary

* insert: ins
* create: create, mk
* generate: gen
* transform: trans
* delete: del, rm
* select: slt, get
