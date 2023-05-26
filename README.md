
# Garage doors and parking monitoring 1pp-garg-parking


Components:

- ESP32
- 2x distance sensor HC-SR04
- 1x 2-kanálový relé modul - 5VDC 5A Songle SRD-05VDC-SL-C
- 1x door contact

POZOR! Pro oboji je potreba 5V napajeni

## Wiring


| ESP32      | connected to      |
| ----------- | -----------------| 
| GPIO16      | RELAY IN1    |  1pp_garg_parking_door
| GPIO17      | RELAY IN2 |  1pp_garg_parking_door2
| GPIO32  | ULTRASOUND       | 1pp_garg_parking_dist1
| GPIO33  | ULTRASOUND       | 1pp_garg_parking_dist1
| GPIO14  | ULTRASOUND       | 1pp_garg_parking_dist2
| GPIO12  | ULTRASOUND       | 1pp_garg_parking_dist2
| GPIO15  | CONTACT        | 1pp_garg_parking_doorcontact


| DOOR CONTACT    | connected to     |
| ----------------| ---------- |
| [no color]  1   | ESP32 GND  |
| [no color]  2   | ESP32 GPIO15  |

| HC-SR04  Ultrasonic Distance Sensor 1  | connected to     |
| ----------------| ---------- |
| [white/yellow]  VCC   | ESP32 VCC 5V  |
| [red/orange]  trigger   | ESP32 GPIO32  |
| [green/red]  echo   | ESP32 GPIO33  |
| [blue/green]  GND   | ESP32 GND  |

| HC-SR04  Ultrasonic Distance Sensor 2  | connected to     |
| ----------------| ---------- |
| [white/yellow]  VCC   | ESP32 VCC 5V  |
| [red/orange]  trigger   | ESP32 GPIO14  |
| [green/red]  echo   | ESP32 GPIO12  |
| [blue/green]  GND   | ESP32 GND  |


| SONOFF RELAY    | connected to     |
| ----------------| ---------- |
| [no color]  GND   | ESP32 GND  |
| [no color]  IN1   | ESP32 GPIO16 RX |
| [no color]  IN2   | ESP32 GPIO17 TX |
| [no color]  VCC   | ESP32 VCC 5V  |


## Screenshots

![App Screenshot](https://github.com/jindrich296/sensor-temp-hum-CWT-TH03S-via-RS485/blob/main/IMG_2034.jpg)

![App Screenshot](https://github.com/jindrich296/sensor-temp-hum-CWT-TH03S-via-RS485/blob/main/IMG_2033.jpg)
