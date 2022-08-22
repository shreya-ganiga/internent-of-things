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
![image](https://user-images.githubusercontent.com/98379636/185889633-7aaf0245-5ab3-48d3-907f-2725ad39544e.png)
 #include <Adafruit_Sensor.h>
    #include <DHT.h>;
    #define DHTPIN 13     // what pin we're connected to
    #define DHTTYPE DHT11   // DHT 22  (AM2302)
    DHT dht(DHTPIN, DHTTYPE); //// Initialize DHT sensor for normal 16mhz Arduino
    //Variables
    int chk;
    float hum;  //Stores humidity value
    float temp; //Stores temperature value
    void setup()
    {
      Serial.begin(9600);
      dht.begin();
    }
    void loop()
   {
       delay(2000);
       //Read data and store it to variables hum and temp
       hum = dht.readHumidity();
       temp= dht.readTemperature();
       //Print temp and humidity values to serial monitor
       Serial.print("Humidity: ");
       Serial.print(hum);
       Serial.print(" %, Temp: ");
       Serial.print(temp);
       Serial.println(" Celsius");
       delay(1000); //Delay 2 sec.
   }
   
   **IR SENSOR:-**
  **................**
int ir=D7;
int led=D6;
void setup() {
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
**ultra sonic:-**
**.....................**
const int trigPin = 13; //D7
   const int echoPin = 12; //D6

   long duration;
   float distanceCm;
   float distanceInch;

   void setup() {
           Serial.begin(9600); // Starting Serial Terminal
   }

   void loop() {
      long duration, inches, cm;
      pinMode(trigPin, OUTPUT);
      digitalWrite(trigPin, LOW);
      delayMicroseconds(2);
      digitalWrite(trigPin, HIGH);
      delayMicroseconds(10);
      digitalWrite(trigPin, LOW);
      pinMode(echoPin, INPUT);
      duration = pulseIn(echoPin, HIGH);
      inches = microsecondsToInches(duration);
      cm = microsecondsToCentimeters(duration);
      Serial.print(inches);
      Serial.print("in, ");
      Serial.print(cm);
      Serial.print("cm");
      Serial.println();
      delay(1000);
   }

   long microsecondsToInches(long microseconds) {
       return microseconds / 74 / 2;
   }

  long microsecondsToCentimeters(long microseconds) {
    return microseconds / 29 / 2;
   }
**RGB:-**
**................**
 int red = D1;
int green = D6;
int blue = D7;
//GROUND IS CONNECTED TO 3V
void setup() {
pinMode(red, OUTPUT);
pinMode(green, OUTPUT);
pinMode(blue, OUTPUT);

}

void loop() {
displayColor(0b100); //RED
delay(1000);
displayColor(0b010); //GREEN
delay(1000);
displayColor(0b001); //BLUE
delay(1000);
displayColor(0b101); //MAGENTA
delay(1000);
displayColor(0b011); //CYAN
delay(1000);
displayColor(0b110); //YELLOW
delay(1000);
displayColor(0b111); //WHITE
delay(1000);
}

void displayColor(byte color) {
digitalWrite(red, !bitRead(color, 2));
digitalWrite(green, !bitRead(color, 1));
digitalWrite(blue, !bitRead(color, 0));
}
**LDR:-**
**...................**
const int ldrPin=A0;

void setup() {
  // put your setup code here, to run once:
  Serial.begin(9600);
  pinMode(ldrPin,INPUT);

}

void loop() {
  // put your main code here, to run repeatedly:
  int rawData=analogRead(ldrPin);
  Serial.println(rawData);
  delay(1000);
}
LDR WITH LED:-
........................................
int ldr=A0;//Set A0(Analog Input) for LDR.
 int value=0;
 int led=D4;
 void setup() {
 Serial.begin(9600);
 pinMode(led,OUTPUT);
 }

 void loop() {
 value=analogRead(ldr);//Reads the Value of LDR(light).
 Serial.println("LDR value is :");//Prints the value of LDR to Serial Monitor.
 Serial.println(value);
 if(value<50)
   {
     digitalWrite(led,HIGH);//Makes the LED glow in Dark.
   }
   else
   {
     digitalWrite(led,LOW);//Turns the LED OFF in Light.
   }
   delay(1000);
 }
**flood monitoring system link:-**
https://theiotprojects.com/iot-based-flood-monitoring-system-using-nodemcu-thingspeak/


