# IR Robot
My robot is a car that reacts to infared stimuli using an IR sensor

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| David H | SAR Highschool | Electrical Engineering | Incoming Senior

![Headstone Image](https://media.discordapp.net/attachments/853028236509052999/857990285299417118/image0.jpg?width=760&height=1012)
  
# Final Milestone
work in progress 

[![Final Milestone](https://www.maillie.com/sites/default/files/02_02_18_508408464_aab_560x292.jpg)}

# Second Milestone
work in progress

[![Third Milestone](https://www.maillie.com/sites/default/files/02_02_18_508408464_aab_560x292.jpg)}

# Building Chassis
  

My first milestone for this project was just putting all the physical components together.  I built the frame of the car, attached the motors, attached the wheels, attached the batteries, attached the arduino, attached the motor controller and then i wired them all together.  One thing that was challenging was getting the perfboard, which i used to connect the motor controller and the IR sensor to the battery pack, to work correctly.  I didn't realize that i needed to create my own metal rails, I was under the assumption that, like a bread board, the perf board also has built in rails, but i was incorrect.  I have not yet been able to get the motors running-- i have a code but it isn't functional yet.  I have the IR sensor functioning correctly bu, but the mototrs are not moving they're just making a noise. moving forward i must figure out what the problem is that is stopping my motors from working, and once that happensI will be at my second milestone.
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
 <font color="#434f54">&#47;&#47;part for motor</font>
 &nbsp;<font color="#434f54">&#47;&#47; set all the motor control pins to outputs</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#d35400">pinMode</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">OUTPUT</font><font color="#000000">)</font><font color="#000000">;</font>


 &nbsp;<font color="#d35400">pinMode</font> <font color="#000000">(</font><font color="#000000">IRSensor</font><font color="#434f54">,</font> <font color="#00979c">INPUT</font><font color="#000000">)</font><font color="#000000">;</font> <font color="#434f54">&#47;&#47; sensor pin INPUT</font>
 &nbsp;
<font color="#000000">}</font>

<font color="#00979c">void</font> <font color="#5e6d03">loop</font><font color="#000000">(</font><font color="#000000">)</font>
<font color="#000000">{</font>
 &nbsp;<font color="#00979c">int</font> <font color="#000000">statusSensor</font> <font color="#434f54">=</font> <font color="#d35400">digitalRead</font> <font color="#000000">(</font><font color="#000000">IRSensor</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;
 &nbsp;&nbsp;<font color="#5e6d03">if</font> <font color="#000000">(</font><font color="#000000">statusSensor</font> <font color="#434f54">==</font> <font color="#000000">1</font><font color="#000000">)</font>
 &nbsp;<font color="#000000">{</font> <font color="#434f54">&#47;&#47; this function will run the motors in both directions at a fixed speed</font>
 &nbsp;&nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47;turn on motor A</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; turn on motor B</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#000000">0</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#000000">}</font>
 &nbsp;<font color="#5e6d03">else</font>
 &nbsp;<font color="#000000">{</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in1</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in2</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enA</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; turn on motor B</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in3</font><font color="#434f54">,</font> <font color="#00979c">HIGH</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">digitalWrite</font><font color="#000000">(</font><font color="#000000">in4</font><font color="#434f54">,</font> <font color="#00979c">LOW</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;&nbsp;&nbsp;<font color="#434f54">&#47;&#47; set speed to 200 out of possible range 0~255</font>
 &nbsp;&nbsp;&nbsp;<font color="#d35400">analogWrite</font><font color="#000000">(</font><font color="#000000">enB</font><font color="#434f54">,</font> <font color="#000000">200</font><font color="#000000">)</font><font color="#000000">;</font>
 &nbsp;<font color="#000000">}</font>
 &nbsp;
<font color="#000000">}</font>

</pre>
