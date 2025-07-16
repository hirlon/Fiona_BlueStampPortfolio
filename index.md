# Robotic Arm
With the help of servos at each joint, the robotic arm is extremely flexible. You can control the arm via a smartphone or a 2 joystick controller.

```HTML
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Fiona L | The Nightingale-Bamford School | Robotics/AI | Incoming Junior |


![Headstone Image](logo.svg)

# Third Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/oH3SdCt35vY?si=WwMIM5t4r-W3lIPx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description
For my third milestone I connected my robotic arm to my phone via an HC-05 bluetooth module.

### HC-05
<img width="500" height="350" src="https://m.media-amazon.com/images/I/61CU5YmBsEL._UF894,1000_QL80_.jpg" alt=" ">

In bluetooth communication, there is a master/slave configuration, indicating which device will initiate/control the connection. I set my HC-05 as a slave because I want it to receive connections/signals from my phone which will act as the master. When connecting the bluetooth module, there are 2 modes: AT mode and bluetooth (data) mode. AT mode is used to configure/control the bluetooth module itself and bluetooth mode is just connecting and communicating with other bluetooth devices. In this case, we are using data mode so it can directly exchange data with my phone. The HC-05 also has 6 pins: State, VCC, GND, TXD, RXD, Key. Out of the 6 pins I connected 4 of them: VCC (provides power to the module), GND (ground connection), TXD (transmits data), and RXD (receives data). The TXD pin of one device must be connected to the RXD pin of the other device and vice versa because you cannot have 2 devices receiving/transmitting simultaneously. 

### PWM
The servo I use is called a hobby servo which uses PWMs to contorl their position. They have 3 wires: power, ground, and control. The PWM signal that is sent ot the servo's control wire instructs the angle of the servo's output shaft. A PWM signal is a digital signal that represents analog values and it alternates between 2 voltage levels. One of the key things about PWMs is its duty cycle (The ratio of the "on" time to the total period of the signal). For example, if a PWM signal has a period of 10 milliseconds and is "on" for 3 milliseconds, its duty cycle is 30% (3 milliseconds/10 milliseconds). By changing the duty cycle, the average voltage delivered to my servo will vary (Higher duty cycle = higher average and lower duty cycle = low average voltage). So how does adjusting the duty cycle affect my servo? Adjusting the duty cycle affects how much voltage is delivered which in turn controls my servos speed from slow to fast. 

### MIT App Inventor
<img width="887" height="462" alt="Screenshot 2025-07-15 110617" src="https://github.com/user-attachments/assets/7a207af4-49aa-49b3-9171-9f933fd79668" />

After attaching the HC-05 to my robotic arm, I created an app using the MIT app inventor to be able to control the robotic arm. On the app there is a button that allows me to connect to the bluetooth module, a button that resets all the servos to 90°, and six buttons that move the joints of the robotic arm (base, joints, and claw). When a button is pressed on my block code, a number is outputted. The movement of the servo depends on the number that was outputted so when my arduino receives that number, it'll change the movement of the servo.

## Challenges
One of the challenges I faced during my third milestone was my robotic arm moving by itself. Although I unplugged the pins from the joysticks, the servos were still receiving unwanted signals which conflicts with the signals I was originally trying to send. I fixed this by commenting out/deleting any code correlated to the joystick. Another challenge I had was my claw suddently not working, turns out the wires on the servo broke off so I just had to replace it.

## Next Steps
For my modifications, I am planning to add more joints to my robotic arm using cadded parts.

# Second Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/s6oYnf6QK6A?si=ZWjJvlmnjy_reT9l" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description
My second milestone was to program the joystick to be able to move my robotic arm. The joysticks send analog values to the arduino nano because each joystick produce a continuous range of voltage levels that represent how far the stick is pushed. Unlike digital values which are HIGH or LOW (1 or 0), analog values are much more precise which makes the movement of the robotic arm much more smoother. In my code, I use specific functions from the code library to translate these analog readings into servo movements. For example, the arm.up(speed) and arm.down(speed) move the arm up and down. arm.left(speed) and arm.right(speed) rotate the base and arm.open(speed) arm.close(speed) open and closes the claw of the robotic arm. The code checks the values of my joystick and based on that range, it will instuct the arm to move how many units and in which direction. There is also a function on my arm where it can repeat captured actions by first declaring a pointer to an integer. Then it captures the action and assigns it to the pointer. 


## Challenges
One of the challenges I faced during this milestone was the servo that was connected to the claw started moving eratically. I assumed it was a problem within the code but after thorougly checking it, I found nothing wrong. Another problem I considered was the servo was not receiving enough energy to power it. Eventually I realized that there was a problem with the servo itself.   

## Next Steps
For my last milestone, I will be connecting the robotic arm to an HC-05 via bluetooth so it'd be able to be controlled by a phone using the MIT inventor app.

# First Milestone
<iframe width="560" height="315" src="https://www.youtube.com/embed/Yta8FxtyrU0?si=a-qyl68ZN326yS7z" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description
My first milestone was the assembly of the robotic arm and the joycon but before assembling I had to test each individual component. There are 3 main components of the robotic arm: the power source, the arduino nano board, and the arm itself. For the power source, I used 5 standard double a batteries and because I used a different power source than what was given (2 lithium ion batteries). I had to cut the battery holder's wire and solder its wires to the arduino. The Nano is placed in the base of the arm and basically acts like the brain because all the wires ultimately connect to it. Once my project is fully programmed, when I move the joystick it'll send a signal to the shield and the arduino will use the uploaded code to transmit an electronic signal to the servos. 

## Challenges
Throughout my project I ran in to a major problem. I used a different power source than the default one so I couldnt attach the battery holder on to the board I was provided with. So I ended up using velcro.

*Insert photo of velcro*

## Next Steps
Next I plan to compile and upload the code to be able to control the robotic arm.

# Starter Project Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/5hE3g0E7hIk?si=tdlVj-aOWcgm4DSa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description
For my start project, I chose the RBG slides. I took digital design/fabrication classes prior to this program so I had experience working with LED lights. I chose
this starter project because it felt comfortable and familiar. This kit includes a PCB and LED components, LEDs are semiconductor devices that emit light when an electric current passes through them. Each LED represents one of the primary colors (Red, Green, and Blue). By controlling the intensity of each LED, you can create a wide range of colors. 

## Challenges
Soldering was difficult because there was a lot to solder and I had learned how to right before starting this project. 

## Next Steps
For my next milestone, I will be moving on to my intensive project.

# Schematics
<img src="https://abhimahajan-1.github.io/Abhi_BlueStampPortfolio/schematics_3_revised_2.png" alt="Figure 1: Remote control and servos">
Figure 1: A visual of the remote control and servos wiring (Taken from COKOINO).

## Code (Milestone 3)
```
#include "src/CokoinoArm.h"
#include <SoftwareSerial.h>
#define buzzerPin 9

