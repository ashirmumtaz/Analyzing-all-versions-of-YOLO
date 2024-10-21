# Analyzing-all-versions-of-YOLO
**Overview**
YOLOv5-v10 Comparison  Benchmarking YOLOv5 to YOLOv10 on a unified dataset. Analyze performance metrics, architectural differences, and identify optimization opportunities across YOLO versions.

**Data Set:**
Downloaded the data set from Roboflow
@misc{
mri-rskcu_dataset,
title = { MRI Dataset },
type = { Open Source Dataset },
author = { Brain MRI },
howpublished = { \url{ https://universe.roboflow.com/brain-mri/mri-rskcu } },
url = { https://universe.roboflow.com/brain-mri/mri-rskcu },
journal = { Roboflow Universe },
publisher = { Roboflow },
year = { 2023 },
month = { jun },
note = { visited on 2024-07-17 },
}
Classes: Contain 2 classes 
•	Eye
•	Tumor




**YOLO V6:**
Clone pretrained repository of Yolov6 from https://github.com/meituan/YOLOv6
Train on custom data with
•	Batch = 32
•	Epochs = 100
•	Img-size = 416
•	Optimizer = SGD
Time Taken 35-40 minutes
**Results of training:**
 



![image](https://github.com/user-attachments/assets/f94882fe-9650-48f9-8e0c-02dc8f978f5f)




**Results of Validation:**
 ![image](https://github.com/user-attachments/assets/f9aeb733-f8fb-4e92-8a49-58de9501aa89)


**Conclusion of Yolov6s Base Model:**
YoloV6 perform worst on grayscale Dataset. Not even able to predict the grayscale data.

**YOLO V7:**
Clone pretrained repository of Yolov6 from
https://github.com/WongKinYiu/yolov7
Train on custom data with
•	Batch = 16
•	Epochs = 55
•	Img-size = 640
•	Optimizer =adam
Time Taken 55-60 minutes



**Results**
 ![image](https://github.com/user-attachments/assets/47f8b066-2de4-45ab-8bf1-200b940dd4cf)

**Detection**


![image](https://github.com/user-attachments/assets/d12d52e2-94b0-4afd-bcef-57929472e73a)












**Conclusion:**
Need high computing power as the number of epochs increases from 55
Or batch size increase from 16

**YOLO V8:**
Clone pretrained repository of Yolov8 from https://github.com/ultralytics /ultralytics
And installed the yolo v8 from this official repository 
Train on custom data with
•	Batch = 16
•	Epochs = 25
•	Img-size = 800
•	Optimizer = ADAM-W
Time Taken 10-15 minutes








**Results**
Confusion matrix
 

![image](https://github.com/user-attachments/assets/571b0a30-a34d-4c1e-a0d9-83b0f1a23799)







**Graphs**


  

![image](https://github.com/user-attachments/assets/25c66f30-ce0a-4ba8-8643-ceb29538e94b)






**Detection**

 ![image](https://github.com/user-attachments/assets/bda5a6b0-5bb8-44e9-a7ef-8b02a39ea584)


**Conclusion**
Till now v8 performed best on this dataset with overall mAP of 0.904 


**YOLO V10:**
Clone pretrained repository of Yolov10 from 
https://github.com/tHU-MIG/yolov10.git
Train on custom data with
•	Batch = 32
•	Epochs = 10
•	Img-size = 640
•	Optimizer = adam-w
•	Time Taken 10-15 minutes

**Results** 
Confusion matrix
 ![image](https://github.com/user-attachments/assets/eee23a82-2cdf-43e6-9f91-3937886bf5db)

**Graphs** 



![image](https://github.com/user-attachments/assets/9352d0b2-bfe3-4c4f-969f-11e2fda6e1af)









**Detection**
 
![image](https://github.com/user-attachments/assets/8d45b59a-49b5-4f74-8056-87cfc169a8bb)

**Conclusion** 
The base model with 10 epochs did not perform well than v8 and v9 To increase its performance epochs should be increased
