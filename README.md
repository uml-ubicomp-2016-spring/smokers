 **smokers**
 
smoking behavior detection on android wearable devices

team members: Han Geng,Ye Tian,Tingna Xie

here are two videos which show what we have achived

[![IMAGE ALT TEXT](http://img.youtube.com/vi/0YwCEhQb5EQ/0.jpg)](http://www.youtube.com/watch?v=0YwCEhQb5EQ "Video Title")
[![IMAGE ALT TEXT](http://img.youtube.com/vi/tisqz-G4AOs/0.jpg)](http://www.youtube.com/watch?v=tisqz-G4AOs "Video Title")


**weekly report**

week 1: 27th march 

we achieved detection of smoking gestures using accelerometer and orietation sensor in android watch ,the basic idea is that when users are trying to smoke ,they must conduct several drags ,hence the watch will be kept in a specific position.so values of "pitch" and "roll" will stay in a specific range for a short period ,then we can predict smoking gestures based on values of pitch and roll.

week 2: 4th Apirl

we succeccfully retrieved data from microphone,we also got the frequecy spectrum of soundwaves in realtime.but we've got some problems with how to analyse the frequecy spectrum and match it with positive samples,because the frequency spectrum of clicking a lighter is kind of unstable ,we need to implement some signal processing algorithms to solve this problem.

week 3: 11th Apirl

we are trying to build an app to extract data from audio files,thus we can find a way to create dataset for svm training.

week 4: 18th Apirl

we have successfully retrieved data from audio files ,and we got enough dataset ,now we are trying to start svm training.

week 5: 25th Apirl

we finished svm training and got a good svm model.now we are trying to test the model in android device and integrate svm model with previously finished code.

week 6: 2nd May

we finished the whole coding part,and we recorded two videos to show the result,and we are prepared to do the demo.