int state=0;
CokoinoArm arm;
int xL,yL,xR,yR;
SoftwareSerial BTSerial(3,2);
const int act_max=10;    
int act[act_max][4];   
int num=0,num_do=0;
void turnUD(void){
  if(xL!=512){
    if(0<=xL && xL<=100){arm.up(10);return;}
    if(900<xL && xL<=1024){arm.down(10);return;} 
    if(100<xL && xL<=200){arm.up(20);return;}
    if(800<xL && xL<=900){arm.down(20);return;}
    if(200<xL && xL<=300){arm.up(25);return;}
    if(700<xL && xL<=800){arm.down(25);return;}
    if(300<xL && xL<=400){arm.up(30);return;}
    if(600<xL && xL<=700){arm.down(30);return;}
    if(400<xL && xL<=480){arm.up(35);return;}
    if(540<xL && xL<=600){arm.down(35);return;} 
    }
}
void turnLR(void){
  if(yL!=512){
    if(0<=yL && yL<=100){arm.right(0);return;}
    if(900<yL && yL<=1024){arm.left(0);return;}  
    if(100<yL && yL<=200){arm.right(5);return;}
    if(800<yL && yL<=900){arm.left(5);return;}
    if(200<yL && yL<=300){arm.right(10);return;}
    if(700<yL && yL<=800){arm.left(10);return;}
    if(300<yL && yL<=400){arm.right(15);return;}
    if(600<yL && yL<=700){arm.left(15);return;}
    if(400<yL && yL<=480){arm.right(20);return;}
    if(540<yL && yL<=600){arm.left(20);return;}
  }
}
void turnCO(void){
  if(arm.servo4.read()>7){
    if(0<=xR && xR<=100){arm.close(0);return;}
    if(900<xR && xR<=1024){arm.open(0);return;} 
    if(100<xR && xR<=200){arm.close(5);return;}
    if(800<xR && xR<=900){arm.open(5);return;}
    if(200<xR && xR<=300){arm.close(10);return;}
    if(700<xR && xR<=800){arm.open(10);return;}
    if(300<xR && xR<=400){arm.close(15);return;}
    if(600<xR && xR<=700){arm.open(15);return;}
    if(400<xR && xR<=480){arm.close(20);return;}
    if(540<xR && xR<=600){arm.open(20);return;} 
    }
  else{arm.servo4.write(8);
  }  
}

void date_processing(int *x,int *y){
  if(abs(512-*x)>abs(512-*y))
    {*y = 512;}
  else
    {*x = 512;}
}

