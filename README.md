# 40-VirtualRacing

![](https://github.com/connected-autonomous-mobility/40-VirtualRacing/blob/master/images/1774_115.png)

### 1 background

It all started at a parking lot...

A few guys meet there, discussed after a long meetup evening, came up with a crazy idea and made it happening. We met at Maker Faire Bay Area 2019 with more guys from [Oakland](http://diyrobocars.com), Ann Arbor, [Detroit](https://www.meetup.com/Detroit-Autonomous-Vehicle-Meetup/), [Ottawa](https://www.meetup.com/Ottawa-Autonomous-Vehicle-Group/), [Shenzehn](https://www.roboticsmasters.co/), [Stuttgart](https://www.meetup.com/Connected-Autonomous-Driving) and many more countries. 
Now we're calling us the ***Parking Lot Nerds*** and are heading towards our new venture: Virtual Autonomous Racing. 

Thanks a lot, Ed & Tawn (Oakland), Nic & Paul (Ottawa), Dave (Ann Arbor), Linda & Wallarug (Shenzhen) and especially Alex (Detroit) for literally driving the extra miles down to Stuttgart and making our journey to Silicon Valley / Maker Faire Bay Area 2019 a once in a life time experience.

### 2 preparation

- [Tawn's gist](https://gist.github.com/tawnkramer/6d244090cb8f2af1bc9f6d1ebc0377b1)
- [Ottawa, paulh](https://github.com/Ottawa-Autonomous-Vehicle-Group/Virtual-Hack-And-Race-Workshop)


### 3 [data](https://github.com/connected-autonomous-mobility/40-VirtualRacing/tree/master/data)


### 4 [models](https://github.com/connected-autonomous-mobility/40-VirtualRacing/tree/master/models)

models trained by others
- [naisy](https://drive.google.com/file/d/1CwBHI4Ms1wphSNg2xyUn7fdYAkepYQSU/view)

### 5 [Leaderboard](https://aleaderboard.com/w2/b24ffdaf-895c-422f-9aed-c51c4edc4579)

### 6 twitch.tv channels

- [DAVG](https://www.twitch.tv/doavg)
- [Oakland](https://www.twitch.tv/mossmann3333)
- [Stuttgart](https://www.twitch.tv/DIYrobocars_stuttgart)

### 7 Quick Start

## 7.1 Run your model
```
(donkey) rainer@neuron:~/mysim2$ python manage.py drive --model=models/lane_keeper.h5
```

## 7.2 In your browser goto
```
http://localhost:8887/drive
```
And set mode to ```local pilot```
