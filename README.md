# Virtual-sensor-in-Unity3D

## Motivation
As the conventional sensor data obtain typicall required to recruit the real human to conduct the designated actitity to generate the sensor signal and collect the dataset, the cost of whole data obtain process is high and the trained machine-learning system is low-flexibility. To better create a flexible application which is able to fit the end-user's situation/requirement, minimizing the collection of sensor data will contribute to a low-cost and high-flexible system.  

## Method
As the accessible 3D reconstructed human motions are increased, measuring the 3D virutal human motion is able to simulate the way occuring in the real-world (e.g., using a physical sensor to detect the human motion) and generated the virtual sythetic signal.

## Environment 
Unity3D Platform with its Physics Engine.

## Realizing a virtual sensor design
### 1. Import a 3D motion in Unity
<img src="https://github.com/NickXia815/Virtual-sensor-in-Unity3D/blob/Image/avatar.png" width="300" height="280" />
Create an Animation Controller (You can refer to the method of realize an animation in Unity)

### 2. Virtual IMU (Inertial Measurement Unit) 
The IMU sensor normally detects the kinematic data. With it attached to the human body, the IMU can sense the acceleration, angular velocity and magnetic. In Unity3D, a virtual IMU can be designed to output the accelertion and angular velocity. Furthermore, the euler angle and quaternion can be output. 

#### a. Create a cube model and put it as the child node under the desired body limb (as in the real world, wearing a sensor)
<img src="https://github.com/NickXia815/Virtual-sensor-in-Unity3D/blob/Image/attach_sensor_module.png" width="350" height="220" />

#### b. Attach the script "virtual_IMU.cs" to the created cube model, setting the key parameters
<img src="https://github.com/NickXia815/Virtual-sensor-in-Unity3D/blob/Image/parametersetting.jpg" width="350" height="250" />

#### c. Play the Animation and recording the data. After that, the data will be stored in the designated folder.
<img src="https://github.com/NickXia815/Virtual-sensor-in-Unity3D/blob/Image/savedfile.jpg" width="400" height="250" />

#### d. Check the data (e.g., acceleration of walking from Right Upper Leg)
<img src="https://github.com/NickXia815/Virtual-sensor-in-Unity3D/blob/Image/result.jpg" width="400" height="250" />

### Infrared distance sensor 
