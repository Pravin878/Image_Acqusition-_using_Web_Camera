# Ex-2-Image Acqusition using Web Camera
## Aim
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera

### Step 2:
Use cv2.imread to read the video or image

### Step 3:
Use cv2.imwrite to save the image

### Step 4:
Use cv2.imshow to show the video

### Step 5:
End the program and close the output video window by pressing 'q'.

## Program:
```
 Developed By: Pravin kumar G
 Register No: 212222230109
```
## i) Write the frame as JPG file
```python
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("Archana.jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```


## ii) Display the video

```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('flower',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## iii) Display the video by resizing the window
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240011_Archana',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```python
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222240011_Archana',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```







## Output

### i) Write the frame as JPG image
![WhatsApp Image 2024-11-13 at 15 49 45_6996c664](https://github.com/user-attachments/assets/b53abe92-c1ad-4792-b768-fab2ff9f90cb)

### ii) Display the video
![WhatsApp Image 2024-11-13 at 15 49 45_6996c664](https://github.com/user-attachments/assets/1ab1e2df-c84c-496e-8fdd-ab2c2fb7aec4)




### iii) Display the video by resizing the window

![WhatsApp Image 2024-11-13 at 15 49 45_c283da78](https://github.com/user-attachments/assets/b962989e-4369-420e-91e6-ddb88f0f921f)


### iv) Rotate and display the video


![WhatsApp Image 2024-11-13 at 15 49 46_37e6ee7a](https://github.com/user-attachments/assets/35a6d589-0706-4da8-bfc1-07f31f9a9acd)




## Result:
Thus the image is accessed from webcamera and displayed using openCV
