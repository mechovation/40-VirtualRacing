# Virtual Racing League - Public Version

## 1 Tawn Kramers training advice (~10.000 images)
"Here's a few tips on how to train a stable lane keeping driver.

Mix 4 different driving types in different proportions:

- 10% precision mainline driving (2 laps)
- 20% mainline with small oscillations (2-3 laps)
- 20% large slow oscillations establishing lane boundaries (2-3 laps)
- 50% normal driving, allowing deviation from center without over correction, allowing more speed (6-8 laps)
1, 2, & 3 can be done quite slowly until you are confident."

## 2 data fast

```
JOYSTICK_MAX_THROTTLE = 0.85
```

### 2.1 raw
```
/home/rainer/mysim2/data/tub_2_20-04-13
/home/rainer/mysim2/data/tub_3_20-04-13
/home/rainer/mysim2/data/tub_3_20-04-13
/home/rainer/mysim2/data/tub_5_20-04-13
/home/rainer/mysim2/data/tub_6_20-04-13
/home/rainer/mysim2/data/tub_7_20-04-13
/home/rainer/mysim2/data/tub_8_20-04-13
/home/rainer/mysim2/data/tub_9_20-04-13
/home/rainer/mysim2/data/tub_10_20-04-13
/home/rainer/mysim2/data/tub_11_20-04-13
/home/rainer/mysim2/data/tub_11_20-04-13
/home/rainer/mysim2/data/tub_12_20-04-13
/home/rainer/mysim2/data/tub_13_20-04-13
/home/rainer/mysim2/data/tub_14_20-04-13
collating 5325 records ...
train: 4016, val: 1005
total records: 5021
```
### 2.2. cleaned
```
/home/rainer/mysim2/data/tub_2_20-04-13
/home/rainer/mysim2/data/tub_3_20-04-13
/home/rainer/mysim2/data/tub_3_20-04-13
/home/rainer/mysim2/data/tub_5_20-04-13
/home/rainer/mysim2/data/tub_6_20-04-13
/home/rainer/mysim2/data/tub_7_20-04-13
/home/rainer/mysim2/data/tub_8_20-04-13
/home/rainer/mysim2/data/tub_9_20-04-13
/home/rainer/mysim2/data/tub_10_20-04-13
/home/rainer/mysim2/data/tub_11_20-04-13
/home/rainer/mysim2/data/tub_11_20-04-13
/home/rainer/mysim2/data/tub_12_20-04-13
/home/rainer/mysim2/data/tub_13_20-04-13
/home/rainer/mysim2/data/tub_14_20-04-13
collating 5008 records ...
train: 3804, val: 952
total records: 4756

```

## 2 data slow

```
JOYSTICK_MAX_THROTTLE = 0.3
```

```
/home/rainer/mysim2/data/tub_28_20-04-13 ---> slow line following 2.5 laps
/home/rainer/mysim2/data/tub_29_20-04-13 ---> oscillations, 2.5 laps
```

### 2.1 raw

### 2.5 data super fast, max = 1.0

tub 50

## 3 Training

### 3.1 parkinglotnerds1
```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13 --model ./models/parkinglotnerds1.h5
```

### 3.2 parkinglotnerds2 (using lane_keeper.h5 as a base)

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13 --model ./models/parkinglotnerds2.h5
```

### 3.3 parkinglotnerds3 (using lane_keeper.h5 as a base and cleaned data)

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13 --model ./models/parkinglotnerds3.h5
```

### 3.4 parkinglotnerds4 (using lane_keeper.h5 as a base and cleaned data + slow driving)

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13,/home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13 --model ./models/parkinglotnerds4.h5
```

### 3.5 parkinglotnerds5 (no base model, just cleaned data + slow driving)

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13,/home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13 --model ./models/parkinglotnerds5.h5
```

### 3.6 parkinglotnerds6 (AI-generated training data of parkinglotnerds5 model, 20,08s in training)

```
myconfig.py:

RECORD_DURING_AI = True 

/home/rainer/mysim2/data/tub_41_20-04-13

(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_41_20-04-13 --model ./models/parkinglotnerds6.h5
does not work because of CHANGED VALUES in JSON
```

#### classical record
```
{"cam/image_array": "335_cam-image_array_.jpg", "user/angle": -0.02099673451948607, "user/throttle": 0.75, "user/mode": "user", "milliseconds": 74086}
```

#### AI record
```
{"cam/image_array": "1722_cam-image_array_.jpg", "user/angle": 0.030396435438093204, "user/throttle": 0.0, "user/mode": "local", "pilot/angle": -0.003899402916431427, "pilot/throttle": 0.6323270797729492, "milliseconds": 395437}
```

