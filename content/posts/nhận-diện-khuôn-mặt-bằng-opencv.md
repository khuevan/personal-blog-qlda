---
path: https://www.youtube.com/watch?v=pdIZWcdnCqQ
date: 2021-01-02T08:05:01.328Z
title: Nhận diện khuôn mặt bằng OpenCV
description: Hướng dẫn code Python nhận diện khuôn mặt
---
![](./facial.jpg)

```js
while(True):
    ret, frame = cap.read() # frame: data camera
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY) # convert to gray pricture
    
    # ket hop face_cascade vs webcam de cho ra gia tri khuon mat
    faces = face_cascade.detectMultiScale(gray, 1.3 ,5) #image,scaleFactor,minNeighbor

    for(x,y ,w,h) in faces:
        # ve hinh vuong nhan dien khuon mat
        cv2.rectangle(frame, (x,y), (x + w,y + h),(0,255,0) ,2)

        directory = str(name)
        parent_dir = "dataSet"
        path = os.path.join(parent_dir, directory) 
        
        #if not os.path.exists(directory):
        os.makedirs(path, exist_ok = True) 
        
        #tang id
        sampleNum +=1
        
        #save the captured face in the dataset folder
        cv2.imwrite('dataSet/'+str(name)+'/'+str(id)+'-'+str(sampleNum)+'.jpg', gray[y:y+h,x:x+w])

    cv2.imshow('frame',frame)
    cv2.waitKey(1)
    # break if the sample number is morethan 20
    if sampleNum>100:
         cap.release()
         cv2.destroyAllWindows()
         break;

cap.release()
cv2.destroyAllWindows()
```

*Chúc các bạn thành công!!!*
