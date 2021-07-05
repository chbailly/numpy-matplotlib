# np.array

## creation

```python
a = np.array([[2,3,4],
              [5,6,7]])

# Difference arange/linspace
np.arange( 0, 2, 0.3 )  // start, end , space
np.lintspace(0, 2, 100) // start, end, nb of elements

# arange does not create another array
# resize will create new array
a = np.arange(15).reshape(3, 5) // 3 rows, 5 columns
 
np.zeros(3,4)
np.ones(3,4)
```

## hstack/vstack

```python
a = np.array([[2,3,4],
              [5,6,7]])
              
b= np.array([[8,7,9]]) # must have the same dimensions (2)
np.vstack(
    (a,b) # SEQUENCE of ndarrays
) 

```



## slicing

```python
a = np.array([[2,3,4],
              [5,6,7]])


a[:,1] = 1 # change 2sd column with 1
a[[0,1],[0,2]] # 1 // a[0,0] = 1 and a[1,2] = 1
a[[0,1],[0,2]] = [6,7]

a[::-1] # reverse

```

# functions + vectorize function

```python
a = np.array([[2,3,4],
              [5,6,7]])
a + 1 // works !!!
np.sin(a) // works !!
# functions already vectorized

np.round, np.sum, np.max, np.std, ....

# Vectorize a function
def f(a, b):
	return 1 if a > b else 0
vf = np.vectorize(f)
vf([1,2,4], 3) => [_1, -1, 1]


```

