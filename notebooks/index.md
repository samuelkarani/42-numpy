
smbaabu
cpierce


```python
import numpy as np
```


```python
np.random.rand(3,2)
```







```python
np.random.rand(1, 12).reshape(4, 3)
```








```python
def inc_array(n):
    return np.random.rand(1, n)
inc_array(5).shape
```









```python
np.random.rand(10, 12)[:4,8:12]
```







```python
from matplotlib.pyplot import imshow
imshow(inc_array(5))
```



```python
import matplotlib.image as mpimg
img = mpimg.imread('./images/marie.png')
arr = inc_array(3)
sepia_img = img.dot(arr.T)
sepia_img /= sepia_img.max()
plt.axis('off')
plt.imshow(img)
```






```python
sepia_filter = np.array([[.393, .769, .189],
                         [.349, .686, .168],
                         [.272, .534, .131]])
sepia_img = img.dot(sepia_filter.T)
sepia_img /= sepia_img.max()
plt.axis('off')
plt.imshow(sepia_img)
```




```python
sepia_filter = np.array(np.random.rand(3, 3))
sepia_img = img.dot(sepia_filter.T)
sepia_img /= sepia_img.max()
plt.axis('off')
plt.imshow(sepia_img)
```
