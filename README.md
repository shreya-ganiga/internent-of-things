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
LAB LIST<br>
1.https://wokwi.com/projects/338225981441442386 :-ESP32(LED/Buzzer)<br>
2.https://wokwi.com/projects/338770823644971603 :-Arduino(LED/BUZZER)<br>

3. https://wokwi.com/projects/338147082096345683 :-DHT22 ( humidity sensor and temperature).<br>

5. https://wokwi.com/projects/338154081559249491 :-DHT22+LCD(humidity sensor and temperature)<br>


**HARDWARE**
**IR SENSOR**
int ir=D5;<br>
int led=D6; void setup() {<br>
// put your setup code here, to run once:<br>
pinMode(ir,INPUT);<br>
pinMode(led,OUTPUT);<br>
Serial.begin(9600);<br>
}<br>

void loop() {<br>
// put your main code here, to run repeatedly:<br>
int irvalue=digitalRead(ir);<br>
if(irvalue==LOW)<br>
{<br>
Serial.println("LOW");<br>
digitalWrite(led,HIGH);<br>
}<br>
else<br>
{<br>
Serial.println("HIGH");<br>
digitalWrite(led,LOW);<br>
}<br>
delay(100);<br>
}<br>

image

Chassing LED<br>
int pinsCount=7; // declaring the integer variable pinsCount<br>
int pins[] = {D0,D1,D2,D3,D4,D5,D6}; // declaring the array pins[]<br>

