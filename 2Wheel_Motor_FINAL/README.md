
# 2-Wheel Robot Design
## This project incorporates the use of program and design software such as STMCubeIDE and KiCad.
## Introduction
The main objective was to design and create a two-wheeled balancing robot using an STM32F401 microcontroller. All components were assembled to include soldering all components on the fabricated PCB, designing and cutting the acrylic chassis, and implementing test code for a 3-wheeled function to use for threshold testing.

<img width="700" height="650" alt="IMG_5727" src="https://github.com/user-attachments/assets/086b91ea-c3c8-439f-a0f1-8992509c93f3" />
<img width="700" height="650" alt="IMG_5721" src="https://github.com/user-attachments/assets/af5cb5f0-44ee-411d-9a42-b4c24b9322a0" />

### Block Diagram and System Diagram
<img width="469" height="272" alt="BLOCK_DIAGRAM" src="https://github.com/user-attachments/assets/f8de3491-926d-41aa-ac65-e8f7076a598d" />
<img width="515" height="272" alt="SYS_DIAGRAM" src="https://github.com/user-attachments/assets/e23a1d34-e3d5-4994-9486-1e553ea9548b" />


 ### Design
 The PCB was designed in KiCAD and the images of layout and schematics can be seen below.

 <img width="350" height="220" alt="PCB_LAYOUT" src="https://github.com/user-attachments/assets/59df63c5-cb81-443e-9675-41336429c2c0" />
<img width="350" height="220" alt="PCB_3D" src="https://github.com/user-attachments/assets/310d4ae0-0ddd-448f-8e86-0cd55dc58786" />
<img width="470" height="370" alt="SCHEMATIC" src="https://github.com/user-attachments/assets/a2320a6b-887c-4aa2-84c1-be9037b0ee8f" />



### Prototyping
Once all components were verified working, such as the ESP8266 wifi chip, the motors, and the USB connection, the chassis was designed using OnShape CAD program to provide a drawing that could be used to verify part placement such as the PCB, motor mounts, battery pack, and front caster wheel. 

<img width="584" height="464" alt="Screenshot 2026-06-08 at 7 30 15 PM" src="https://github.com/user-attachments/assets/57ee3094-a15a-4fc8-9c2c-2eb2f32f5af7" />

Once the layout was verified with a 'dry fit', a .DXF file was downloaded from the CAD software and used in the laser cutter to shape and cut the acrylic chassis. All components were mounted and the robot was ready for testing.

### Testing
The 3-Wheel system is controlled by the use of an ESP8266 that provides a wifi signal (Access Point) to connect to a phone or tablet. The IP address is typed into the device and interfaces with the robot to perform manuevers such as forward, backward, left, right, or stop. The remote also receives a stream of data that is updated every 100 ms such as pitch, roll, velocity, and a counter. 

<img width="300" height="700" alt="IMG_5737" src="https://github.com/user-attachments/assets/3a0bd0db-daa6-461c-875e-eb4b80136832" />

https://github.com/user-attachments/assets/3100aa6c-19b2-47c0-a776-326ca26b746c


Once the 3-wheeled task was completed, I was motivated to try to incorporate PID control to balance on two wheels. This introduced the encoder which was orignally to be an MT6701 but we were provided with an AS5600. The difference between these components is the address it uses to connect through I2C. I used Claude code to create a ".h" and ".c" file to include in the "main.c" program to initiate the encoder. Once this was accomplished, the code was written, tested, and verified. The testing consisted of finding the natural pitch recorded when the robot is balanced. This was used as the setpoint needed to determine whether the robot needs to correct forward or backward. Ultimately, the 2-wheel balanced was acheived but not perfected. 



https://github.com/user-attachments/assets/a37571b3-f4c5-43bc-a98e-a4f5ce808e1f



#### *** All PCB design materials and images are located in folder 2026_12_2Wheel_Balance_Robot_v1 2 ***
PCB layout used from Dr. Martins provided layout
