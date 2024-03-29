# FPGA__ESP8266__Car__Control
We used FPGA to control the action of motor and used the ESP8266 NodeMCU to send the control signal from web page.
<br>
## WiFi control module
We used the ESP8266 NodeMUC WiFi module and contructed the control interface with HTML code<br>
to control the electric car.<br>
<img src="https://github.com/tim8557/FPGA__ESP8266__Car__Control/blob/main/images/esp8266_nodemcu.jpg" width="200" ><br>

## User control interface
Here is the web page that we use to control the electic car.<br>
<br>
![image](https://github.com/tim8557/FPGA__ESP8266__Car__Control/blob/main/images/wifi_control_interface.JPG)<br>

## Use FPGA to control the motor
The pictire is the time sequence and state machine of FPGA. The sync_d0, sync_d1 and sync_d2<br>
are the signals from ESP8266. We use this three signals to make the motor action. For example, if the control<br>
signal is 3'b001, the motor will be acclerated. There are seven states in our project.<br>
<br>
**clk:** clock frequency of FPGA<br>
**rst:** reset signal<br>
**d0_sync:** the signal from ESP8226 to the syncornizer<br>
**d1_sync:** the signal from ESP8226 to the syncornizer<br>
**d2_sync:** the signal from ESP8226 to the syncornizer<br>
**state:** the state was used to control the action of motor.<br>
**pwm:** we used the duty cycle to control rotational speed of motor.<br>
**pwm2:** make the motor work at different rotational speed for turnig left or right.<br>
<br>
![image](https://github.com/tim8557/FPGA__ESP8266__Car__Control/blob/main/images/time_sequence.JPG)
<br>
We used L293D to control the direction of rotation.<br>
<br>
<img src="https://github.com/tim8557/FPGA__ESP8266__Car__Control/blob/main/images/l293d.jpg" width="100" ><br>

## Result
The seven-seg display can show the distance between the car and obstacle.<br>
<br>
<img src="https://github.com/tim8557/FPGA__ESP8266__Car__Control/blob/main/images/result_car_control.jpg" width="300" ><br>
<br>
### First demo vedio
In this vedio, the car can stop when the distance is smaller than 25 cm between car and obstacle.<br> 
https://www.youtube.com/watch?v=zgS9nRPCUMc<br>
<br>
### Second demo vedio
In this vedio, the led light become green when the direction of rotation is forward. The light become <br> 
red when the direction of rotation is reverse. The color of light can mention us the direction of rotation<br>
when we stop the car.<br>
https://www.youtube.com/watch?v=whfVSmhwwZ0
