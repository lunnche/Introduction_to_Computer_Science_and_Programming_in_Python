# decomposition,abstraction,functions
分解，抽象，函数  

![image-20220213142826565](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220213142826565.png)

![image-20220213142850141](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220213142850141.png)

![image-20220213143912079](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220213143912079.png)

## good programming
*  more code not necessarily a good thing
*  measure good programmers by the amount of functionality
*  introduce functions
*  mechanism to achieve decomositon adn abstraction

## example - projector
* a projector is a black box
* don't know how it works
* know the interface:input/output
* connect any electronic to it that can communicate with that input
* black box somehow converts image from input source to a wall, manifying it 
* abstraction idea：do not need to know how projector works to use it. 

## example projector
* projecting large image for Olympics dercomposed into separate tasks for separate projects 
* each projector takes input and produces separate output
* all projectors work together to produce larger image
* decompositon idea: different devices work together to achieve an end goal  

## create structure with docomposition
* in projector example,separate devices
* in programming,divide code into modules
    * are self-contained
    * used to break up code
    * intended to be reusable
    * keep code organized
    * keep code coherent
* this lecture,achieve decomposition with functions
* in a few weeks,achieve decomposition with classes

## supress details with abstraction
* in projectro example, instructions for how to use it are sufficient,no need to know how to build one
* in programming,think of a piece of code as a black box
    * cannot see details
    * do not need to see details
    * do not want to see details
    * hide tedious coding details
* achieve abstraction with function specifications or docstrings

function specification 就说了三件事：输入，干什么，输出  

## functions 
* write reusable pieces/chunks of code,called functions
* functions are not run in a program until they are "called" or "invoked" in a program
* function characteristics:
    * has a name
    * has parameters(0 or more)
    * has a docstring(optional but recommended)
    * has a body
    * returns something 

![image-20220213154025085](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220213154025085.png)

## variable scope
* formal parameter gets bound to the value of actual parameter when function is called
* new scope/frame/enviroment created when enter a function
* scope is mapping of names to objects
```python
def f(x):
    x = x + 1
    print('in f(x): x =',x)
    return x

x = 3
z = f(x)
```

到p14 17：52


