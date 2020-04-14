<h1>Convert  image to an array for making dataset</h1>

<h3>In this project at first we see how to load an image and show this using pillow.</h3> 

<p>Pillow is a python image library. It is by deafult installed by andconda. It is even required for simple image loading and saving in other Python scientific libraries such as Matplotlib.</p>


<h4>Load image using pillow</h4>

```
from PIL import Image
img = Image.open('opera_house.jpg')
```
<h4>Summerize image details</h4>

```
print(img.format)
print(img.mode)
print(img.size)
```

<h4>Now see how to convert images to numpy array</h4>

<p>For this at first we need to import asarray function from numpy.
The asarray() function is used to convert an given input to an array. Input data, in any form that can be converted to an array. This includes lists, lists of tuples, tuples, tuples of tuples, tuples of lists and ndarrays.</p>
<br>
<p>Now we pass img object to the asarray() function and it returns an array.</p>

```
#import library
from numpy import asarray
```
```
#convert image to numpy array which is loaded before
data = asarray(img)
```
<h5>We can see the type of this array using python python built in type() function and it returns the type of this array</h5>

```
type(data)
```
<h5>Check the shape of this array</h5>

```
print(data.shape)
```

<h5>Now we see also how to back mean how to create Pillow object from this numpy array<h5>

```
img2 = Image.fromarray(data)
img2
```

<p>We can also do this by Matplotlib with pillow installed.</p>
<p>We can load image with imread() function. </p>
<p>At first we import image and pyplot from matplotlib</p>


```
#Load libraries of matplotlib
from matplotlib import image,pyplot
#load image
data = image.imread('opera_house.jpg')
```
<p>Now chekc the type of this data using the same thing we have done before.</p>

```
type(data)
```
<p>Now check the data details </p>

```
print(data.dtype)
print(data.shape)
```
<p>Now we show the image </p>

```
pyplot.imshow(data)
pyplot.show()
```
For details chekc <a href="https://github.com/Jugal-Chanda/Convert-image-to-an-array-for-making-dataset/blob/master/ImgToData.ipynb">Check This Code</a>