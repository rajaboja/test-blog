* #### There's a helpful utility to convert a 'fixed width formatted' string into a Pandas Dataframe. 


```
import pandas as pd
from io import StringIO

text = """
    [S] [C]         [Z]            
[F] [J] [P]         [T]     [N]    
[G] [H] [G] [Q]     [G]     [D]    
[V] [V] [D] [G] [F] [D]     [V]    
[R] [B] [F] [N] [N] [Q] [L] [S]    
[J] [M] [M] [P] [H] [V] [B] [B] [D]
[L] [P] [H] [D] [L] [F] [D] [J] [L]
[D] [T] [V] [M] [J] [N] [F] [M] [G]
 1   2   3   4   5   6   7   8   9 
 """

pd.read_fwf(StringIO(text),names=range(9))
```

```
 	0 	1 	2 	3 	4 	5 	6 	7 	8
0 	NaN 	[S] 	[C] 	NaN 	NaN 	[Z] 	NaN 	NaN 	NaN
1 	[F] 	[J] 	[P] 	NaN 	NaN 	[T] 	NaN 	[N] 	NaN
2 	[G] 	[H] 	[G] 	[Q] 	NaN 	[G] 	NaN 	[D] 	NaN
3 	[V] 	[V] 	[D] 	[G] 	[F] 	[D] 	NaN 	[V] 	NaN
4 	[R] 	[B] 	[F] 	[N] 	[N] 	[Q] 	[L] 	[S] 	NaN
5 	[J] 	[M] 	[M] 	[P] 	[H] 	[V] 	[B] 	[B] 	[D]
6 	[L] 	[P] 	[H] 	[D] 	[L] 	[F] 	[D] 	[J] 	[L]
7 	[D] 	[T] 	[V] 	[M] 	[J] 	[N] 	[F] 	[M] 	[G]
8 	1 	2 	3 	4 	5 	6 	7 	8 	9
```
