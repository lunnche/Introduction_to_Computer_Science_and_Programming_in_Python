## string manipulation,guess and check,approximations,bisection  
## last time
* strings
* branching-if/elif/else
* while loops
* for loops
之前看了slide，没看视频，去补

## TODAY
* string manipulation
* guess and check algorithms
* approximate solutions
* bisection method  

## strings
* think of as a sequence of case sensitive characters
* can compare strings with `==`,`>`,`<` etc.
* len() is a function used to retrieve the length of the string in the parentheses

```
s = "abc"
len(s) -> evaluates to 3
```

## strings
* square brackets used to perform indexing into a string to get the value at a certain index/position

![image-20220203151032627](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203151032627.png)

* can slice strings using [start:stop:step]
* if give two numbers,[start:stop],step=1 by default
* you can also omit numbers and leave just colons

![image-20220203151213452](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203151213452.png)

注意，切片里边是： 不是，

s[::-1] 实际上就是 反转字符串

* string are "immutable"-cannot be modified

![image-20220203152206695](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203152206695.png)

到silde7 视频L02开始就没看了，补

视频看到p11  10：56

## for LOOPS RECAP  
* for loops have a loop variable that iterates over a set of values

```
for var in range(4):  -> var iterates over values 0,1,2,3
    <expressions>     -> expressions indide loop executed with each value for var

for var in range(4,6): -> var iterates over values 4,5
    <expressions>  
```

* range is a way to iterate over numbers, but a for loop variable can iterate over any set of values, not just numbers!

## STRINGS AND LOOPS
* these two code snippets do the same thing
* bottom one is more "pythonic"

```
s = "abcdefgh"
for index in range(len(s)):
    if s[index] == 'i' or s[index] == 'u':
        print("There is an i or u")  

for char in s:
    if char == 'i' or char == 'u':
        print("There is an i or u")
```

视频到p11   15：55
啥叫"pythonic" 就是说你一眼就能明白这个代码是干啥的  
不是迭代一组数，而是直接迭代字符串中的每个字符  

跟python无关 虽然元音只有 aeiou  但单独表示一个字母
"qefhilmnorsxAEFHILMNORSX" 前边都应该加 "an" 而不是 "a"
例如：
```
Give me an R!
```

来看看这门课截止到目前掌握的技能和算法：


![image-20220206113649454](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220206113649454.png)

![image-20220206114001507](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220206114001507.png)

## 简单算法
1. guess and check (exhaustive enumeration)  
* the process below also called <font color="red">exhaustive enumeration</font>  

* given a problem...
* you are able to <font color="red">guess a value</font> for solution
* you are able to <font color="red">check if the solution is correct</font>
* keep guessing until find solution or guessed all values

最简单的情况：
```python
cube = 8
for guess in range(cube+1):
    if guess**3 == cube:
        print("Cube root of", cube, "is", guess)
```

但是考虑不周，加点细节：
```python
cube = 8
for guess in range (abs(cube)+1):
    if guess**3 >= abs(cube):
        break
    if guess**3 != abs(cube):
        print(cube, 'is not a perfect cube')
    else:
        if cube < 0:
            guess = -guess
        print('Cube root of '+str(cube)+' is '+str(guess))
```

上边考虑了负数  
啥玩意叫perfect cubes ？9就是 8不是 其实就是立方数，我猜  
所以呢，上边的程序用guess and check 算法只能算完全立方数的立方根，算不了一个任意数的立方根。  

## APPROXIMATE SOLUTIONS  
* <font color="red">good enough</font> solution
* start with a guess and increment by some <font color="red">small value</font>
* keep guessing if $\left |guess^3 - cube\right | \geqslant \epsilon$ for some <font color="red">small epsilon</font>  


* decreasing increment size -> slower program
* increasing epsilon   -> less accurate answer  

## APPROXIMATE SOLUTION - cube root 
```python
cube = 27
epsilon = 0.01
guess = 0.0
increment = 0.0001
num_guesses = 0
while abs(guess**3 - cube) >= epsilon and guess <= cube:
    guess += increment
    num_guesses += 1
print('num_guesses =', num_guesses)
if abs(guess**3 - cube) >= epsilon:
    print('Failed on cube root of', cube)
else:
    print(guess, 'is close to the cube root of',cube)
```

加上`guess <= cube`是为了防止出现陷入无限循环的情况，一口没吃到包子馅，下一口过了

## 二分搜索
the larger the space actually is that I need to search the better it is to use bisection search.  

到p11 39：54

* half interval each iteration  
* new guess is halfway in between

![image-20220212172928082](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220212172928082.png)

## bisection search -cube root  
```python
cube = 27
epsilon = 0.01
num_guessed = 0
low = 0
high = cube
guess = (high + low)/2.0  
while abs(guess**3 - cube) >= epsilon:
    if guess**3 < cube :
        low = guess  
    else :
        high = guess
    guess = (high + low)/2.0
    num_guesses += 1
print 'num_guesses =', num_guesses
print guess, 'is close to the cube root of ',cube
```

## bisection search convegence
* search apces
    * first guess:  N/2
    * second guess: N/4
    * kth guess:    $N/2^k$
* guess converges on the order of $\log_2 N$ steps
这步怎么得到的？
因为最后找到1个数，所以$\frac{N}{2^k}=1$
所以：$k=\log_2 N$

* bisection search works when value of function varies monotonically with input  
* code as shown only works for positive `cubes > 1` -why?
* challenges  modify to work with negative cubes!
              modify to work with `x<1`!
              
             
完结撒花🌺
