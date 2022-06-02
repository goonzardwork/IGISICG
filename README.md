# Style Guide for IGIS Data Lab Python Code

* author -- Sang Il Bae
* version -- 1.0.0
* created -- 2022.06.02
* last edit -- 2022.06.02

## Introduction

<p>

This document provides coding convention for IGIS Data Lab Python codes. This style is meant to prevent __unreadable__ codes that Python users mostly face. Most styles are directly implemented from PEP 8. This documents tackles other specific things

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


#### Dictionary

* insert: ins
* create: create, mk
* generate: gen
* transform: trans
* delete: del, rm
* select: slt, get
