# Hand Protection Alert System
### Table of Content
  * [Overview](#overview)
  * [Architechture](#architechture)
  * [Demo](#demo)
  * [Installation](#installation)
  * [Technology Stack](technologystack)
 
 ### **Overview**
- In any production line safety of the worker is the first priority so that they can work safely and confidently which eventually increase the growth in a company. So this project try to solve that issue by building a system which can be deployed through **IP Camera, Microcontroller, Relay etc**.
  - There are two lines in our system which makes worker cautious, one is safety line in which if workers hand reaches **ALARM Continously Set ON** and another is **Boundary Line** in which if workers hand reaches **Machine Automatically Swiched off from the command Microcontroller gives.**

### **Architechture**
![shredder](https://user-images.githubusercontent.com/75604769/177889835-3dd92603-1340-43ce-9683-48fe7a5dee6b.png)

### **Demo video**


https://github.com/yashn1998/Hand_protection_alert_system/assets/102281447/41d6dbfe-cf9b-4416-bbfb-322079d6eca6


### :raising_hand: Project Workflow 

Our pipeline consists of three steps:
  1. An AI model which detect all human hands in the live video.
  2. An AI model which predict if that hands is out of safety line.
  3. The output is **ALARM** to alert worker and shutting down a machine if hamd crosses **Boundary line**.
  
### 🚀 Model's performance
  - **Faster RCNN** give unrealistic **MAP** value of 85 so I choose to finalized my model by training it on **SSD MobileNetV2 which give me a MAP in between 70.**
  - First training with **3500** images gives the **MAP** of **60** so I increased the data to **7500. and it gives MAP of 85 in Faster RCNN and 70 on SSD MobileNetV2.**

