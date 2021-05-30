# HackonwithAmazon Team:Aquite
<div align="center">

  ![](https://www.mecco.com/Files/BlogItems/Spotting-Couterfeits.jpg)

</div>

---

<p align="center">We all agree that manufacturers have a right to ensure that fake goods are not marketed in their names and that their own goods are not marketed under fake names</p>

# Table of Contents
+ [About](#description)
+ [Getting Started](#getting_started)
+ [Training Weights](#Training_Weights)
+ [Deployment](#Deployment)
+ [Desired Output](#Desired_Output)
+ [Future Scope](#future_scope)
+ [Refrences](#Refrences)

## About <a name="description"></a>
+ In today’s world, how do you know if you are buying a genuine product?
+ We plan to implement a model which will enable the user to find if a product is original or counterfeit by just inputting the logo of the brand.

### Why YOLOv3? <a name="why_YOLOv3"></a>
+ YOLOv3 executed faster than both Faster R-CNN and SSD.
+ With YOLOv3 The results are also cleaner with little to no overlapping boxes.

## Getting Started <a name="getting_started"></a>
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.


## Prerequisites:

1) Python (preferably latest version)
2) Code Editor (Eg: Visual Studio/Pycharm)


### Installation
A step by step series of examples that tell you how to get a development env running

Either you can download the zip file or clone the repository using following link
```
$ git clone https://github.com/anjiii-18/HackOn_With_Amazon-Aquite.git
```

Install pip by using below command in terminal

Linux: 
```
 $ apt install python3-pip      #python 3
```

Install all the  requirements mentions in the requirements.txt file by running 

```
$ pip install -r requirements.txt
```


## Training Weights <a name="Training_Weights"></a>
- Create yolov3 and training folders in your google drive
- Mount drive, link your folder, and navigate to the yolov3 folder.
- Clone the Darknet git repository https://github.com/AlexeyAB/darknet
- Create & upload the following files for training to your drive-
1. obj.zip [zip of the training/validation images and their annotation files in yolo format]
2. yolov3.clg [contains the configuration of yolov3 model]
3. obj.name [contains the names of the class labels] 
4. obj.data [contains the number of classes and the locations of train, test, names and backup]
5. process.py [Create and/or truncate train.txt & test.txt and then populates them, also contains the percentage of images to be used for the test (validation) set, we have kept 10% dataset as our test set]
- Make changes in the Makefile to enable OPENCV and GPU.
- Run make command to build darknet.
- Copy the files “obj.zip”, “yolov3.cfg”, “obj.data”, “obj.names”, and “process.py” from the yolov3 folder to the darknet directory.
- Run the process.py python script to create the train.txt & test.txt files.
- Download the pre-trained YOLOv3 weights
- Train the detector
- Check performance (maP, precision, recall and F-score)

## Deployment <a name="Deployment"></a>
+ Name the weight file as "yolov3" and upload it in the cloned directory or you can download our trained weights file from the [link](https://drive.google.com/file/d/14mK1h9j5xYPodqTc823jFll3beAL3Rki/view?usp=sharing).

Note: "yolov3.weights" file must be present inside "HackOn_With_Amazon-Aquite" folder like: 

<div align="center">

  ![](https://github.com/anjiii-18/HackOn_With_Amazon-Aquite/blob/main/Result_Images/img5.jpeg)

</div>

You need to install opencv in your system which can be done using following command:

```
 $ pip3 install opencv-python
```

+ Now, run app.py file using following command in terminal

```
$ python3 app.py        #python3
```

Now you can upload any image of a Nike and Adidas product and check for its originality just in a click!  

## Desired Output <a name="Desired_Output"></a>
+ These are the desired output images which our model is detecting for a give input images.
<div align="center">

  ![](https://github.com/sakshi012000/HackOn_With_Amazon-Aquite/blob/main/Result_Images/img1.jpeg)

</div>
<div align="center">

  ![](https://github.com/anjiii-18/HackOn_With_Amazon-Aquite/blob/main/Result_Images/img2.jpeg)

</div>


That's how we can upload any brand logo and get the originality.



## Future Scope <a name="future_scope"></a>
+ This is highly important issue which needs technical solutions like these to tackle.
+ We can train our  model with a large dataset and high capacity GPU to expand it to various other brands and can defeat the counterfeit products in the market !!


## Refrences <a name="Refrences"></a>
+ https://github.com/AlexeyAB/darknet
+ https://cvat.org/
+ https://pjreddie.com/darknet/
