```python
import numpy as np
```


```python
a = np.array([1,2,3])
b = np.array([(1.5,2,3), (4,5,6)], dtype = float)
c = np.array([[(1.5,2,3), (4,5,6)], [(3,2,1), (4,5,6)]], 
 dtype = float)
```


```python
np.zeros((3,4))
np.ones((2,3,4),dtype=np.int16)
d = np.arange(10,25,5)
np.linspace(0,2,9)
e = np.full((2,2),7) 
f = np.eye(2) 
np.random.random((2,2))
np.empty((3,2))
```




    array([[1.39069238e-309, 1.39069238e-309],
           [1.39069238e-309, 1.39069238e-309],
           [1.39069238e-309, 1.39069238e-309]])




```python
np.save('my_array', a)
np.savez('array.npz', a, b)
np.load('my_array.npy')
```




    array([1, 2, 3])




```python
a.shape 
len(a) 
b.ndim 
e.size
b.dtype 
b.dtype.name 
b.astype(int) 

```




    array([[1, 2, 3],
           [4, 5, 6]])




```python
from numpy import array
g = a - b
array([[-0.5, 0. , 0. ],
[-3. , -3. , -3. ]])
np.subtract(a,b) 
b + a
array([[ 2.5, 4. , 6. ],
[ 5. , 7. , 9. ]])
np.add(b,a) 
a / b
array([[ 0.66666667, 1. , 1. ],
[ 0.25 , 0.4 , 0.5 ]])
a * b
array([[ 1.5, 4. , 9. ],
[ 4. , 10. , 18. ]])
np.divide(a,b) 
np.multiply(a,b) 
np.exp(b) 
np.sqrt(b) 
np.sin(a) 
np.cos(b)
np.log(a) 
e.dot(f)
array([[ 7., 7.],
[ 7., 7.]])
```




    array([[7., 7.],
           [7., 7.]])




```python
a == b 
array([[False, True, True],
[False, False, False]], dtype=bool)
a < 2 
array([True, False, False], dtype=bool)
np.array_equal(a, b) 
```




    False




```python
i = np.transpose(b) 
i.T 
```




    array([[1.5, 2. , 3. ],
           [4. , 5. , 6. ]])




```python
b.ravel() 
g.reshape(3,-2)
```




    array([[-0.5,  0. ],
           [ 0. , -3. ],
           [-3. , -3. ]])




```python
np.concatenate((a,d),axis=0)
array([ 1, 2, 3, 10, 15, 20])
np.vstack((a,b)) 
array([[ 1. , 2. , 3. ],
[ 1.5, 2. , 3. ],
[ 4. , 5. , 6. ]])
np.r_[e,f]
np.hstack((e,f)) 
array([[ 7., 7., 1., 0.], 
[ 7., 7., 0., 1.]])
np.column_stack((a,d)) 
array([[ 1, 10],
[ 2, 15],
[ 3, 20]])
np.c_[a,d] 
```




    array([[ 1, 10],
           [ 2, 15],
           [ 3, 20]])




```python
np.hsplit(a,3) 
[array([1]),array([2]),array([3])]
np.vsplit(c,2) 
[array([[[ 1.5, 2. , 1. ],
[ 4. , 5. , 6. ]]]), 
array([[[ 3., 2., 3.],
[ 4., 5., 6.]]])]
```




    [array([[[1.5, 2. , 1. ],
             [4. , 5. , 6. ]]]),
     array([[[3., 2., 3.],
             [4., 5., 6.]]])]


