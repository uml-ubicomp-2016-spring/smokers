


italics = *italics*
bold  = **bold**
bold italics = ***bold italics***

**Detection of smoking behavior with android smart watch**
*Han Geng,Ye Tian,Yuting Xie*
*Ubiquitous computing ,Spring 2016,UMASS Lowell*

**Introduction**

Smoking is considered as a big reason of lung cancer,and it also causes a lot of other health problems.So an effective way of quitting smoking is necessary for most of people who are addicted to tobacco and try to stay away from it.But,as we know,human behavior is always hard to change especially when it is associated with addictive chemicals like nicotine.However we are not trying to make something that could physically help people quit smoking but rather a way to help people remember and aware of how much the tobacco has harmed their health.There are already lots of smoking detection approaches .In this report we will compare our approach with another project made by Artem Dementyev in MIT,in which they developed a self-designed wrist-worn device with dust sensor,and a G-sensor(temperature and accelerometer),they got pretty accurate result.In their report they also mentioned a previous study (study [1])in which the researchers used an wrist-worn device to analyze smoking behaviors with data from accelerometer,and they got an accuracy of about 70%.Our study was inspired by their work, we implemented an audio-signal based algorithm and integrated it with accelerometer to achieve our goal.

**Methods**

*Subjects and measurements*
Due to the limited finance and time,we only test this on our team members:Ye Tian and me.we have tested this in both experimental situation and outside environment.

**Device**

Android smart phone with  SDK-19 android system.
![GitHub Logo](https://github.com/uml-ubicomp-2016-spring/smokers/blob/master/graph1.png?raw=true)

**Features**

We decided to use two important features to analyze the smoking behaviors

(1)Sound of clicking a lighter,we all know one must light a cigarette before smoking . Most people would prefer to use a lighter to do this ,few people may still prefer matches or other fire source for specific reasons,since it’s just minority we only consider the lighter clicks in our study

(2)Smoking gestures,we used accelerometer to detect smoking gestures,same idea as previously mentioned studies,and did a lot of trial to get experimental data for the algorithm.

**Technical Approach**

For the audio signal analyze ,we used SVM model,which is a very popular machine learning model in classification analyze,and we extracted totally 18 features of each audio signal frame.we recorded hundreds of lighter clicks of both Ye Tian and me as positive samples ,and we recorded a randomly environmental audio track to generate negative samples.
For the SVM model we used Gaussian kernel,which is also referred to as RBF.In most cases RBF works the best,and in our case it’s absolutely the right choice.
Here is a graph of experimental testing-result of the SVM model.



![GitHub Logo](https://github.com/uml-ubicomp-2016-spring/smokers/blob/master/watch.JPG?raw=true)

In this graph x axis shows the number of positive clicks used for training(one positive sample may generate 1-3 positive frames),y axis shows the result of test on 217 positive samples,all positive samples come from my clicks ,the number of negative samples are always 2870.The test is finished in experimental environment.
One problem with our approach is that we found out ,different persons click a lighter in different ways(different in strength and speed).So we have also made a test on positive samples created by different subjects.






Here is a table which shows the result:

![GitHub Logo](https://raw.githubusercontent.com/uml-ubicomp-2016-spring/smokers/ebb9aecf53d2cce168fdeeeb0bd7767b7ce3dabb/table.PNG?raw=true)

We can see from the table,when we used my 50 samples (one sample could generate 1-3 frames,so the total number of data set could be 50-150)to train and use Ye Tian’s samples to test,the accuracy will be dramatically reduced,but when we mixed all samples together we can pull the accuracy to a receivable line.that means if we can get enough positive data set,our SVM model could cover most real-world cases.
We have also tested our model in real-world environment,we found out that if noise is extremely large ,there would be no way to analyze the audio signal.And if the noise is slight ,it would reduce the accuracy of detection.
And in the link below is video demo of this part:


**Topology graph**
![GitHub Logo](https://github.com/uml-ubicomp-2016-spring/smokers/blob/master/topo.PNG?raw=true)

and here is another demo to show a completed successful detection:
https://youtu.be/tisqz-G4AOs

**Result and comparison**
We have only two members who could smoke in our team ,so we could not collect a large testing data .We did 20 times of tests on each of us ,and the overall accuracy is 80%.Which is lower than the result in the study of Artem Dementyev ,but higher than in study[1].But our work hasn’t finished yet,we still have a large space for improvement on our algorithm.

When compared with Artem Dementyev’s study,our disadvantages are:
(1)less accurate than their approach
(2)If the environment is noisy ,our project’s performance will be worse.

The advantages are:
(1)our device is well commercialized ,their device is too specific,so their study could barely lead to a product.
(2)In our project we explored the implementation of audio analyze on wearable device,thus we could integrate more projects to achieve more valuable goals,their implementation could barely barely extend to other filed .



**Bibliography**

*[1] Scholl, Philipp M., and Kristof Van Laerhoven. "A Feasibility Study of Wrist-Worn Accelerometer Based Detection of Smoking Habits." Innovative Mobile and Internet Services in Ubiquitous Computing (IMIS), 2012 Sixth International Conference on. IEEE, 2012.*

*[2] Artem Dementyev .,"Detection and analysis of smoking events with wrist-worn sensors " Affective Computing, Fall 2013, MIT.*
