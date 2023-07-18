# Tiel-Lilygo-SlimeVR-Tracker
SlimeVR Trackers using LilyGo TTGO T-OI with 16340 Battery
![IMG_20230718_155817](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/9ed07990-4b93-42fa-814f-f4f49336b192)


## Pros
1. Hotswappable
2. Easier to make; Less stuff to solder
3. Small form factor
4. Simplifies parts buying
   
## Cons
1. Can't be flashed through web flasher. Requires firmware modification
2. 2-3$ more expensive than wemos d1
3. Less range than wemos d1 since it is using a tinier ceramic antenna.
4. Requires a 3d printed case
5. Generally lower capacity. 800mah (8 hours) is the highest capacity battery I can find.

## Parts list:
The links are only an example. If you can find a cheaper one on another
store then go with that.

### Main Trackers
1. [Lilygo T-OI](https://www.aliexpress.com/item/4000429611680.html)
2. [BMI 160](https://www.aliexpress.com/item/4000052683444.html)
   Suggested stores: Mwss, Wansai, Tenstar, Aixterm
3. 16340 Battery
   The highest capacity legitimate battery I can find is 800mah.

   WARNING: If you find a cheap one advertising above 1000mah it is most likely fake.
   Like this one that boasts 2800 but actually only has 350mah (3.5 Hours) when tested. Buyer beware
   
   ![Screenshot 2023-07-18 195823](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/8d8f4c03-a82a-4128-bb1a-d837966f9940)

5. Any wire. 26-28 awg

### Extension Trackers
1. Grove 4 pin cable male.
   Suggested lengths:
   Ankle-Foot extension: 20cm
   Chest-Waist extension: 30cm
2. [BMI 160](https://www.aliexpress.com/item/4000052683444.html)


### Accessories
1. 1.5 Inch garter for straps or any 1.5 inch straps if you wont use the 3d printed buckles
2. [18650 Charger](https://www.aliexpress.com/item/1005005191646987.html)
3. (Optional) [Gopro Chest Mount](https://www.aliexpress.com/item/1005005058530956.html)
   For more stable chest trackers

## 3d Printing
All parts to be printed without supports

1. Buckles and Cases both Main and Extension can be printed at these settings for 0.4mm nozzle
   
   Line width: 0.6
   
   Layer height: 0.32

3. The switch should be printed at this setting

   Line width: 0.3
   
   Layer height: 0.2

## Assembly

## Main tracker
### What you'll need:
![M01](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/99fc61e3-98ec-4120-831d-bedba1175fc2)
1. Lilygo Board
2. BMI160
3. 3pcs of wire. 2 for ground. 1 for power
4. 3d printed case and switch
5. 16340 battery
6. Header pin cut to 2 pins

### 1. Strip the wires
![M02](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/f688a724-03f6-448d-bf4b-7ab40d334eb2)

### 2. Twist the two wires meant for ground
![M03](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/4656cbd7-ff58-40b0-835f-9b7817ae45ff)

### 3. Connect the wires to the IMU
Wire for power goes to 3V3
Wire for ground goes to GND and SAO
![M04](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/f04bbdb7-768f-4458-991c-5322d3def678)


### 4. Solder the header pins to the Lilygo Board
It goes on the holes labeled 4 & 5
![M05](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/eaa78e4f-1e8d-43c6-b4a4-d7afed5b4f45)

### 5. Solder the Ground and Power to the Lilygo Board
Wire for power connects to the hole labeled 3V3

Wire for ground connects to the hole labeled GND

![M06](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/96ba692b-da10-4858-8e6c-0dc852c18c96)

### 6. Solder SCL and SDA to the header pins
SCL goes to the pin labeled 5

SDA goes to the pin labeled 4
![M07](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/e54a11f3-8426-4197-aa37-0c86d0b157ee)

### 7. Insert to case
![M08](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/5fc4bd0a-868b-4f4e-a0ea-aecafd08cea6)

### 8. Done
![M09](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/5c3087e7-8bd2-453c-9824-54c4d381b2df)

## Extension Tracker
### What you'll need:
![E01](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/e8a4975d-177d-464e-a6a4-059c821aec5b)
1. BMI160
2. Grove 4 pin
3. 3d printed extension case

### 1. Cut one end of the cable and strip the wire
![E02](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/4beb9f7a-d5a7-455b-a000-3d86078341b6)

### 2. Connect to IMU
![E03](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/30841c3d-564a-4c8a-97c8-533f5aac9e9d)
From this we know that:
1. Ground is the yellow wire
2. 3V3 is the white wire
3. SDA is the red wire (The board's label is different but it really is SDA in the firmware)
4. SCL is the black wire

Connect the appropriate wires to the IMU
![E04](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/5a01d2df-f06a-4c60-bf2e-4ad58e38ac92)

### 3. Put inside the extension case & Done
![E05](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/42b26f68-c84d-4fb8-adb6-d85c98628e5c)

## Flashing the firmware
First, Setup the environment. Follow this guide on [SlimeVR documentation](https://docs.slimevr.dev/firmware/setup-and-install.html)

### 1. Modify firmware files
In platformio.ini Set your wifi credentials
![01](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/01c73d55-0cd1-4ccc-b0b2-1e039a661795)


In \src\batterymonitor.h set the define of batteryADCMultiplier to:

#define batteryADCMultiplier 0.0072271914132379
![02](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/ab0d17ff-be26-47d2-8fbe-3d5c9de68efd)


In defines.h
Set IMU to BMI160

Set Secondary imu to BMI160

Set board to WemosD1

Set secondary rotation to 90 (For foot extension trackers only)

![03](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/4096bd81-87d5-44ec-9594-151d0cfd7e2d)

### 2. Build and Flash
Connect the board through micro USB. Then turn on the switch
![07](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/4499b1be-06e4-4a7c-a75a-277ae6272e7c)

Click the build button [1] on the lower left of VSCode

Click the upload button [2]

![04](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/466c29d2-9c43-4b53-bf8e-399a60890c01)
Wait for the firmware flash to finish

### 3. Done
Enjoy your tracker! It should connect to the slime server

![06](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/7393e78e-c813-411d-aacd-e424d2519b7e)
![IMG_20230718_155817](https://github.com/RDTiel/Tiel-Lilygo-SlimeVR-Tracker/assets/139855889/32f8c18b-7265-4835-b81a-c9cc74e7ec99)

## BMI 160 calibration
[Youtube Video](https://youtu.be/bCKwmGeUpok)
Note; This was done like this to make it visible in the camera. You should do it in a more stable way (On a table).

## Credits
Extension case is from [Arcturus](https://github.com/Lixulia/Arcturus/tree/main)

Buckle is from Printables [HD_Creator](https://www.printables.com/@HD_Creator) In printables


