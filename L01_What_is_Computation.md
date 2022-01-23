## What is Computation?  

学啥？  

* represent knowledge with data strctures  
* iteration and recursion as computational metaphors  
* abstraction of procedures and data types  
* organize and modularize systems using object classes and methods  
* different classes of algorithms,searching and sorting  
* complexity of algorithms  

## WHAT DOES A COMPUTER DO  

* Fundamentally:  
    * performs calculations  
      a billion calculations per second!  
    * remembers results  
      100s of gigabytes of storage!  
* What kinds of calculations?  
    * built-in to the language  
    * ones that you define as the programmer  
* computers only know what you tell them  

## TYPES OF KNOWLEDGE  
* declarative knowledge is  statements of fact  陈述式支持  
* imperative knowledge is a recipe or "how-to"  命令式知识  
比如在课堂上抽中一人奖励google cardboard，怎么实现呢  
1. Students sign up at http://bit.ly/60001-raffle  
2. Ana opens her IDE  
3. Ana chooses a random num between 1st and nth responder  
4. Ana finds the number in the responders sheet.Winner!  

来了第一段代码，给出16和272之间的一个随机数：  
```python
import random
random.randint(16,272)
```

## A NUMERICAL EXAMPLE  
* square root of a number x is y such that y*y=x  
* recipe for duducing square root of a number x (16)  
1. Start with a guess,g  
2. if g*g is close enough to x,stop and say g is the answer  
3. Otherwise make a new guess by averaging g and x/g  
4. Using the new guess,repeat process until close enough  

|g|g*g|x/g|(g+x/g)/2|
|:-|:-|:-|:-|
|3|9|16/3|4.17|
|4.17|17.36|3.837|4.0035|
|4.0035|16.0277|3.997|4.000002|

## WHAT IS A RECIPE  
1. sequence of simple steps
2. flow of control process that specifies when each step is executed  
3. a means of determining when to stop  

## COMPUTERS ARE MACHINES  
* how to capture a recipe in a mechanical process  
* fixed program computer  
    * calculator  
* stored program computer  
    * machines stores and executes instructions  

![image-20220123170338171](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220123170338171.png)


## STORED PROGRAM COMPUTER  
* sequence of instructions stored inside computer
    * built from predefined set of primitive instructions
    1. arithmetic and logic
    2. simple tests
    3. moving data  

* special program (interpreter) executes each instruction in order  
    * use tests to change flow of control through sequence  
    * stop when done  

primitives 原语  

## BASIC PRIMITIVES  
* Turing showed that you can compute anything using 6 primitives  
6原语:
move left
move right
read
write
scan
do nothing

* modern programming languages have more convenient set of primitives  
* can abstract methods to create new primitives  

* anything computable in one language is computable in any other programming language  

## CREATING RECIPES  
* a programming language provides a set of primitive operations  
* expressions are complex but legal combinations of primitives in a programming language  
* expressions and computations have values and meanings in a programming language  

## ASPECTS OF LANGUAGES  
* primitive constructs 
    * English:words
    * programming language:numbers,strings,simple operators  

![image-20220123174345363](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220123174345363.png)

* syntax  
    * English:"cat dog boy" -> not syntactically valid
              "cat hugs boy" -> syntactically valid 
    * programming language:"hi"5 -> not sytactically valid  
                           3.2*5 -> syntactically valid  
* static semantics is which syntactically valid strings have meaning 
    * English:"I are hungry"->syntactically valid
                             but static semantic error
    * programming language:3.2*5 -> syntactically valid
                           3+"hi"-> static semantic error  


* semantics is the meaning associated with a syntactically correct string of symbols with no static semantic errors  
    * English:can hanve many meanings"Flying planes can be dangerous"
    * programming languages:have only one meaning but may not be what programmer intended  

## WHERE THINGS GO WRONG  
* syntactic errors
    * common and easily caught  
* static semantic errors  
    * some languages check for these before running program  
    * can cause unpredictable behavior
* no semantic errors but different meaning than what programmer intended 
    * program crashes,stops running
    * program runs forever
    * program gives an answer but different tahn expected  

## PYTHON PROGRAMS  
* a program is a sequence of definitions and commands 
    * definitions evaluated
    * commands executed by Python interpreter in a shell  
* commands(statements) instruct interpreter to do something
* can be typed directly in a shell or stored in a file that is read into the shell and evaluated  
    * Problem Set 0 will introduce you to these in Anaconda  

## OBJECTS  
* programs manipulate data objects  

* objects have a type that define the kinds of things programs can do to them  
    * Ana is a human so she can walk,speak English,etc.
    * Chebacca is a wookie so he can walk,"mwaaarhrhh",etc.  

* objects are  
    * scalar(cannot be subdivided)
    * non-scalar(have internal structure that can be accessed)  

## SCALAR OBJECTS  
* int -represent integers,ex.5  
* float -represent real numbers,ex.3.27  
* bool -represent Boolean values True and False  
* NoneType -special and has one value,None  
* can use type() to see the type of an object  

```python
>>> type(5)
int
>>> type(3.0)
float
```

## TYPE CONVERSIONS(CAST)  
* can convert object of one type to another
* float(3) convert integer 3 to float 3.0
* int (3.9) truncates float 3.9 to integer 3  

## EXPRESSIONS  
* combine objects and operators to form expressions  
* an expression has a value,which has a type  
* syntax for a simple expression
```
<object><operator><object>
```

## OPERATORS ON ints and floats  
* i+j -> the sum
* i-j -> the difference
* i*j -> the product
上面三个 if both are ints,result is int,if either or both are floats,result is float
* i/j -> division  result is float

* i%j -> the remainder when i is divided by j
* i**j -> i to the power of j  

看到p1 34：37

