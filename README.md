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
#### draw line top-left to bottom-right
```
import cv2
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
res = cv2.line(img, (0, 0), (399, 399), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/0955ee4d-ecb0-4d39-9d62-1dfe33816817)
#### draw a circle at the center of the image
```
import cv2
# Create a blank white image of size 400x400
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
center = (200, 200)  # (width // 2, height // 2)
radius = 100
color = (255, 0, 0)
thickness = 2
cv2.circle(img, center, radius, color, thickness)
cv2.imshow('Image with Circle', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/4aa79dae-3ad8-458f-9035-0704e94556b2)

#### draw a rectangle
```
import cv2
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
top_left = (50, 50)  # (x, y) coordinates for the top-left corner
bottom_right = (350, 350)  # (x, y) coordinates for the bottom-right corner
color = (0, 255, 0)
thickness = 3
cv2.rectangle(img, top_left, bottom_right, color, thickness)
cv2.imshow('Image with Rectangle', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/213d0a3e-015d-4cb8-bba2-a3eb8163a90d)

#### write "OpenCV Drawing" on top-left
```
import cv2
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
text = "OpenCV Drawing"
text_position = (10, 30)  # (x, y) coordinates for the text position
font = cv2.FONT_HERSHEY_SIMPLEX  # Font type
font_scale = 1  # Font scale factor
font_color = (255, 0, 0)  # BGR format, e.g., blue
font_thickness = 2  # Thickness of the text
cv2.putText(img, text, text_position, font, font_scale, font_color, font_thickness)
cv2.imshow('Image with Rectangle and Text', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/e78fa738-7b37-4a62-9461-7e205f383c25)

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
#### access and print the value of pixel at (100,100)
```
import cv2
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
x, y = 100, 100
pixel_value = img[y, x]  # Note that OpenCV uses (row, column) indexing
print(f"Pixel value at (100, 100): {pixel_value}")
cv2.imshow('Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/91159ce2-db61-4bda-ac8c-a485265c4456)

#### modify colour of pixel at (200,200) to white.
```
import cv2
img = cv2.imread("coke.jpg")
img = cv2.resize(img, (400, 400))
x, y = 200, 200
new_color = (255, 255, 255)  # White
img[y, x] = new_color
cv2.imwrite('modified_image.jpg', img)
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/2c01a5f8-de52-42fb-a379-1471db4b1784)


### v)Image Resizing
### resize image to half of its size
```
import cv2
img = cv2.imread("coke.jpg")
if img is None:
    print("Error: Image not found.")
else:
    img_resized_to_400 = cv2.resize(img, (400, 400))
    img_resized_to_half = cv2.resize(img_resized_to_400, (200, 200))
    cv2.imshow('Final Resized Image', img_resized_to_half)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/f01b732d-23c6-4446-8d0f-9b3579795e9d)

### vi)Image Cropping
```
import cv2
img = cv2.imread("coke.jpg")
if img is None:
    print("Error: Image not found.")
else:
    img_resized = cv2.resize(img, (400, 400))
    top_left_x, top_left_y = 50, 50
    crop_width, crop_height = 100, 100
    if (top_left_x + crop_width <= 400) and (top_left_y + crop_height <= 400):
        cropped_img = img_resized[top_left_y:top_left_y + crop_height, top_left_x:top_left_x + crop_width]
        cv2.imshow('Cropped Image', cropped_img)
        cv2.waitKey(0)
        cv2.destroyAllWindows()
    else:
        print("Error: Cropping region is out of bounds.")
```
![image](https://github.com/user-attachments/assets/952d0e2b-2926-4a77-9cf1-4b396cac057f)

### vii)Image Flipping

#### horizontal
```
import cv2
img = cv2.imread("coke.jpg")
if img is None:
    print("Error: Image not found.")
else:
    img_resized = cv2.resize(img, (400, 400))
    img_flipped_horizontal = cv2.flip(img_resized, 1)
    cv2.imshow('Flipped Image Horizontally', img_flipped_horizontal)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/b91402d1-96a2-493e-ae92-60d11e8dde93)

#### vertical
```
import cv2
img = cv2.imread("coke.jpg")

if img is None:
    print("Error: Image not found.")
else:
    img_resized = cv2.resize(img, (400, 400))
    img_flipped_vertical = cv2.flip(img_resized, 0)
    cv2.imshow('Flipped Image Vertically', img_flipped_vertical)
    cv2.waitKey(0)
    cv2.destroyAllWindows()

```
![image](https://github.com/user-attachments/assets/e9bbc6e8-c691-490f-a8f2-22dab81baea4)


### viii)Write and Save the Modified Image
```
import cv2

# Load the original image
img = cv2.imread("coke.jpg")

# Check if the image was loaded successfully
if img is None:
    print("Error: Image not found.")
else:
    # Resize the image to 400x400
    img_resized = cv2.resize(img, (400, 400))

    # Save the resized image to a file
    output_file = "resized_coke.jpg"
    cv2.imwrite(output_file, img_resized)

    print(f"Resized image saved to {output_file}")
```
![image](https://github.com/user-attachments/assets/d407b24a-47fe-423c-96b8-cb555aa42f19)







## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







