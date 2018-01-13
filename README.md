# Environment Tester
-	An Android Application used to test if the current environment is good for sleep as long as you put your phone on the desk
-	Designed and developed the frontend with xml and backend with java and python
-	Implemented audio features and trained the audio data with Decision Tree Classifier, SVM Classifier and Random Forest     Classifier
-	Implemented light metric (LUX) into backend

Desgined by Junqi Zhang, Yudong Diao, Chao Li
Background
	Due to the fact that most college students don’t have sufficient time for sleep, thus, sleeping quality is very important to us. Our final project’s basic idea is to determine an environment is good for sleep or not.

Introduction
In this project what we mainly did is changing the UI and adding a parameter, LUX(unit for light), to test whether the environment is good for sleeping. There are four results, very good, good, bad, very bad.

#APP UI
![alt text](https://github.com/yudongdiao/Final/blob/master/Picture1.png?raw=true)
![alt text](https://github.com/yudongdiao/Final/blob/master/Picture2.png?raw=true)


#Data Collections:
	Audio:
-	We collected data at Noisy environment such as, live show, gym, dorm with loud music playing
-	Fair environment: classroom with professor talking, group study room at Du Bois library
-	Quiet(Good): dorm with no music playing, quiet study floor.

#Light:
-	Because measurement of light is just one scalar, we don’t need to collect light data. All we need to do is to consider under what LUX value is Bad, Fair and Good for sleeping. 

#Algorithm criteria:
result=audio factor*300+LUX data
Audio factor
Range: 0~3
Lux: 0~20000
If(result < 800) {very good}
If(result between 800 and 1600){good}
If(result between 1600 and 2400){bad}
Else very bad

#Implementation for LUX data:
We added a light sensor. Once the data of sensor changed, we send  the lux data from MainActivity.java to Constant and then receive it using audiofragment.java.

