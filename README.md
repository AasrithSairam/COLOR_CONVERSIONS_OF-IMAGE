# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.
## Algorithm:
### Developed By: Ponguru Aasrith Sairam
### Register Number: 212223240116
### Program:

### i) Read and display the image

```
import cv2
image=cv2.imread('coke.jpg',1)
image=cv2.resize(image,(400,400))
cv2.imshow('coke',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
![image](https://github.com/user-attachments/assets/48b324ff-2d4a-4fc8-85e2-4699c2b73c22)



### ii)Write the image
```
    image=cv2.imread('coke.jpg',0)
    cv2.imwrite('copy2.jpeg',image)
```
## Output:
![image](https://github.com/user-attachments/assets/f778bd1a-11ea-498a-b2ac-495a535a250a)



### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('coke.jpg',1)
    print(image.shape)
```
## Output:
![image](https://github.com/user-attachments/assets/b8ac80e9-c9ca-4116-a277-b2da2b0927d0)


### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('coke.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('coke part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/9da91a3b-4667-4cbc-9f0c-9d3c4beb6f20)



### v)Cut and paste portion of image
```
  import cv2
  image=cv2.imread('pic.jpg',1)
  image=cv2.resize(image,(400,400))
  tag =image[130:200,110:190]
  image[110:180,120:200] = tag
  cv2.imshow('cut and paste',image)
  cv2.waitKey(0)
  cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/57100059-7ec2-4fa8-b9ad-374c2670767e)



### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('pic.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![image](https://github.com/user-attachments/assets/6ea548c2-cf2d-4857-91bd-4de84cf0c875) ![image](https://github.com/user-attachments/assets/f5919a2f-d3c9-4560-88aa-9972d3df77ce) ![image](https://github.com/user-attachments/assets/2b7266a0-95ef-4e7d-be3e-bc9e654cbad4) ![image](https://github.com/user-attachments/assets/c2399fd6-4da6-4d7b-a8a5-e820340a7605) ![image](https://github.com/user-attachments/assets/d1195a7d-ec92-4c98-a020-df406c4932bc)








### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('pic.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:



### viii) RGB and BGR to YCrCb
```
import cv2
img = cv2.imread('pic.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:




### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('pic.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:




### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("pic.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:





## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







