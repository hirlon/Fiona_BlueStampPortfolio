# Robotic Arm
With the help of servos at each joint, the robotic arm is extremely flexible. You can control the arm via a smartphone or a 2 joystick controller

```HTML
```

| **Engineer** | **School** | **Area of Interest** | **Grade** |
|:--:|:--:|:--:|:--:|
| Fiona L | The Nightingale-Bamford School | Robotics | Incoming Junior


![Headstone Image](logo.svg)
  
# Final Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/D3Orj-GOAwU?si=ew9-6m_k9eDBSQP9" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

# First Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/y3VAmNlER5Y" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Description
My first milestone was the assembly of the robotic arm and the joycon but before assembling I had to test each individual component. There are 3 main components of the robotic arm: the power source, the arduino nano board, and the arm itself. For the power source, I used 5 standard double a batteries and because I used a different power source than what was given. I had to solder the battery holder's wires to the arduino. The Nano is placed in the middle of the arm and basically acts like the brain because all the wires ultimately connect to it. How it'll work is that when I move the joystick it'll send a signal to the shield and the arduino will use the uploaded code to transmit and electronic signal to the servos.

## Challenges
Throughout my project I ran in to a major problem. I used a different power source than the default one so I couldnt attach the battery holder on to the board I was provided with. SO I ended up using velcro.

## Next Steps

# Starter Project Milestone

<iframe width="560" height="315" src="https://www.youtube.com/embed/5hE3g0E7hIk?si=tdlVj-aOWcgm4DSa" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Description
For my start project, I chose the RBG slides. I took digital design/fabrication classes prior to this program so I had experience working with LED lights. I chose
this starter project because it felt comfortable and familiar. This kit includes a PCB and LED components, LEDs are semiconductor devices that emit light when an electric current passes through them. Each LED represents one of the primary colors (Red, Green, and Blue). By controlling the intensity of each LED, you can create a wide range of colors. 

## Challenges
Soldering was difficult because there was a lot to solder and I had learned how to right before starting this project. 

## Next Steps
For my next milestone, I will be moving on to my intensive project.

# Code
Here's where you'll put your code. The syntax below places it into a block of code. Follow the guide [here]([url](https://www.markdownguide.org/extended-syntax/)) to learn how to customize it to your project needs. 

```c++
void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  Serial.println("Hello World!");
}

void loop() {
  // put your main code here, to run repeatedly:

}
```
# Schematics
<img src="https://abhimahajan-1.github.io/Abhi_BlueStampPortfolio/schematics_3_revised_2.png" alt="Figure 1: Remote control and servos">
Figure 1: A visual of the remote control and servos wiring.

# Bill of Materials

| **Part** | **Note** | **Price** | **Link** |
|:--:|:--:|:--:|:--:|
| Cokoino Robot Arm | Contains joycon and a robotic arm | $49.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/LK-COKOINO-Compliment-Engineering-Technology/dp/B081FG1JQ1)"> Link </a> |
| 5 AA Battery Holder | Holds 5 Double A Batteries | $7.99 | <a href="[https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/](https://www.amazon.com/LampVPath-Battery-Holder-Leads-Wires/dp/B07WRQ44YK/ref=sr_1_6?crid=3OUOUDN2BFP73&keywords=5+AA+battery+pack&qid=1689046519&sprefix=5+aa+battery+pack%2Caps%2C158&sr=8-6)"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |
| Item Name | What the item is used for | $Price | <a href="https://www.amazon.com/Arduino-A000066-ARDUINO-UNO-R3/dp/B008GRTSV6/"> Link </a> |


