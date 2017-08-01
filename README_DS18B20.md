# *DS18B20 Sensor*
## Part I. General Overview
### What is the DS18B20?

  * 1-Wire Digital Thermometer
  * Measures Temperatures from -55°C to +125°C
  * Must be used with a pull up resistor with a value of around 4.7 kΩ
  * Power supply range: 3.0 V to 5.5 V
  * Requires only 1 port pin for communication

### Datasheet
[DS18B20 Datasheet](https://github.com/charihara/Experimental_Sensors/blob/master/Datasheets/DS18B20_Data_Sheet.pdf)

### Connection Images
![image of DS18B20 connection](https://github.com/charihara/Experimental_Sensors/blob/master/Images/DS18B20_Connection.JPG)

### Working Logic / Functionality
#### Output

  * Thermometer resolution is user-selectable from 9 to 12 bits
  * Converts temperatues to 12-bit digital word in 750 ms
  * 

## Part II. Waggle Specific
### Application
#### How does the sensor work with Photon and P I/O Cloud?
##### (link to event page on particle.io)
##### (explain how the data is displayed as a log -- link to log page on particle.io)
### Source Code from particle.io

```C 
int rainPin = A0;

void setup() {
    
  pinMode(rainPin, INPUT);

}

void loop() {
 // read the input on analog pin 0:
  int sensorValue = analogRead(rainPin);
  Particle.publish("YL-69", String(sensorValue), PRIVATE);
  delay(60000);

}
```
   
### Particle Data Interface with Beehive dev
### Waggle-space ID
### Data Structure
