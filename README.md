# Description
This is a step-by-step guide to connect the robotic vehicle (with computer such as Jetson Nano) to available network

## Steps
1. check the network address (ex: wlan0) on jetson nano via ifconfig on terminal
2. record the ip address. ex: 10.255.0.209
3. check network ip address on laptop via ipconfig on cmd (windows)
4. record the ip address. ex: 10.255.0.429
5. open putty on laptop
6. write ip address of the vehicle. ex: 10.255.0.209
7. login id and password for the vehicle
8. run the command, sudo mavproxy.py --master=/dev/ttyTHS1 --out=10.255.0.429:14550, the ip address is for laptop, here it is 10.255.0.429. Use THS1 for when jetson nano was connected to autopilot (durandal, pixhawk) via telemetry. Use ACM1 (ACM0) when the connection is via USB
