class: title-slide
count: false
.logo-title[]

# ELECTENG 209 Recap
### Building a Smart Energy Monitor

.TitleAuthor[Varun Bora, Thomas Culham, Pranav Gulati, David Cole]

---

layout: true
name: template_slide

.logo-slide[]
.footer[Team 30 - Varun Bora, Thomas Culham, Pranav Gulati, David Cole]

---
name: last_presentation

.last_presentation[
### Recap From Our Last Presentation
]

- Build a Bluetooth energy monitor that measures voltage, current, power and energy
- Development of sensors and signal conditioning circuits

.row[
.last-left[
.last_presentation[
### Since The Last Presentation
]
- Firmware finalized
- Breadboarding started, PCB has arrived
- Smart Energy Challenge attempted
]

.last-right[
  <img src="img/hardware/pcb.jpg" height="300" class="pcb-expand">
  <small>Figure I: PCB Design</small>
]
]

---
name: hardware

# Hardware

.row[
.row-left[
- Started to breadboard our project last week
- Learning about the wonders of noise in electrical signals
]
.row-right[
  <img src="img/hardware/breadboard.jpg">
  <small>Figure II: Breadboarding</small>
]
]

---
name: accuracy_1

# Accuracy (PI)

<div class="row">
  <div class="row-left">
    <img src="img/accuracy/voltage.png">
    <small>Figure III: Ideal vs Measured Voltage</small>
  </div>
  <div class="row-right">
    <img src="img/accuracy/current.png">
    <small>Figure IV: Ideal vs Measured Current</small>
  </div>
</div>

---
name: accuracy_2

# Accuracy (PII)

<div class="row">
  <div class="row-left">
.left[
- Brief was set to be within 5% of the true value
- Voltage and Current within 1%
- Power within 5%
  - Not as accurate as we would have liked
]
  </div>
  <div class="row-right">
      <img src="img/accuracy/power.png">
      <small>Figure V: Ideal vs Measured Power</small>
  </div>
</div>

---
name: flowcharts

# Firmware Implementation

<div class="row">
  <div class="row-left">
    <img src="img/firmware/main.png" class="leftzoom">
    <small>Figure VI: Main and sub-module logic</small>
  </div>
  <div class="row-right">
    <img src="img/firmware/adc.png" class="rightzoom">
    <small>Figure VII: ADC/Sensor logic</small>
  </div>
</div>

???
- Usage of state in the ADC interrupt.
- Auto-triggering the ADC with a 1ms timer to ensure 1kHz sample rate.

---
name: sec_1

# Smart Energy Challenge (PI)

<div class="row">
  <div class="row-left">
.left[
- Implement a web-based interface for data logging readings from the Smart Energy Monitor
- Option to utilize an IoT platform (ThingSpeak, Google Cloud IoT Core)
  - Not all platforms are free depending on usage
  - Limited customizability
]
  </div>
  <div class="row-right">
    <img src="img/challenge/thingspeak.png">
    <small>Figure VIII: ThingSpeak Interface</small>
    <small>Screenshot taken from https://thingspeak.com/channels/935349</small>
  </div>
</div>

---
name: sec_2

# Smart Energy Challenge (PII)

<div class="row">
  <div class="row-left"style="width: 65%">
.left[
- Bypassed IoT platforms and built our own with open-source libraries:
  - chart.js and zoom plugin for HTML charts
  - React.js to tie the interface together
  - node-serialport to read from the USB-to-serial adapter and/or bluetooth module
- Daemon module:
  - Reads from Smart Energy Monitor serial port
  - Stores in a MongoDB database
  - Pushes latest readings to clients via WebSocket
- Web interface:
  - Receives readings from daemon and displays on a user-friendly chart
]
  </div>
  <div class="row-right" style="width: 30%">
    <img src="img/challenge/flowchart.png" style="height: auto; width: auto;">
    <small>Figure IX: Challenge logic flowchart</small>
  </div>
</div>

---
name: sec_3

# Smart Energy Challenge (PIII)

.center[
  <img src="img/challenge/interface.png" height="425">
  <small>Figure X: Challenge interface</small>
]

---

class: title-slide
layout: false
count: false
.logo-title[]

# Acknowledgements
#### Special thanks to Duleepa and the TAs
#### for their valuable feedback and assistance throughout the semester.

---

class: title-slide
layout: false
count: false
.logo-title[]

# Questions?
### Thank you
