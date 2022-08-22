# internent-of things
1.https://wokwi.com/projects/333796636268429907

2.https://wokwi.com/projects/333797944251646547

3.tempature & humadity sensor<br>
https://wokwi.com/projects/334347223081943635

INFORMATION

https://arduinogetstarted.com/tutorials/arduino-temperature-humidity-sensor

4.ulaTRA SONIC

:https://wokwi.com/projects/334343126477963859

INFORMATION
https://howtomechatronics.com/tutorials/arduino/ultrasonic-sensor-hc-sr04/

5.PIR
https://wokwi.com/projects/334345672871379538

INFORMATION
https://create.arduino.cc/projecthub/biharilifehacker/arduino-with-pir-motion-sensor-fd540a

** 6.IR sensor**
https://wokwi.com/projects/334347798007775826

** 7.BLINK LED**
https://wokwi.com/projects/334432141665370707**

** 8.BUTTON LED**
https://wokwi.com/projects/334434511819375186

** 9.LED FADE**
https://wokwi.com/projects/334436844701745746

** 10.ULTRASONIC LED**

https://wokwi.com/projects/334440053872788052

** 11.SERVOMETER**
https://wokwi.com/projects/334976238758134354


** 12.SERVOMETER CONTROLLED BY POTENTIOMETER**

https://wokwi.com/projects/334977575166149202

** 13.BUTTON SERVOMETER**
https://wokwi.com/projects/334980038617203283

** 14.ULTRASONIC SERVOMETER**
https://wokwi.com/projects/334981244350628435

** 15.BUZZER**
https://wokwi.com/projects/335071080345502291

** 16.BUZZER WITH BUTTON**
https://wokwi.com/projects/335069682709037651

** 17.BUZZER WITH ULTRASONIC SENSOR**
https://wokwi.com/projects/335072529533108819

** 18.BUZZER WITH DIFFERENT SOUNDS**
https://wokwi.com/projects/335066652092662356

19.buzzer with led
https://wokwi.com/projects/335613483142873684

20.buzzer with ultrasonic for 20cm<br>
https://wokwi.com/projects/335613396042908243<br>

21.potentiometer<br>
https://wokwi.com/projects/335701896674148948<br>

22.potentiometer with led<br>
https://wokwi.com/projects/335703061675639379<br>

23.DHT22 temperature and humidity sensor<br>
 https://wokwi.com/projects/338147082096345683 <br>
 
 24.-DHT22+LCD(humidity sensor and temperature) <br>
https://wokwi.com/projects/338154081559249491 <br>
LAB LIST
1.https://wokwi.com/projects/338225981441442386 :-ESP32(LED/Buzzer)<br>
2.https://wokwi.com/projects/338770823644971603 :-Arduino(LED/BUZZER)<br>

3. https://wokwi.com/projects/338147082096345683 :-DHT22 ( humidity sensor and temperature).<br>

5. https://wokwi.com/projects/338154081559249491 :-DHT22+LCD(humidity sensor and temperature)<br>


**HARDWARE**
**IR SENSOR**
int ir=D5;
int led=D6; void setup() {
// put your setup code here, to run once:
pinMode(ir,INPUT);
pinMode(led,OUTPUT);
Serial.begin(9600);
}

void loop() {
// put your main code here, to run repeatedly:
int irvalue=digitalRead(ir);
if(irvalue==LOW)
{
Serial.println("LOW");
digitalWrite(led,HIGH);
}
else
{
Serial.println("HIGH");
digitalWrite(led,LOW);
}
delay(100);
}

image

Chassing LED
int pinsCount=7; // declaring the integer variable pinsCount
int pins[] = {D0,D1,D2,D3,D4,D5,D6}; // declaring the array pins[]

void setup() {
for (int i=0; i<pinsCount; i=i+1){ // counting the variable i from 0 to 9
pinMode(pins[i], OUTPUT); // initialising the pin at index i of the array of pins as OUTPUT
}
}
void loop() {
for (int i=0; i<pinsCount; i=i+1){ // chasing right
digitalWrite(pins[i], HIGH); // switching the LED at index i on
delay(100); // stopping the program for 100 milliseconds
digitalWrite(pins[i], LOW); // switching the LED at index i off
}
for (int i=pinsCount-1; i>0; i=i-1){ // chasing left (except the outer leds)
digitalWrite(pins[i], HIGH); // switching the LED at index i on
delay(100); // stopping the program for 100 milliseconds
digitalWrite(pins[i], LOW); // switching the LED at index i off

}
}

