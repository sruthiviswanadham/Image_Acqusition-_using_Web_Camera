# Image_Acqusition-_using_Web_Camera

## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.


## Program:

### Developed By: Viswanadham Venkata Sai Sruthi
### Register No: 212223100061

## i) Write the frame as JPG file

```
import cv2
cap=cv2.VideoCapture(0)
frame_number=0

while frame_number<5:
    ret,frame=cap.read()
    cv2.imshow('frame',frame)
    cv2.imwrite(f"frame_(frame_number).jpg",frame)
    frame_number+=1
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()

```


## ii) Display the video

```
videoCaptureObject = cv2.VideoCapture(0)
while True:
    ret, frame = videoCaptureObject.read()
    cv2.imshow('myimage', frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()  
```


## iii) Display the video by resizing the window

```

import cv2
cap=cv2.VideoCapture(0)
cv2.namedWindow('Video',cv2.WINDOW_NORMAL)
while True:
    ret,frame=cap.read()
    cv2.imshow('Video',frame)
    cv2.resizeWindow('Video',100,200)
    if cv2.waitKey(1) & 0xFF ==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()        

```


## iv) Rotate and display the video

```

cap=cv2.VideoCapture(0)
rotation_angel=90

while True:
    ret,frame=cap.read()
    rotated_frame=cv2.rotate(frame,cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video',rotated_frame)
    if cv2.waitKey(1)&0xFF==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()  
```

## Output

### i) Write the frame as JPG image

![image](https://github.com/user-attachments/assets/4ed7be48-1799-4bef-b31d-6984c495e723)

### ii) Display the video

![Screenshot 2024-10-20 222524](https://github.com/user-attachments/assets/a14b8d8e-2a72-44fc-a95d-e4fdb6e581a3)

### iii) Display the video by resizing the window

![image](https://github.com/user-attachments/assets/64d10f12-5af6-4247-b11a-887a6615e808)



### iv) Rotate and display the video

![image](https://github.com/user-attachments/assets/63b308f0-8e16-4447-9ecf-cb7174833b4c)


## Result:
Thus the image is accessed from webcamera and displayed using openCV.


