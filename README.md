# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By:
### Register Number: 


## Output:

### i)Read and Display an Image

```
import cv2
image=cv2.imread('coke.jpg',1)
image=cv2.resize(image,(400,400))
cv2.imshow('coke',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/a68cbee7-2e78-4036-9e4a-c019084ae832)


### ii)Draw Shapes and Add Text

<br>
<br>

### iii)Image Color Conversion
```
import cv2
img = cv2.imread('coke.jpg',1)
img = cv2.resize(img,(300,300))
cv2.imshow('Original Image',img)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![image](https://github.com/user-attachments/assets/473ae2a0-a910-42f6-b649-72e9319a3f53)
![image](https://github.com/user-attachments/assets/e9c5aad1-bf03-4091-8f0c-d61a313f8f0b)
![image](https://github.com/user-attachments/assets/6c3a5bb1-1058-4a3d-84b9-b2e994887032)

```
import cv2
img = cv2.imread('coke.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/d8155ddb-8d1c-47d9-b1df-e59f3fffebc6)

```
import cv2
img = cv2.imread('coke.jpg')
img = cv2.resize(img,(300,300))

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/739877b7-ca13-4fea-bca9-f405a18181c6)

### iv)Access and Manipulate Image Pixels
<br>
<br>

### v)Image Resizing
<br>
<br>

### vi)Image Cropping
<br>
<br>

### vii)Image Flipping
<br>
<br>

### viii)Write and Save the Modified Image
<br>
<br>






## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







