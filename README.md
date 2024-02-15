# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By:Samyuktha S
### Register Number: 212222240089

### OUTPUT:
### i) Read and display the image
```Python
import cv2
image = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
resized_image = cv2.resize(image, (200, 300))
cv2.imshow('Samyuktha', resized_image)    
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![m2](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/d0ad2299-e7db-4035-8a13-d892f6958cd4)

 
  </td>
  </tr>

   <tr>
    <td width=50%>


### ii)Write the image
```Python
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
cv2.imwrite('demos.jpg',image)
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/949dbcdb-cd81-43ef-8ca1-0aa577b16c71)


 
  </td>
  </tr>

   <tr>
    <td width=50%>
      
### iii)Shape of the Image
```Python
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
print(image.shape)
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/54cc4372-c072-4e0c-a9d4-ccb499ea7693)

 
  </td>
  </tr>

   <tr>
    <td width=50%>


### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
    image=cv2.resize(image,(500,500))
    for i in range (250,500):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-15 200736](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/e4f64c1e-e880-4eba-bab6-7e9cb8728bb1)


 
  </td>
  </tr>

   <tr>
    <td width=50%>


### v)Cut and paste portion of image
```Python
import cv2
image=cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
image=cv2.resize(image,(300,300))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('image1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-15 200845](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/5eb20924-6248-489f-b639-16879a2ed113)


 
  </td>
  </tr>

   <tr>
    <td width=50%>



### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
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
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/f9711f69-c885-455e-be75-36063b0ede96)


 
  </td>
  </tr>

   <tr>
    <td width=50%>
      
### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/0afae64d-45ff-48b1-8a52-238910e6228b)


 
  </td>
  </tr>

   <tr>
    <td width=50%>


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/e1a7dedb-141b-4523-a0e5-c3e183fa7bdd)


 
  </td>
  </tr>

   <tr>
    <td width=50%>


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))

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
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/22a7da41-3902-4679-8e52-97388f2c3b9a)


 
  </td>
  </tr>

   <tr>
    <td width=50%>

### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread(r'C:\Users\SEC\Pictures\Screenshots\nat.jpg')
img = cv2.resize(img,(200,200))
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
  </td>
  <td>

### OUTPUT:
![image](https://github.com/SamyukthaSreenivasan/COLOR_CONVERSIONS_OF-IMAGE/assets/119475703/19c5d0ae-05de-4394-88ff-c6a07435778f)


 
  </td>
  </tr>

   <tr>
    <td width=50%>




## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







