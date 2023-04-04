# Project Title : Parameter setting and reliability test of a sensor system for person detection in a car wearing summer wear
-----------------------------------------------------------------------------------------------------------------------------
This project study is carried out under the course of **Machine Learning** in Master of Engineering in Information Technology at Frankfurt University of Applied Sciences, Germany. The experiment is performed in the Winter Semester 2022/23.

# Introduction : 

This project aims to optimize a Machine Learning model to accurately detect humans wearing summer clothing in the seat of a car using data from an ultrasonic sensor. The reliability of the sensor system is investigated and adjusted to ensure accurate detection. Confusion matrixes are used to evaluate performance. The project also compares additional measurements to the raw signal report. The experimental results will improve the accuracy of the ultrasonic sensor system and inform future research in the field of analyzing visual imagery with Machine Learning techniques.

**Project Description**
========================

The key motivation of this project is to determine the optimal settings for a sensor system that used for detecting people in a car who are wearing summer clothing. The work deals with investigating the reliability of the sensor system and ensure that it can accurately detect the presence of a person in a car, even when they are dressed in lightweight summer clothing that may be less visible or less easily detectable than heavier clothing. [2] Task accomplishment may involve testing and analyzing the data-generated from the ultrasonic sensor pointed at the car seat. Examine the reliability of the sensor system and test the accuracy through confusion matrixes that easily can differentiate among varying humans, empty seats and even a dummy doll. Then, develop and implement a suitable software program to systematically analyze reflected ultrasonic waves based on the profile of the objects. As a further scope, several additional measurements to compared to the report from the raw signals.

Overall, the experimental results of the project will help improving effectiveness and accuracy of the ultrasonic sensor, for detection of the clothes and classify which most applied ML techniques in analyzing visual imagery nowadays.


**Project Objectives**
========================

For this project the following objectives are accomplished:

-	 Collect measurement data wearing summer cloths (data set of at least 1000 events of getting into the car). Store both ADC data, FFT data, and feature values.

-	 Record the experimental setup including all environmental conditions and photos of the clothing.

-	 At least 10 different persons with varying outfits and sizes. Record the size of the persons involved for each measurement. Take photos of the clothing used.

-  Analyze systematically results, data, and FFTs,ADC for false predictions, true positive, false nagative based on research scientific papers on ultrasonic physics.

-	 Evaluation of data set by Creating confusion matrix of the classification results.

-	 Research on and implementation of improvements such as: distance measure, feature extraction, outfit detection, classifier training accuracy etc.

-   Develop and implement required programming code or software for feature extraction and classification for analysis of the recorded data sets on a PC or Laptop.


**Implementation**
==================

1.Experimental Setup:
--------------------------------
A.	SRF02 Ultrasonic Sensor with Red Pitaya
The setup used the SRF02 Ultrasonic Sensor, which is a single transducer ultrasonic rangefinder on a small PCB uses for both transmission and reception. Here single transducer resulting a higher minimum range than other dual transducer rangers. The minimum measurement range is around 15cm, and it can function with a 5V grounded power supply. Sample picture shown below.

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/74227867/229152556-8a63117c-9546-4423-a55e-53e52e278c9c.png">
</p>


B.	UDP Client Software
The UDP_Client program is a vital tool in acquiring data from the Red Pitaya in this project. The program was developed by Daniel Schäfer from the Frankfurt University of Applied Sciences, and it boasts a user-friendly Graphical User Interface (GUI) as shown in Fig. 2. Through the use of this program, the team is able to efficiently gather data from the Red Pitaya, which is crucial for the success of the project. Sample Picture Shown Below.

<p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/74227867/229152785-e6728c95-6209-439c-9221-49b3015abd46.png">
</p>
![image](https://user-images.githubusercontent.com/74227867/229152785-e6728c95-6209-439c-9221-49b3015abd46.png)

C.	Measurement System
The car was a white Ford Fiesta v16 for data collection as shown in the Fig. 3 below. The focus of the measurement was from the side seat shown in Fig. 4 to the driving seat, and an ultrasonic sensor was attached to the car console using a Red Pitaya device. The sensor was mounted at a distance of 72 cm from the center of the console and 29.5 cm from the car floor, with an angle of 22 degrees from the reference line. The car's side seat was adjustable. Sample Picture of the car shown below

![image](https://user-images.githubusercontent.com/74227867/229152982-adbaf259-fb8e-4387-980c-95552fa576a8.png)

D.	Data Validation
Below Figure shows three persons image which we took before entering inside the car for data collection.
![image](https://user-images.githubusercontent.com/74227867/229153313-f2cab58f-546a-41fd-a786-183efc5c0452.png)  

E.	Random Forest Classifier
Random Forest Classifier is a popular machine learning algorithm used for building classification models, shown in Figure below. It is an ensemble learning method that constructs a multitude of decision trees at training time and outputs the class that is the mode of the classes (classification) or mean prediction (regression) of the individual trees.

![image](https://user-images.githubusercontent.com/74227867/229153547-10233b19-6f05-4682-a0dd-7e3d863758fe.png)

Workflow of the Random Forest Classifier is given below
![image](https://user-images.githubusercontent.com/74227867/229153609-a0cd22fa-960c-4dc8-99b2-0d249eb24190.png)


**Results**
==============

A.	Confusion Matrix Without Classifier Training
![image](https://user-images.githubusercontent.com/74227867/229154075-4eba4984-b66b-4932-ba21-ca2dcf1be0ab.png)

B.	FFT data Confusion Matrix of Classifier Training with 10,000 data
![image](https://user-images.githubusercontent.com/74227867/229154435-ebbcdf8a-0915-4510-b43f-fae6aaf610a1.png)

C.  FFT data Confusion Matrix of Classifier Training with 30,000 data
![image](https://user-images.githubusercontent.com/74227867/229154563-5b4089b1-7d2c-4ea7-8091-e215c90f5164.png)

D.  FFT data Confusion Matrix of for a Single Person Data of 1000
![image](https://user-images.githubusercontent.com/74227867/229154683-fbe06e14-be81-4d22-b8e2-580d20f58439.png)

E.  FFT data Confusion Matrix of for an Empty Seat
![image](https://user-images.githubusercontent.com/74227867/229154844-43eae168-4b1c-4d7a-a448-c3601944c765.png)

E.  FFT data Confusion Matrix of for a Dummy Doll
![image](https://user-images.githubusercontent.com/74227867/229155069-d3d52d76-f721-4e39-b6d4-013fa99d12e1.png)

E.  ADC data Confusion Matrix of 10,000 data
![image](https://user-images.githubusercontent.com/74227867/229155183-d301f8e0-93c7-4a7a-9524-403b617ed4de.png)

**Conclusion**
==============

In conclusion, this project has demonstrated the potential of machine learning for classifying humans in a car seat using ultrasonic data. Our findings suggest that there are still challenges to be addressed, but by continuing to explore and refine our models, we can make significant advances in this area. We hope that our work can contribute to the development of more robust and effective classification techniques for applications such as automotive safety and security.


**Contributor**
===============
1. Jiban Kumar  Ray, MEng. in Information Technology, Frankfurt University of Applied Sciences
2. Md Mijanur Rahaman, MEng. in Information Technology, Frankfurt University of Applied Sciences
3. Debasish Dutta, MEng. in Information Technology, Frankfurt University of Applied Sciences
