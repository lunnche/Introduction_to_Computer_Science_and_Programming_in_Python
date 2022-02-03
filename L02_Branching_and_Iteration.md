## BRANCHING,ITERATION  

这个课会在课前至少一小时，提供幻灯和代码，贴心  

上节课学的最重要的一点就是computer only does what it is told .  

## LAST TIME  
* syntax and semantics  
* scalar objects  
* simple operations  
* expressions,variables and values  

## TODAY 
* string object type  
* branching and conditionals  
* indentation  
* iteration and loops  

## STRINGS  
* letters,special characters,spaces,digits  
* enclose in <font color="red">quotation marks or single quotes</font>
hi = "hello there"
* <font color="red">concatenate</font> strings  
name = "ana"

greet = hi + name 

greeting = hi + " " + name  

* do some <font color="red">operations</font> on a string as defined in Python docs  
silly = hi + " " + name * 3  

注意的是，星号只允许string 和 number之间相乘。  

## INPUT/OUTPUT:print  
* used to <font color="red">output</font> stuff to console  
* keyword is print  

```python
x = 1
print(x)
x_str = str(x)
print("my fav num is", x, ".", "x =", x)
print("my fav num is " + x_str + ". " + "x = " + x_str)
```

注意第一个pritn里用了逗号，第二个用了加号。
如果你用了逗号，python就会自动为你隔开的东西之间加上空格。  
如果你用逗号，被隔开的东西并非都必须是字符串。用加号的必须都是字符串。  

## INPUT/OUTPUT: input("")  
* prints whatever is in the quotes  
* user types in something and hits enter  
* binds that value to a variable  
```
text = input("Type anything... ")
print(5*text)  
```
* input <font color="red">gives you a string</font> so must cast if working with numbers
```python
num = int(input("Type a number... "))
print(5*num)
```

p5 13:16

* iput <font color="red">gives you a string</font> so must cast if working with numbers  
```python
num = int(input("Type a number... "))
print(5*num)
```

## COMPARISON OPERATORS ON int,float,string  
* i and j are variable names
* comparisons below evaluate to a Boolean
```
i > j
i >= j
i < j
i <= j
i == j -> equality test, True if i is the same as j
i != j -> inequality test, True if i not the same as j
```

## LOGIC OPERATORS ON bools
* a and b are variable names (with Boolean values)
```
not a -> True if a is False
         False if a is True
a and b -> True if both are True
a or b -> True if either or both are True
```

![image-20220203113803944](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203113803944.png)

## CONTROL FLOW - BRANCHING

![image-20220203114052330](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203114052330.png)

* <condition> has a value True of False
* evaluate expressions in that block if <condition> is True  

## INDENTATION
* matters in Python
* how you denote blocks of code
```python
x = float(input("Enter a number for x: "))
y = float(input("Enter a number for y: "))
if x == y:
    print("x and y are equal")
    if y != 0:
        print("therefore, x / y is",x/y)
    elif x < y:
        print("x is smaller")
    else:
        print("y is smaller")
    print("thanks!")
```

## CONTROL FLOW:while LOOPS
* <condition> evaluates to a Boolean
* if <condition> is True,do all the steps inside the while code block
* check <condition> again
* repeat until <condition> is False  

## CONTROL FLOW:
while and for LOOPS
* iterate through numbers in a sequence

```python
# more complicated with while loop
n=0
while n < 5:
    print(n)
    n = n+1

# shortcut with for loop
for n in range(5):
    print(n)

```

## CONTROL FLOW:for LOOPS
* each time through the loop, <variable> takes a value
* first time, <variable> starts at the smallest value
* next time, <variable> gets the prev value +1
* etc.  

## range(start,stop,step)
* default values are start = 0 and step = 1 and optional
* loop until value is stop - 1

```python
mysum = 0
for i in range(7,10):
    mysum += i
print(mysum)  

mysum = 0
for i in range(5,11,2):
    mysum += i
print(mysum)
```

## break STATEMENT
* immediately exits whatever loop it is in
* skips remaining expressions in code block
* exits only innermost loop!

![image-20220203144227436](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220203144227436.png)

ppt看完了，课还没听完，去听课，再补充
