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