void buzzer(int H,int L){
  while(yR<420){
    digitalWrite(buzzerPin,LOW);
    delayMicroseconds(H);
    digitalWrite(buzzerPin,LOW);
    delayMicroseconds(L);
    }
  while(yR>600){
    digitalWrite(buzzerPin,LOW);
    delayMicroseconds(H);
    digitalWrite(buzzerPin,LOW);
    delayMicroseconds(L);
    }
}

void C_action(void){
  if(yR>800){
    int *p;
    p=arm.captureAction();
    for(char i=0;i<4;i++){
    act[num][i]=*p;
    p=p+1;     
    }
    num++;
  }
}


void setup() {
  Serial.begin(9600);
  BTSerial.begin(9600);
  //arm of servo motor connection pins
  arm.ServoAttach(4,5,6,7);
  arm.servo1.write(90);
  arm.servo2.write(90);
  arm.servo3.write(90);
  arm.servo4.write(90);
}

void loop() {
  if(BTSerial.available()>0){
    state=BTSerial.read();
  }
  if(state==1){
    arm.down(20);
  }
  if(state==3){
    arm.up(20);
  }
  if(state==5){
    arm.left(20);
  }
  if(state==7){
    arm.right(20);
  }
  if(state==9){
    arm.open(20);
  }
  if(state==11){
    arm.close(20);
  }
  if(state==13){
    arm.servo1.write(90);
    arm.servo2.write(90);
    arm.servo3.write(90);
    arm.servo4.write(90);
  }
  if(arm.servo4.read()<7){
    arm.servo4.write(8);
  }
  Serial.println(state);
}
```
## Code (Milestone 2)
```
#include "CokoinoArm.h"
#include <SoftwareSerial.h>
#define buzzerPin 9
int state=0;
CokoinoArm arm;
int xL,yL,xR,yR;
SoftwareSerial BTSerial(3,2);
const int act_max=10;    //Default 10 action,4 the Angle of servo
int act[act_max][4];    //Only can change the number of action
int num=0,num_do=0;
void turnUD(void){
  if(xL!=512){    // This code checks the value of xL, and based on the range, will instruct the robotic arm to move up/down x units.
    if(0<=xL && xL<=100){arm.up(10);return;}
    if(900<xL && xL<=1024){arm.down(10);return;} 
    if(100<xL && xL<=200){arm.up(20);return;}
    if(800<xL && xL<=900){arm.down(20);return;}
    if(200<xL && xL<=300){arm.up(25);return;}
    if(700<xL && xL<=800){arm.down(25);return;}
    if(300<xL && xL<=400){arm.up(30);return;}
    if(600<xL && xL<=700){arm.down(30);return;}
    if(400<xL && xL<=480){arm.up(35);return;}
    if(540<xL && xL<=600){arm.down(35);return;} 
    }
}
void turnLR(void){    
  if(yL!=512){    // This code checks the value of yL, and based on the range, will instruct the robotic arm to move left/right x units.
    if(0<=yL && yL<=100){arm.right(0);return;}
    if(900<yL && yL<=1024){arm.left(0);return;}  
    if(100<yL && yL<=200){arm.right(5);return;}
    if(800<yL && yL<=900){arm.left(5);return;}
    if(200<yL && yL<=300){arm.right(10);return;}
    if(700<yL && yL<=800){arm.left(10);return;}
    if(300<yL && yL<=400){arm.right(15);return;}
    if(600<yL && yL<=700){arm.left(15);return;}
    if(400<yL && yL<=480){arm.right(20);return;}
    if(540<yL && yL<=600){arm.left(20);return;}
  }
}
void turnCO(void){
  if(arm.servo4.read()>7){    // This function checks the position of servo 4. If the reading is greater than 7, the conditionals will execute and the claw will open/close x units based on the value given. If the conditional is false (the reading is less than 7) it will set servo 4 to position 8.
    if(0<=xR && xR<=100){arm.close(0);return;}
    if(900<xR && xR<=1024){arm.open(0);return;} 
    if(100<xR && xR<=200){arm.close(5);return;}
    if(800<xR && xR<=900){arm.open(5);return;}
    if(200<xR && xR<=300){arm.close(10);return;}
    if(700<xR && xR<=800){arm.open(10);return;}
    if(300<xR && xR<=400){arm.close(15);return;}
    if(600<xR && xR<=700){arm.open(15);return;}
    if(400<xR && xR<=480){arm.close(20);return;}
    if(540<xR && xR<=600){arm.open(20);return;} 
    }
  else{arm.servo4.write(8);

  }  
}
void date_processing(int *x,int *y){    // This function sets one of these values to 512 by comparing which of the 2 values are closer. 
  if(abs(512-*x)>abs(512-*y))    // The abs function computes the absolute value of the difference between 512 and the values of x and y
    {*y = 512;}
  else
    {*x = 512;}
}

