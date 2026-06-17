uAnti Sleeper Alarm System for Drivers

Overview

This project is designed to improve driver safety by detecting drowsiness using Arduino Nano and IR sensor.

Problem Statement

Driver drowsiness is one of the major causes of road accidents. This project helps reduce accidents by alerting the driver when signs of sleep are detected.

Components Used

- Arduino Nano
- IR Sensor
- Buzzer
- Relay Module
- Connecting Wires

Features

- Eye detection
- Sleep alert system
- Safety relay activation

Applications

- Cars
- Trucks
- Long distance driving

Code of This Project

<arduino.h>
void setup()
{
pinMode(SENSE, INPUT); // Attach the Eye Blink Sensor signal pin 
pinMode(LED_BUILTIN, OUTPUT); // 13+ // Buzzer Attached 
}
void loop()
{
if(digitalRead(SENSE))
{
 digitalWrite(LED_BUILTIN, LOW);

}
else
{
  delay (2000);
  if(digitalRead(SENSE))
  {
 digitalWrite(LED_BUILTIN, LOW);
 
}
  else
  digitalWrite(LED_BUILTIN, HIGH);  
  
  }
}
