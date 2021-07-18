
# Hey Dad, Learn To Me !

Due to COVID-19 situation, lot of family shift to working from home and long distance learning, parents and kids share the same space for working and studing. 
For parents, it's good to take care you kids belong with you but some of time that's very challenge for me to switch work mode and family mode in the house. <br /><br />
Thanks for the high internet bandwidth at home, you can actually did all of your work at home with people around the world. <br /> 
That's mean you could be possible to sit on your dining table yo watch you computer from 7am morning until 9pm for one and one conf. calls without look and talk with your family. :sob: <br /> <br />
Because that, I'd like to create an interest interactivity program with kid then when they need to talk with parents then they can swipe or speech a key word to some of tiny machine to give parents heads up.<br />

## Project source
This project based on some of open-source project from Tiny Motion Trainer (https://experiments.withgoogle.com/tiny-motion-trainer), TensorFlow Lite for Microcontrollers (https://www.tensorflow.org/lite/microcontrollers) and Raspberry Pi Pico SDK (https://github.com/raspberrypi/pico-sdk).

## Hardware Board:
1. arduino nano 33 *2:<br />
      Use TFLu to detection gesture and key-word.
		 
2. micro:bit v2 *2<br />
      Communicate between commander and receiver. micro:bit provide a lot of funny multimedia widget like funny voice tone, led light strips and digital LED, so increase kid's interesting.
		
3. Raspberry Pi Pico Ardicam *1 <br />
      (https://www.arducam.com/raspberry-pi-pico-tensorflow-lite-micro-person-detection-arducam/)
      Use TFLu to person detection. (https://github.com/odincodeshen/tflite-micro/tree/main/tensorflow/lite/micro/examples/person_detection)
      Arduino nano doesn't support camera, so I use one of Pi PICO module from arducam. <br />

4. micro:bit hardware extension from Seees x Grove <br />
      https://www.seeedstudio.com/Grove-Inventor-Kit-for-micro-bit-p-2891.html

## How to Play:
They are two devices: <br />
A. Commander device <br />
B. Receiver device <br />

1. When kid want parents listen to him/her, kid will swipe commander device or speech a key word to the commander device.
2. Once device recognize the gesture or keywork, commander will send out command to Receiver device.
3. Then, parent received a sound and also LED lighting from the dining table. The speaker will buzzing evry few seconds.
4. To stop the buzzing, parent need put aside the work on hand and move the sight line into the receiver device. <br />
5. The receiver device will calcaute the image three times then stop the buzzing. At that time, parent could focus on what the kid what's the talk about.

## Have fun and hope you can enjoy :blush:
<br />
<br />
<br />

## Motion Training
When I bring this idea to discuss with kid, we decide two of gestures, time-out and roll.

### Time out 
<a href="https://www.youtube.com/embed/aCJEFmkYoiE
" target="_blank"><img src="/photos/time_out_gesture.PNG" 
alt="Time-out Gesture Example" width="480" height="480" border="10" /></a>
<br />

### Roll
<a href="https://www.youtube.com/embed/iG2-kHf2zCA
" target="_blank"><img src="/photos/roll_gesture.PNG" 
alt="Roll Gesture Example" width="480" height="480" border="10" /></a>
<br />

### Machine Learning Training
Then, we follow up this Tiny Motion Trainer (https://experiments.withgoogle.com/tiny-motion-trainer) to create two of gestures. <br />

Collect 50 samples for "Time-Out" <br />

<img src="/photos/motion_training4.PNG" width="1000px" />   
<br />

Collect 50 samples for "Roll"<br />
<img src="/photos/motion_training3.PNG" width="1000px" />   
<br />

Start the training on Google Cloud. <br />
<img src="/photos/motion_training5.PNG" width="1000px" />   
<br />

Verified the trained model, looks pretty well on my try. :blush: <br />
<img src="/photos/motion_training1.PNG" width="800px" />   
<img src="/photos/motion_training2.PNG" width="800px" />   
<br />

Finally, download the example code into my local machine to add communication function.