void buzzer(int H,int L){	  // Defines a function named buzzer
  while(yR<420){	  // This loop will continue executing as long as the value of yR is less than 420
    digitalWrite(buzzerPin,HIGH);	  // Sets the buzzerpin to high, which activates it.
    delayMicroseconds(H);  	// This determines the duration of the buzzer.
    digitalWrite(buzzerPin,LOW);	  // Sets the buzzerpin to low, turning it off.
    delayMicroseconds(L);  	// This determines the duration that the buzzer is silent.
    yR = arm.JoyStickR.read_y();    // Updates the value of yR by reading the position of the joystick.
    }

  while(yR>600){  // Read above
    digitalWrite(buzzerPin,HIGH);
    delayMicroseconds(H);
    digitalWrite(buzzerPin,LOW);
    delayMicroseconds(L);
    yR = arm.JoyStickR.read_y();
    }
}

void C_action(void){
  if(yR>800){		//Checks if the variable yR is greeting than 800
    int *p;		//Declares a pointer to an integer
    p=arm.captureAction();		//Captures action and assigns to pointer
    for(char i=0;i<4;i++){		//A loop repeats 4 times to capture actions and store them.
    act[num][i]=*p;		//Stores the value pointed by p
    p=p+1;		//Moves the pointer to the next integer 
    }
    num++;		//Increments the action count
    num_do=num;		//Updates the amount of actions done
    if(num>=act_max){		//If actions exceed the max amount → Resets to zero and buzzer will sound at 600Hz for 400 milliseconds
      num=0;
      buzzer(600,400);
      }

    while(yR>600){yR = arm.JoyStickR.read_y();}
    //Serial.println(act[0][0]);
  }
}
void Do_action(void){
  if(yR<220){
    buzzer(200,300);
    for(int i=0;i<num_do;i++){
      arm.do_action(act[i],15);
      }
    num=0;
    while(yR<420){yR = arm.JoyStickR.read_y();}
    for(int i=0;i<2000;i++){
      digitalWrite(buzzerPin,HIGH);
      delayMicroseconds(200);
      digitalWrite(buzzerPin,LOW);
      delayMicroseconds(300);        
    }
  }
}
void setup() {
  Serial.begin(9600);  //Initializes serial connection
  BTSerial.begin(9600);    // Initializes bluetooth communication
  // arm of servo motor connection pins
  arm.ServoAttach(5,11,7,10);
  // arm of joy stick connection pins : xL,yL,xR,yR
  arm.JoyStickAttach(A0,A1,A2,A3);
  pinMode(buzzerPin,OUTPUT);  // Sets buzzer as an output
  // Sets all servo at 90 degrees
  arm.servo1.write(90);
  arm.servo2.write(90);
  arm.servo3.write(90);
  arm.servo4.write(90);
}

void loop() {
  if(BTSerial.available()>0){    // Allows devices to communicate wirelessly
    state=BTSerial.read();    // This variable is used to determine which command had been received and what action the arm should perform.
  }
  if(state==1){
    arm.down(20);//moves arm up just says down
  }
  if(state==3){
    arm.up(20);//moves arm down just says up
  }
  if(state==5){
    arm.left(20);
  }
  if(state==7){
    arm.right(20);
  }
  if(state==9){
    arm.open(20);
  }
  if(state==11){
    arm.close(20);
  }
  if(state==13){
    arm.servo1.write(90);
    arm.servo2.write(90);
    arm.servo3.write(90);
    arm.servo4.write(90);
  }
  if(arm.servo4.read()<7){
    arm.servo4.write(8);
  }

  Serial.println(state);
  xL = arm.JoyStickL.read_x();
  yL = arm.JoyStickL.read_y();
  xR = arm.JoyStickR.read_x();
  yR = arm.JoyStickR.read_y();
  date_processing(&xL,&yL);
  date_processing(&xR,&yR);
  turnUD();
  turnLR();
  turnCO();
  C_action();
  Do_action();
}
```
# Bill of Materials
| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Cokoino Robot Arm | Contains joycon and a robotic arm | $49.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/LK-COKOINO-Compliment-Engineering-Technology/dp/B081FG1JQ1)"> Link </a> |
| 5 AA Battery Holder | Holds 5 Double A Batteries | $7.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/LampVPath-Battery-Holder-Leads-Wires/dp/B07WRQ44YK/ref=sr_1_6?crid=3OUOUDN2BFP73&keywords=5+AA+battery+pack&qid=1689046519&sprefix=5+aa+battery+pack%2Caps%2C158&sr=8-6)"> Link </a> |
