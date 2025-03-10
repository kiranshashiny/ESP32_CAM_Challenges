# ESP32_CAM_Challenges Faced on Mac OS  June 14th 2023

Interesting link from Drone Bot Workshop


https://dronebotworkshop.com/esp32-cam-intro/#:~:text=Open%20your%20Serial%20Monitor%2C%20making,on%20the%20ESP32%2DCAM%20module.


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/696cdae9-9b82-491e-9d08-37944da42733)


Troubleshooting tips.

- Connect the GPIO0 and the GND to upload code - or else it wont work.

- I have used an external 5V wall adapter to get this to work. Connecting from the FTDI 5V to Webcam was not successful.

- It only works with the 2.4 Ghz. I used JioFiber-24 and _EXT

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/769f3440-787b-4b3e-b436-d408df8b9668)

First, just check that the power supply is good, Connect a 5v and GND to the **bare** ESP32CAM, a small blip of flash light will / should be seen.
This indicates that the power supply is good.

During Arduino IDE Upload : Press the on-board RST button on the back side to start uploading -or else it wont work. If the connections are right, the onboard large LED will light up for just a flash. If it does not - then it's a problem - fix it first. 

After uploading - disconnect the GND to GPIO pin, and watch the Serial Monitor for messages.

- Use Arduino 2 IDE instead of Arduino 1.x.x IDE - has the " AI thinker in the Board Manager " 1.x.x does not have it.

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/89542c70-4497-4454-9a27-3997aa322fad)

- In order to over come the Code too big error  - then use the Arduino 2.x IDE.

- Use a separate 5V from wall adapter to power the ESP32 Webcam, or else I will get the "brown out time out error"

- The JioFiber 5G Wifi connection did not connect so I connected to the JioFiber-24 

The brown out condition is explained below :

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/06e617db-dbf3-423b-ab6d-511e7f636e3d)


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/e8a2e6bb-c67b-43a9-aad8-c83f2fef9022)



![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/5f118219-95e0-4d51-bf78-3bd1aa17280c)

Open the browser, and go. to http://192.168.29.117 to render the image.
Click on Start stream or Get Still to get the images.

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/ff996e04-71be-4915-b622-06e54ddcdbbb)

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/8ddf6fc9-43fa-4fd7-b401-94757cbc7d6b)


SUCCESS

dbconfig-common  is in /etc/dbconfig-common

user id for http://192.168.x.x:phpmyadmin is 
phpmyadmin  -> password is standard


Send data from webcam to Raspberry Pi -to render on the Rpi Server

https://randomnerdtutorials.com/esp32-cam-post-image-photo-server/#1-1


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/a04de772-d698-49e1-961c-adba92bbf04a)

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/cb4850a5-e21d-4934-90df-34721e0ebf40)

https://randomnerdtutorials.com/esp32-cam-post-image-photo-server/#1-1

##Problem: During the Upload - if you encounter, this error 

```
[E][camera.c:1113] camera_probe(): Detected camera not supported.
[E][camera.c:1379] esp_camera_init(): Camera probe failed with error 0x20004
```
![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/1dfeeb18-85ef-4573-a173-dc142cdd714e)

Ensure that you have set the camera model is set to AI_THINKER 

It would have been set to #define CAMERA_MODEL_WROVER_KIT // Has PSRAM

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/7050c4f9-7173-468c-a566-f3e9f8e59db2)


During successful upload, these were the messages on the Serial Monitor, and Arduino IDE status clip.
The default download speed of 460800 did not matter.

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/c61f9d32-908d-45dc-ba99-766d897945e3)


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/2ba44cd0-cc75-4649-aae6-f12e7f81275d)



Some important Installation locations on Mac OS

Documents/Arduino/hardware/espressif/esp32


screen /dev/cu.usbserial 115200 

Some how this did not work.


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/4c61de37-a621-45ee-a4f9-7754d7ff8b0e)



![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges_troubleshooting/assets/14288989/02f0343e-621e-4a10-a25a-70f17166c3d4)
