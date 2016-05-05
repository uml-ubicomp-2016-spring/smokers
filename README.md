 **smokers**
 
smoking behavior detection on android wearable devices
team members: Han Geng,Ye Tian,Tingna Xie
[![IMAGE ALT TEXT](http://img.youtube.com/vi/YOUTUBE_VIDEO_ID_HERE/0.jpg)](http://www.youtube.com/watch?v=YOUTUBE_VIDEO_ID_HERE "Video Title")

week 1: 27th march 
we achieved detection of smoking gestures using accelerometer and orietation sensor in android watch ,the basic idea is that when users are trying to smoke ,they must conduct several drags ,hence the watch will be kept in a specific position.so values of "pitch" and "roll" will stay in a specific range for a short period ,then we can predict smoking gestures based on values of pitch and roll.

week 2:4th Apirl
we succeccfully retrieved data from microphone,we also got the frequecy spectrum of soundwaves in realtime.but we've got some problems with how to analyse the frequecy spectrum and match it with positive samples,because the frequency spectrum of clicking a lighter is kind of unstable ,we need to implement some signal processing algorithms to solve this problem.