#### read AI record
- [x] check reading routine: def collate_records(records, gen_records, opts): [code](https://github.com/autorope/donkeycar/blob/33d101bf786df306797288ed07a4603042413281/donkeycar/templates/train.py)
- [x] implement in new reading.py
- [x] identify generating gen_records, [create_sample_tub(tub_path, records=initial_records)](https://github.com/autorope/donkeycar/blob/99eec5908beca96128c3aad7e4b45172b8ccc598/donkeycar/tests/test_train.py), [definition](https://github.com/autorope/donkeycar/blob/1e65182ebb4d0ee98dc192f8fb440bcc118f1b9e/donkeycar/tests/setup.py)
- [x] check [tubwriter](https://github.com/autorope/donkeycar/blob/2ea51a38c31880fa87936669bbbba259c022b710/donkeycar/tests/test_tub.py)
- [x] do modification to read AI records
- [x] train
- [x] result: no an improvement in speed, see model 11


### 3.7 parkinglotnerds7 (no base model, just cleaned data + slow driving + new fast )

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_2_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_3_20-04-13,/home/rainer/mysim2/data/tub_5_20-04-13,/home/rainer/mysim2/data/tub_6_20-04-13,/home/rainer/mysim2/data/tub_7_20-04-13,/home/rainer/mysim2/data/tub_8_20-04-13,/home/rainer/mysim2/data/tub_9_20-04-13,/home/rainer/mysim2/data/tub_10_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_11_20-04-13,/home/rainer/mysim2/data/tub_12_20-04-13,/home/rainer/mysim2/data/tub_13_20-04-13,/home/rainer/mysim2/data/tub_14_20-04-13,/home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13,/home/rainer/mysim2/data/tub_50_20-04-14 --model ./models/parkinglotnerds7.h5
```


### 3.8 parkinglotnerds8 (no base model, just cleaned data + slow driving + new fast ) ***BEST***

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13,/home/rainer/mysim2/data/tub_50_20-04-14 --model ./models/parkinglotnerds8.h5

AI_THROTTLE_MULT = 1.15

(donkey_ottawa) rainer@neuron:~/mysim_ottawa$ python manage.py drive --model ./models/parkinglotnerds8.h5 --myconfig client0.py 

```
![](https://github.com/Heavy02011/50-donkey/blob/master/VirtualRacingLeague/1774_115.png)


### 3.9 parkinglotnerds8 (no base model, just cleaned data + slow driving + new fast, crop 47 )

```
(donkey) rainer@neuron:~/mysim2$ python manage.py train --tub /home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13,/home/rainer/mysim2/data/tub_50_20-04-14 --model ./models/parkinglotnerds9_crop47.h5
```
## 15.4.2020, donkey_ottawa code

### 3.10 parkinglotnerds10 (no base model)

```
(donkey) rainer@neuron:~/mysim2$ 
python manage.py train --tub /home/rainer/mysim2/data/tub_28_20-04-13,/home/rainer/mysim2/data/tub_29_20-04-13,/home/rainer/mysim2/data/tub_50_20-04-14,/home/rainer/mysim_ottawa/data/tub_8_20-04-15,/home/rainer/mysim_ottawa/data/tub_9_20-04-15,/home/rainer/mysim_ottawa/data/tub_10_20-04-15 --model ./models/parkinglotnerds10.h5

```


### 3.11 parkinglotnerds10 (running parkinglotnerd8.h5 with AI = 1.1 and saving & converting to train)

```
(donkey_ottawa) rainer@neuron:~/mysim2$ 
python manage.py train --tub /home/rainer/mysim_ottawa/data/AI_tub_48_20-04-16 --model ./models/parkinglotnerds11.h5

```



## 4 Running the model
```
(donkey) rainer@neuron:~/mysim2$ python manage.py drive --model ./models/parkinglotnerds1.h5
```

## 5 Discussion
- What are criteria that distinguish good from bad training data? 
- How could we measure them out of the data we have,e.g. jerk for trajectory elements?
- What are "best" driving strategies?
- Eh guys, do you remember the autonomous driving startup that used something like SAC (?) State Actor Critique, i.e. let the car drive some way and intervene when it drives of the road and give it a punishment in the reward function of the RL algorithm?

### BOSCH Abstatt
python manage.py train --tub /media/rainer/_data/20-data/M3-robocar_training/20191116-bosch-abstatt/tub_130_19-11-16  --model ./models/xx.h5
