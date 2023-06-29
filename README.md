# ESP32_CAM_Challenges Faced on Mac OS  June 14th 2023


Troubleshooting tips.

Connect the GPIO0 and the GND to upload code - or else it wont work.

During Arduino IDE Upload : Press the on-board RST button on the back side to start uploading -or else it wont work.

Use Arduino 2 IDE instead of Arduino 1.x.x IDE - has the " AI thinker in the Board Manager " 1.x.x does not have it.

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/89542c70-4497-4454-9a27-3997aa322fad)

In order to over come the Code too big - then use the Arduino 2.x IDE.

Use a separate 5V from wall adapter to power the ESP32 Webcam, or else I will get the "brown out time out error"

The JioFiber 5G did not connect so I connected to the JioFiber-24 


![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/e8a2e6bb-c67b-43a9-aad8-c83f2fef9022)



![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/5f118219-95e0-4d51-bf78-3bd1aa17280c)

Open the browser, and go. to http://192.168.29.117 to render the image.
Click on Start stream or Get Still to get the images.

![image](https://github.com/kiranshashiny/ESP32_CAM_Challenges/assets/14288989/ff996e04-71be-4915-b622-06e54ddcdbbb)



SUCCESS
