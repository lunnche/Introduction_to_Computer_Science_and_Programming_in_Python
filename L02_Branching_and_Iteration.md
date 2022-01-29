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

## INPUT/OUTPU: input("")  
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
