>幂次运算： num  ^  num
```diff
calc > 3^3 
27
```
>根号运算： num  **  num
```diff
calc > 8**3 
2.0
```
>if-else： if "条件判断" "expression" else "expression" 
```diff
calc > i=1
calc > if i==1 i=2 else i=3
calc > i
2
``` 
>for-to： for "起始值" to "结束值" : "要执行的算数指令"
```diff
calc > i=1
calc > for 0 to 3 : i=i*2
calc > i
16
``` 

>若输入一串运算,则会列出：(1)lex输出 (2)执行结果 (3)Three-Address Code
```diff
calc > 3^3/3-2*3
LexToken(NUMBER,3,1,0)
LexToken(POWER,'^',1,1)
LexToken(NUMBER,3,1,2)
LexToken(DIVIDE,'/',1,3)
LexToken(NUMBER,3,1,4)
LexToken(MINUS,'-',1,5)
LexToken(NUMBER,2,1,6)
LexToken(TIMES,'*',1,7)
LexToken(NUMBER,3,1,8)
3.0
[['op', 'arg1', 'arg2', 'result'], ['^', '3', '3', 't1'], ['/', 't1', '3', 't2'], ['*', '2', '3', 't3'], ['-', 't2', 't3', 't4'], ['=', 't4', ' ', 'a']]
