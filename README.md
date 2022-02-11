<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/Adell02/LORA-NET">
    <img src="img/logo.png" alt="Logo" >
  </a>

<p align="center">
    A unique radio network
    <br /><br />
    <a href="https://github.com/Adell02/LORA-NET/issues">Report Bug</a>
    ·
    <a href="https://github.com/Adell02/LORA-NET/issues">Request Feature</a>
  </p>
</div>

<p align="center"><strong>IMPORTANT! The project is being developed, for that reason, the features that aren't available at the moment will be marked as 🔴</strong></p>
<br />

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#user-nodes">User Nodes</a></li>
        <li><a href="#middle-nodes">Middle Nodes</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#hardware-connections">Hardware Connections</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

<!-- ABOUT THE PROJECT -->
## About The Project
The aim of LORA net is to learn building a network based in 2.4GHz LoRa communication modules and ATmega328P U (Arduino Uno) as microcontroller. 

LORA net consists in a mesh network based in two kind of nodes: `User Nodes` and `Middle Nodes`. 

### User Nodes

Each user with an apropiate LoRa module and settings can access the network using the python-based desktop application in the <a href="https://github.com/Adell02/LORA-NET/GUI_v.0">GUI folder</a>. 
There are (to date) three main functions available for User Nodes:
<ul>
  <br />
  <li><strong>🔴Google Search:</strong> The node request to any other in the network with internet connection available a Google Search. The User receives the entries relative to that search and can choose from which of all to get the text in it. </li>
  <li><strong>Private Message:</strong> The desired message is sent to a specific node in the network (acording to an ID) if it's available.</li>
  <li><strong>File Transfer:</strong> Sending compressed via radio to any other user in the net</li>
</ul>

### 🔴Middle Nodes

Most of the nodes of the network may be Middle Nodes in order to ensure a good performance of the net at long distances. These nodes are responsible for receiving, analyzing where are the packets addressed to and sending them again following the most efficient route when a transmission can't directly reach the recipient node.  


We are working to bring a feature that allows converting a User Node into a Middle Node whenever needed, imporving the net performance.

## Getting Started
This project is based on the Arduino Uno and Semtech's modules SX127x. 

### Hardware Connections
<div>
  <img src="https://user-images.githubusercontent.com/84263340/153633151-c42c3546-dbfb-435a-bd68-98cd23723e13.png" width="200" height="200">
  <img src="https://user-images.githubusercontent.com/84263340/153633898-49054876-de93-42f7-8cde-cd6fd96ee445.png" width="200" height="200">
</div>

| SX127x  | Arduino Uno |
| ------------- | ------------- |
| NSS  | D10  |
| MOSI  | D11  |
| MISO  | D12  |
| SCK  | D13  |
| GND  | GND  |
| 3.3V  | 3.3V  |
| RST  | D9  |
| DIO0  | D2  |


<br />

### Files
Every file regarding the uC is programmed with the Arduino IDE (C++). The main Arduino file (Arduino_GUI.ino) is located <a href="https://github.com/Adell02/LORA-NET/GUI_v.0/Arduino_GUI">here</a> and works in line with the main python program named <a href="https://github.com/Adell02/LORA-NET/GUI_v.0/">gui.py</a>.

Commenting our code is relevant to make it readable. 
