# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import opencv.

### Step2:
Read the original Image.

### Step3:
Store the required conversion of the image in a variable.

### Step4:
Show the image stored in the given variable.

### Step5:
Destroy all the windows and end the program.

## Program:
```python
# Developed By: Aakash S
# Register Number: 212221240001
# i) Convert BGR and RGB to HSV and GRAY
import cv2
houseImage = cv2.imread('flo.jpg')
cv2.imshow('Original Image',houseImage)
hsvImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvImage)
hsvImage1=cv2.cvtColor(houseImage,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvImage1)
grayImage = cv2.cvtColor(houseImage,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayImage)
grayImage1 = cv2.cvtColor(houseImage,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayImage1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

```python
# ii)Convert HSV to RGB and BGR

import cv2
houseHSVImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original HSV Image',houseHSVImage)
RGBImage = cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2RGB)
cv2.imshow('BGR2HSV',RGBImage)
BGRImage=cv2.cvtColor(houseHSVImage,cv2.COLOR_HSV2BGR)
cv2.imshow('RGB2HSV',BGRImage)
cv2.waitKey(0)
cv2.destroyAllWindows()



```
```python
# iii)Convert RGB and BGR to YCrCb
import cv2
houseImage = cv2.imread('dip1.jpeg')
cv2.imshow('Original HSV Image',houseImage)
YCrCb_image = cv2.cvtColor(houseImage, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR2HSV',YCrCb_image)
YCrCb_image1 = cv2.cvtColor(houseImage, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB2HSV',YCrCb_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('dip1.jpeg')
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
mergeBgr = cv2.merge((blue,green,red))
cv2.imshow('Merged BGR image',mergeBgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
```python
# v) Split and merge HSV Image
import cv2
image = cv2.imread('dip1.jpeg')
hsv = cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue - Image',h)
cv2.imshow('Saturation - Image',s)
cv2.imshow('Gray - Image',v)
mergedHSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',mergedHSV)
cv2.waitKey(0)
cv2.destroyAllWindow
```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>

![Output](1.png)
![Output](1\)i.png)
![Output](1\)ii.png)
![Output](1\)iii.png)
![Output](1\)iv.png)
### ii) HSV to RGB and BGR
<br>

![Output](2.png)
![Output](2\)i.png)
![Output](2\)ii.png)
### iii) RGB and BGR to YCrCb
<br>

![Output](3.png)
![Output](3\)i.png)
![Output](3\)ii.png)

### iv) Split and merge RGB Image
<br>


![Output](4.png)
![Output](4\)i.png)
![Output](4\)ii.png)
![Output](4\)iii.png)

### v) Split and merge HSV Image
<br>

![Output](5.png)
![Output](5\)i.png)
![Output](5\)ii.png)
![Output](5\)iii.png)
![Output](5\)iv.png)



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
