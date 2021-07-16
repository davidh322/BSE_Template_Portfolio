# IR Robot
My robot is a car that reacts to infared stimuli using an IR sensor

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| David H | SAR Highschool | Electrical Engineering | Incoming Senior

![Headstone Image](https://media.discordapp.net/attachments/853028236509052999/857990285299417118/image0.jpg?width=760&height=1012)

# Milestone #4
For the fourth milestone I switched the car from arduino to esp32 and I created an app to control the direction of the car, control the aim of the laser, and shoot the laser.  This step was big as i had no prior experience with esp32 or with RC.  The way I did this was by using a website called MIT app inventor to make a customized app.  this app has 4 buttons for direction, one button to shoot the laser, and a joystick to aim the servos of the laser turret.  Each of the five buttons send a different number when pressed.  The ESP32 reads these numbers using if statements in my code.  Depending on which button is pressed the motors will be run in different formations.  for for- every motor goes forward, for back- every motor moves back, for right- the left motors move forward and the right motors move back, and for left- the right motors move forward and the left motors move back.  For the joystick when the user moves the joystick the coordinates of the place its moved to are read and then mapped to fit degrees which than tells the servos to move in order to aim the laser correctly.  When the user wants to shoot the laser all they do is hit fire which sends a 1 to the esp32 telling it to shoot the laser.  I now have a car that functionally can be controlled and shot at a target.  One problem that i dealt with is that i originally used a joystick for the directions but the values were too confusing and messy so i used direct buttons instead.  moving orward i want the buttons to work more consistently and i want to be more exact with my controls

[![Milestone #4](https://res.cloudinary.com/marcomontalbano/image/upload/v1626447758/video_to_markdown/images/youtube--qc_6O92dDOM-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/qc_6O92dDOM "Milestone #4")

# Milestone #3
To get the second part of my project started I got the laser and the target to work together.  Before i built the car and everything i wanted to make sure that the laser and LDR both work.  I wired and coded the laser to shoot every second and i coded the LDR to recognize when it is hit by the laser.  I used analog write to have the laser turn on and off.  For the LDR I made code that turns on an LED when the readings of the LDR reached a certain level. One problem that i had to deal with was that the values of the LDR would sometimes be inconsistent and they would be different for different rooms. I solved this by just changing the level that set off the LED.
[![Milestone #3](https://res.cloudinary.com/marcomontalbano/image/upload/v1626446512/video_to_markdown/images/youtube--Jmryic6Yx3U-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/Jmryic6Yx3U "Milestone #3")

# Circuit Diagram #2


# Session #2: RC Laser Car
Once I decided to stay a second session my project took a new route.  I decided to leave autonomous robotics to learn more about remote control.  I devised a plan to create a robot controlled by an app on an android phone that allows the user to drive around and aim and shoot a laser at a target.  



# Final Milestone
work in progress 

[![Final Milestone](https://www.maillie.com/sites/default/files/02_02_18_508408464_aab_560x292.jpg)}

# Potential Additions
1. I want to add mecanum wheels so that my robot can move more freely
[![First Milestone](https://cdn.discordapp.com/attachments/853028236509052999/860516448161628190/image0.jpg)]}
2. I want to check out different functions of the IR sensor that i can use for my robot
3. i want to find a way to make the componenets more organized and to create a body that covers it
4. Remote control

# Obstacle Avoidance
Last year I made an object avoiding robot with an ultrasonic sensor however my robot was not that good so i decided to start with obstacle avoidance for my IR sensor because its familiar to me and i wanted to conquer it.

# Explanation of IR sensor
[![IR Sensor Explanation](https://res.cloudinary.com/marcomontalbano/image/upload/v1625233787/video_to_markdown/images/youtube--q11FJqHPQo4-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/q11FJqHPQo4 "IR Sensor Explanation")

# Second Milestone
My second milestone for this project was using the IR sensor to run obstacle avoidance.  My robot uses the IR sensor to determine wether there is an object in the way of my robot.  The IR(infared) sensor sends infared signals out of a terminal which bounce off of anything in its way.  These signals our received by another terminal- telling the sensor wether anything is in its way or not.  If anything comes within 1 centimeter of the sensor the car turns around.  In the code for my robot(as seen below) I do this by using an 'If-statement'. Typically, when there is nothing in the way, all 4 motors go forward, but when the sensor has a reading of less than 1 two motors go forward and two motors go backwards- turning the car around.  The wiring and coding for this project was quite challenging, I had to re-do the wiring multiple times, at one point I even re-did the entire wiring.  I put the wiring together myself without following instruction so I had to work backwards to create the correct code.  There were so many small parts that just a small problem, like the mototr controller being grounded to the battery pack rather than the arduino or declaring the wrong pins in the code, was enough to stop the entire circuit from working.  All this troubleshooting really taught me a lesson about engineering.  Engineering is a cycle- you cant just build something in one run and have it be finifshed.  Great work requires revision, not only in robotics but throughout The problem solving sector.  Moving forward I want to explore more functions of the IR sensor.  I will probably try to have my robot follow lines or work with a remote controll.  I am really having a great time working on this project and i relly want to take it very far.
[![milestone #2](https://res.cloudinary.com/marcomontalbano/image/upload/v1625232410/video_to_markdown/images/youtube--yfa9DlzGAm0-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/yfa9DlzGAm0 "milestone #2")

# Regression of Obstacle Avoidance:
5. Everything working- runs smoothly, turns enough, delay works, is able to run over wire, and is able to avoid walls multiple times
![5](https://im2.ezgif.com/tmp/ezgif-2-f866d16e0d13.gif)

4. Robot avoids obstacles but isnt working well enough yet
![4](https://im2.ezgif.com/tmp/ezgif-2-3a1a6f5a0807.gif)

3. after a lot of trouble shooting i finally get the robot to work but it still only runs back and forth
![3](https://im2.ezgif.com/tmp/ezgif-2-25792d17fb60.gif)

2. I get the robot and motors to turn on and make a noise
![2](https://im2.ezgif.com/tmp/ezgif-2-9369557ff8ae.gif)

1. I have the system working somewhat on seperate componenets in order to test the code
![1](https://im2.ezgif.com/tmp/ezgif-2-f69d2a8f0b8e.gif)
# Building Chassis
  

My first milestone for this project was just putting all the physical components together.  I built the frame of the car, attached the motors, attached the wheels, attached the batteries, attached the arduino, attached the motor controller and then i wired them all together.  One thing that was challenging was getting the perfboard, which i used to connect the motor controller and the IR sensor to the battery pack, to work correctly.  I didn't realize that i needed to create my own metal rails, I was under the assumption that, like a bread board, the perf board also has built in rails, but i was incorrect.  I have not yet been able to get the motors running-- i have a code but it isn't functional yet.  I have the IR sensor functioning correctly bu, but the mototrs are not moving they're just making a noise. moving forward i must figure out what the problem is that is stopping my motors from working, and once that happensI will be at my second milestone.
[![milestone #1](https://res.cloudinary.com/marcomontalbano/image/upload/v1625232694/video_to_markdown/images/youtube--wg4PHka5zfo-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://youtu.be/wg4PHka5zfo "milestone #1")
[![First Milestone](https://media.discordapp.net/attachments/853028236509052999/857980473094832159/image0.jpg?width=760&height=1014)]}

# Circuit Diagram

[![Circuit Diagram](![image](https://user-images.githubusercontent.com/86114808/123437303-87cef080-d59d-11eb-93a2-ef3df598d9dd.png)

# Code

<pre>
<font color="#00979c">int</font> <font color="#000000">IRSensor</font> <font color="#434f54">=</font> <font color="#000000">2</font><font color="#000000">;</font> <font color="#434f54">&#47;&#47; connect ir sensor to arduino pin 2</font>

<font color="#434f54">&#47;&#47;part for motor</font>
<font color="#434f54">&#47;&#47; connect motor controller pins to Arduino digital pins</font>
<font color="#434f54">&#47;&#47; motor one</font>
<font color="#00979c">int</font> <font color="#000000">enA</font> <font color="#434f54">=</font> <font color="#000000">5</font><font color="#000000">;</font>
<font color="#00979c">int</font> <font color="#000000">in1</font> <font color="#434f54">=</font> <font color="#000000">11</font><font color="#000000">;</font>
<font color="#00979c">int</font> <font color="#000000">in2</font> <font color="#434f54">=</font> <font color="#000000">10</font><font color="#000000">;</font>
<font color="#434f54">&#47;&#47; motor two</font>
<font color="#00979c">int</font> <font color="#000000">enB</font> <font color="#434f54">=</font> <font color="#000000">6</font><font color="#000000">;</font>
<font color="#00979c">int</font> <font color="#000000">in3</font> <font color="#434f54">=</font> <font color="#000000">9</font><font color="#000000">;</font>
<font color="#00979c">int</font> <font color="#000000">in4</font> <font color="#434f54">=</font> <font color="#000000">8</font><font color="#000000">;</font>



<font color="#00979c">void</font> <font color="#5e6d03">setup</font><font color="#000000">(</font><font color="#000000">)</font>
<font color="#000000">{</font>
 &nbsp;<font color="#434f54">&#47;&#47;part for motor</font>
 &nbsp;<font color="#434f54">&#47;&#47; set all the motor control pins to outputs</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>


 &nbsp;<font color="#d35400">pinMode</font> <font color="#000000">(</font><font color="#000000">IRSensor</font><font color="#434f54">,</font> <font color="#00979c">INPUT</font><font color="#000000">)</font><font color="#000000">;</font> <font color="#434f54">&#47;&#47; sensor pin INPUT</font>

<font color="#000000">}</font>

<font color="#00979c">void</font> <font color="#5e6d03">loop</font><font color="#000000">(</font><font color="#000000">)</font>
<font color="#000000">{</font>
 &nbsp;<font color="#00979c">int</font> <font color="#000000">statusSensor</font> <font color="#434f54">=</font> <font color="#d35400">digitalRead</font> <font color="#000000">(</font><font color="#000000">IRSensor</font><font color="#000000">)</font><font color="#000000">;</font>

 &nbsp;<font color="#5e6d03">if</font> <font color="#000000">(</font><font color="#000000">statusSensor</font> <font color="#434f54">&lt;</font> <font color="#000000">1</font><font color="#000000">)</font>
 &nbsp;<font color="#000000">{</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47;this function will run the motors in both directions at a fixed speed</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; &nbsp;&nbsp;&nbsp;&nbsp;turn on motor A</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47;turn on motor B</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;&nbsp;<font color="#d35400">delay</font><font color="#000000">(</font><font color="#000000">3000</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#000000">}</font>
 &nbsp;<font color="#5e6d03">else</font>
 &nbsp;<font color="#000000">{</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; turn on motor B</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;
 &nbsp;<font color="#000000">}</font>
 
<font color="#000000">}</font>

</pre>
