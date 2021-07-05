

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0,10,100)
plt.plot(x, np.sin(x), 'r--', linewidth=3, label="sin") # red dash lines
plt.plot(x, np.cos(x), 'b', label="cos")
plt.xlim(0,6) # 0->6 for absciss
plt.xticks(
    [0,2,6], 
    ["x=0", "x=2", "x=6"],
    rotation='vertical')

# both can work to add text...
plt.text(2, np.cos(2), "<-cos(2)")
plt.annotate("cos2", [2, np.cos(2)]) # more powerfull

plt.savefig("example.png")
plt.legend()
plt.show()
```



![](.\example.png)

# other types of graph

* plt.scatter => works the same !
* plt.bar => idem

# Disposition

## easy way
```python
pyplot.figure(1)

pyplot.subplot(1, 2, 1) # grid 1row x 2columns  position 1
pyplot.scatter(range(5), [x ** 2 for x in range(5)], color = 'blue')

pyplot.subplot(2, 2, 2)  # grid 2rows x 2columns  position 1
pyplot.plot(range(5), color = 'red')

pyplot.subplot(2, 2, 4)
pyplot.bar(range(5), range(5), color = 'green')
```

![](.\dispo.png)

## clean way
```python
figure = pyplot.figure()
axes = figure.add_subplot(111) # axes is a subplot
axes.set_xlabel('axe des x')
axes.set_ylabel('axe des y')
axes.set_title('titre du graphe 1')

# create a figure with axes in a single line
myfig, (ax1, ax2) = pyplot.subplots(nrows = 2, ncols = 1)

# current axe or figure
axes = plt.gca()
fig = plt.gcf()
```