void setup() {<br>
for (int i=0; i<pinsCount; i=i+1){ // counting the variable i from 0 to 9<br>
pinMode(pins[i], OUTPUT); // initialising the pin at index i of the array of pins as OUTPUT<br>
}<br>
}<br>
void loop() {<br>
for (int i=0; i<pinsCount; i=i+1){ // chasing right<br>
digitalWrite(pins[i], HIGH); // switching the LED at index i on<br>
delay(100); // stopping the program for 100 milliseconds<br>
digitalWrite(pins[i], LOW); // switching the LED at index i off<br>
}<br>
for (int i=pinsCount-1; i>0; i=i-1){ // chasing left (except the outer leds)<br>
digitalWrite(pins[i], HIGH); // switching the LED at index i on<br>
delay(100); // stopping the program for 100 milliseconds<br>
digitalWrite(pins[i], LOW); // switching the LED at index i off<br>

}<br>
}<br>
**LDR**
![image](https://user-images.githubusercontent.com/98379636/185889633-7aaf0245-5ab3-48d3-907f-2725ad39544e.png)<br>
**DHT11**<br>
 #include <Adafruit_Sensor.h><br>
    #include <DHT.h>;<br>
    #define DHTPIN 13     // what pin we're connected to<br>
    #define DHTTYPE DHT11   // DHT 22  (AM2302)<br>
    DHT dht(DHTPIN, DHTTYPE); //// Initialize DHT sensor for normal 16mhz Arduino<br>
    //Variables<br>
    int chk;<br>
    float hum;  //Stores humidity value<br>
    float temp; //Stores temperature value<br>
    void setup()<br>
    {<br>
      Serial.begin(9600);<br>
      dht.begin();<br>
    }<br>
    void loop()<br>
   {<br>
       delay(2000);<br>
       //Read data and store it to variables hum and temp<br>
       hum = dht.readHumidity();<br>
       temp= dht.readTemperature();<br>
       //Print temp and humidity values to serial monitor<br>
       Serial.print("Humidity: ");<br>
       Serial.print(hum);<br>
       Serial.print(" %, Temp: ");<br>
       Serial.print(temp);<br>
       Serial.println(" Celsius");<br>
       delay(1000); //Delay 2 sec.<br>
   }<br>
   
   **IR SENSOR:-**<br>
  **................**<br>
int ir=D7;<br>
int led=D6;<br>
void setup() {<br>
  // put your setup code here, to run once:<br>
  pinMode(ir,INPUT);<br>
    pinMode(led,OUTPUT);<br>
    Serial.begin(9600);<br>
    
}<br>

void loop() {<br>
  // put your main code here, to run repeatedly:<br>
  int irvalue=digitalRead(ir);<br>
  if(irvalue==LOW)<br>
  {<br>
    Serial.println("LOW");<br>
    digitalWrite(led,HIGH);<br>
  }<br>
  else<br>
  {<br>
    Serial.println("HIGH");<br>
    digitalWrite(led,LOW);<br>
  }<br>
delay(100);<br>
}<br>
**ultra sonic:-**<br>
**.....................**<br>
const int trigPin = 13; //D7<br>
   const int echoPin = 12; //D6<br>
   long duration;<br>
   float distanceCm;<br>
   float distanceInch;<br>

   void setup() {<br>
           Serial.begin(9600); // Starting Serial Terminal<br>
   }<br>

   void loop() {<br>
      long duration, inches, cm;<br>
      pinMode(trigPin, OUTPUT);<br>
      digitalWrite(trigPin, LOW);<br>
      delayMicroseconds(2);<br>
      digitalWrite(trigPin, HIGH);<br>
      delayMicroseconds(10);<br>
      digitalWrite(trigPin, LOW);<br>
      pinMode(echoPin, INPUT);<br>
      duration = pulseIn(echoPin, HIGH);<br>
      inches = microsecondsToInches(duration);<br>
      cm = microsecondsToCentimeters(duration);<br>
      Serial.print(inches);<br>
      Serial.print("in, ");<br>
      Serial.print(cm);<br>
      Serial.print("cm");<br>
      Serial.println();<br>
      delay(1000);<br><br>
   }<br>

   long microsecondsToInches(long microseconds) {<br><br>
       return microseconds / 74 / 2;<br>
   }<br>

  long microsecondsToCentimeters(long microseconds) {<br>
    return microseconds / 29 / 2;<br>
   }<br>
**RGB:-**<br>
**................**<br>
 int red = D1;<br><br>
int green = D6;<br>
int blue = D7;<br>
//GROUND IS CONNECTED TO 3V<br>
void setup() {<br>
pinMode(red, OUTPUT);<br>
pinMode(green, OUTPUT);<br>
pinMode(blue, OUTPUT);<br>

}<br>

void loop() {<br>
displayColor(0b100); //RED<br>
delay(1000);<br>
displayColor(0b010); //GREEN<br>
delay(1000);<br>
displayColor(0b001); //BLUE<br>
delay(1000);<br>
displayColor(0b101); //MAGENTA<br>
delay(1000);<br>
displayColor(0b011); //CYAN<br>
delay(1000);<br>
displayColor(0b110); //YELLOW<br>
delay(1000);<br>
displayColor(0b111); //WHITE<br>
delay(1000);<br>
}

void displayColor(byte color) {<br>
digitalWrite(red, !bitRead(color, 2));<br>
digitalWrite(green, !bitRead(color, 1));<br>
digitalWrite(blue, !bitRead(color, 0));<br>
}<br>
**LDR:-**<br>
**...................**<br>
const int ldrPin=A0;<br>

void setup() {<br>
  // put your setup code here, to run once:<br>
  Serial.begin(9600);<br>
  pinMode(ldrPin,INPUT);<br>

}<br>

void loop() {<br>
  // put your main code here, to run repeatedly:<br>
  int rawData=analogRead(ldrPin);<br>
  Serial.println(rawData);<br>
  delay(1000);<br>
}<br>
LDR WITH LED:-<br>
........................................<br>
int ldr=A0;//Set A0(Analog Input) for LDR.<br>
 int value=0;<br>
 int led=D4;<br>
 void setup() {<br>
 Serial.begin(9600);<br>
 pinMode(led,OUTPUT);<br>
 }<br>

 void loop() {<br>
 value=analogRead(ldr);//Reads the Value of LDR(light).<br>
 Serial.println("LDR value is :");//Prints the value of LDR to Serial Monitor.<br>
 Serial.println(value);<br>
 if(value<50)<br>
   {<br>
     digitalWrite(led,HIGH);//Makes the LED glow in Dark.<br>
   }<br>
   else<br>
   {<br>
     digitalWrite(led,LOW);//Turns the LED OFF in Light.<br>
   }<br>
   delay(1000);<br>
 }<br>
**flood monitoring system link:-**<br>
https://theiotprojects.com/iot-based-flood-monitoring-system-using-nodemcu-thingsp<br>
wifi<br>
https://wokwi.com/projects/321525495180034642<br>

** Seven segment LED display example**<br>
https://wokwi.com/projects/342585434329580116<br>


