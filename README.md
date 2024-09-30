# Record-Image Acquisition using Web Camera
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
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'
<br>

## Program:

### Developed By:SRINIDHI SENTHIL
### Register No:212222230148

## i) Write the frame as JPG file
```
import cv2

cap = cv2.VideoCapture(0) frame_number = 0 # Initialize frame number

while frame_number < 5:

ret, frame = cap.read()

cv2.imshow('frame', frame)

# Save frame as JPG file cv2.imwrite(f"frame_{frame_number}.jpg", frame) frame_number += 1

if cv2.waitKey(1) & 0xFF == ord('q'):

break

cap.release()

cv2.destroyAllWindows()         
```




## ii) Display the video
```
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('RESULT',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```




## iii) Display the video by resizing the window
```
import cv2
cap = cv2.VideoCapture(0)
# Create a resizable window
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
ret, frame = cap.read()
cv2.imshow('Video', frame)
# Resize the window
cv2.resizeWindow('Video', 10, 200)
if cv2.waitKey(1) & 0xFF == ord('q'):
break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```
import cv2
cap = cv2.VideoCapture (0) # Define the rotation angle (in degrees)
rotation_angle = 90

while True:
    ret, frame = cap.read()
# Rotate the frame
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    cv2.imshow('Rotated Video', rotated_frame)
    if cv2.waitKey(1) & 0xFF == ord('q'):
        break
cap.release()
cv2.destroyAllWindows()



```
## Output

### i) Write the frame as JPG image
![WhatsApp Image 2024-09-30 at 08 46 50_7d3b119a](https://github.com/user-attachments/assets/d1234d4c-3e71-4179-982a-00b363d3a522)

</br>
</br>


### ii) Display the video
![WhatsApp Image 2024-09-30 at 08 47 48_2bba23f3](https://github.com/user-attachments/assets/a7a6b2b2-1745-4a6c-887e-83318c373b40)

</br>
</br>


### iii) Display the video by resizing the window

![WhatsApp Image 2024-09-30 at 09 09 41_d6caeb02](https://github.com/user-attachments/assets/550bddaf-8a1d-427c-9c34-68a3dabe29d7)

</br>
</br>



### iv) Rotate and display the video
![WhatsApp Image 2024-09-30 at 09 10 49_06cdde9b](https://github.com/user-attachments/assets/766e7e0b-121f-41c5-bf79-f6fffb5c1162)


</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
