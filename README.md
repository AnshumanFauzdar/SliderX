# SliderX

![SliderX](https://user-images.githubusercontent.com/40523329/147356925-ddfb1e2e-24bf-4f23-be9e-166d78cc5f8e.png)

Open-Sourced camera slider with silent stepper motor driver and 3D printable parts soon to be released on kickstarter!

# Development

Currently development is divided into 3 parts:
- [Hardware Development including PCB](https://github.com/AnshumanFauzdar/SliderX/tree/main/hardware)
- [Webserver Development](https://github.com/AnshumanFauzdar/SliderX/tree/main/dev)
- [Firmware Development](https://github.com/AnshumanFauzdar/SliderX/tree/main/firmware) [Firmware development is extended from [valar systems](https://github.com/daniel-frenkel/Valar-Systems)]

# Hardware Development
All the 3D printable parts are designed in solidworks 2019 and STL are uploaded on thingiverse

There are some possible design changes:
- Smaller stepper motor or change orientation to 90°
- Change standard screw mounting to M4
- Change v-slot gantry from 3D printable to standard market aluminum gantry
- change connecting parts to more modular design and DIY friendly

PCB Development:
v1.0.0 PCB contained following errors:
1. Small size
2. No mounting holes
3. Small ESP32 placement
4. No resistor for GPIO out
5. No indicator LEDs
6. Missing silk screen notations

v1.1.0 changes:
1. Fix issues from v1.0.0
2. Add 3.3v input for buttons GPIO connection
3. Add 4 indicator LEDs
4. Size increased to 75x50mm
5. Add fiducial markings

Initial PCBs were ordered from china, due to shipping issues it  is impossible to get from there. Looking actively for Indian manufacturers and will update here.

# WebServer Development
SliderX will be controllable with two methods - on-board controller and webserver control

UI mockup for SliderX:
![mockup](https://user-images.githubusercontent.com/40523329/142221151-5ddb3b99-8856-42a3-8ebc-c7356d45dd62.png)

Features implementation:
- control using websocket
- API implementation
- WiFi access point page
- fast rendering
- cross-platform implementation
- synced controls from on-board control

# Firmware Development
Firmware development is extended from [valar systems](https://github.com/daniel-frenkel/Valar-Systems)

TMC2209 is used in this project for silent operation and additional features like stallguard

Features to be implemented in firmware:
- Stallguard to replace end switch
- on-board control with LCD and rotary encoder
- minify code with web-socket implementation
- automated testing with github actions
