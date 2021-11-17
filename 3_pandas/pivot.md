# Pivot方法

<!--
此处适合使用iPython把每一步的交互式结果重新整理。
例子显示一堆空值很奇怪，考虑优化一下给的示例value，或者把这里从抖音项目里来的真实需求的背景描述清楚。
-->

样例

```python
df = pd.DataFrame({'foo': ['one', 'one', 'one', 'two', 'two', 'two'], 'bar': ['A', 'B', 'C', 'A', 'B', 'C'], 'zoo': ['x', 'y', 'z', 'q', 'w', 't']})
df['is_exist']= True
df.pivot(index=['foo', 'bar'],columns='zoo',values='is_exist')
```

结果

```ipython
Out[11]: 
zoo         q     t     w     x     y     z
foo bar                                    
one A     NaN   NaN   NaN  True   NaN   NaN
    B     NaN   NaN   NaN   NaN  True   NaN
    C     NaN   NaN   NaN   NaN   NaN  True
two A    True   NaN   NaN   NaN   NaN   NaN
    B     NaN   NaN  True   NaN   NaN   NaN
    C     NaN  True   NaN   NaN   NaN   NaN
```
