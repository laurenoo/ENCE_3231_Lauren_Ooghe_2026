# 2-Wheel Robot Design
## This project incorporates the use of program and design software such as STMCubeIDE and KiCad.
<img width="700" height="650" alt="IMG_5727" src="https://github.com/user-attachments/assets/086b91ea-c3c8-439f-a0f1-8992509c93f3" />
<img width="700" height="650" alt="IMG_5721" src="https://github.com/user-attachments/assets/af5cb5f0-44ee-411d-9a42-b4c24b9322a0" />

### Block Diagram and System Diagram
<img width="469" height="272" alt="BLOCK_DIAGRAM" src="https://github.com/user-attachments/assets/f8de3491-926d-41aa-ac65-e8f7076a598d" />
<img width="515" height="272" alt="SYS_DIAGRAM" src="https://github.com/user-attachments/assets/e23a1d34-e3d5-4994-9486-1e553ea9548b" />


The main objective was to design and create a two-wheeled balancing robot using an STM32F401 microcontroller. All components were assembled to include soldering all components on the fabricated PCB, designing and cutting the acrylic chassis, and implementing test code for a 3-wheeled function to use for threshold testing. The 3-Wheel system is controlled by the use of an ESP8266 that provides a wifi signal (Access Point) to connect to a phone or tablet. The IP address is typed into the device and interfaces with the robot to perform manuevers such as forward, backward, left, right, or stop. The remote also receives a stream of data that is updated every 100 ms such as pitch, roll, velocity, and a counter. 

### Prototype

Once the 3-wheeled task was completed, I was motivated to try to incorporate PID control to balance on two wheels. This introduced the encoder which was orignally to be an MT6701 but we were provided with an AS5600. The difference between these components is the address it uses to connect through I2C. I used Claude code to create a ".h" and ".c" file to include in the "main.c" program to initiate the encoder. Once this was accomplished, the code was written, tested, and verified. The testing consisted of finding the natural pitch recorded when the robot is balanced. This was used as the setpoint needed to determine whether the robot needs to correct forward or backward. Ultimately, the 2-wheel balanced was acheived but not perfected. 

#### *** All PCB design materials are located in folder 2026_12_2Wheel_Balance_Robot_v1 2 ***
PCB layout used from Dr. Martins provided layout
