# Internet-of-things
1. Servomotor https://wokwi.com/projects/334977496186356308  <br>
***************************************************************************
2.LiquidCrystal LCD https://wokwi.com/projects/333825443765420627  <br>
*****************************************************************************
3. 3 LED traffic signal https://wokwi.com/projects/335617053248455252 <br>
*****************************************************************************
Traffic signal https://wokwi.com/projects/334975793262232148  <br>
 *****************************************************************************
4.Servomotor for statement https://wokwi.com/projects/334977496186356308<br>
*****************************************************************************
5.RGB https://wokwi.com/projects/333804541306733140  <br>
******************************************************************************
6.Servomotor with Potentiometer https://wokwi.com/projects/334981720686199378  <br>
***********************************************************************************
7.Buzzer https://wokwi.com/projects/335065147784561235 <br>
**************************************************************************************
8. Buzzer with pushbutton https://wokwi.com/projects/335066798676247122 <br>
*****************************************************************************************
9. Ultrasonic https://wokwi.com/projects/335068638604165715  <br>
******************************************************************************************
Ultrasonic with if statement https://wokwi.com/projects/335071626494214739 <br>
 *****************************************************************************************
https://wokwi.com/projects/335068638604165715<br>
 ****************************************************************************************
https://wokwi.com/projects/335072348261581395 <br>
 ***************************************************************************************
10. Ultrasonic with buzzer https://wokwi.com/projects/335073764052042322 <br>
*****************************************************************************************
11. LED https://wokwi.com/projects/335610079960105556 <br>
*******************************************************************************************
12. Ultrasonic sensor,buzzer,LED https://wokwi.com/projects/335612012397593172  <br>
*******************************************************************************************
13.Servomotor with buzzer https://wokwi.com/projects/335635909331386963 <br>
************************************************************************************************
14. Buzzer with LED and pushbutton https://wokwi.com/projects/335699245817397844 <br> 
*************************************************************************************************
15. Potentiometer with LED https://wokwi.com/projects/335700972632277587 <br>
************************************************************************************************************
16. Sensor Buzzer: https://wokwi.com/projects/334433831716127314<br>
********************************************************************************************************************
17.Temperature and Humidity: https://wokwi.com/projects/334346231606149714<br>
*********************************************************************************************************
temperature humidity sensor
https://wokwi.com/projects/334344785890378322
****************************************************************************************************************************
18.Servo motor controlled by push button:
https://wokwi.com/projects/334980736128909908
******************************************************************************************************************************
19.LED Chaser<br>
https://wokwi.com/projects/340775764469219922 
**************************************************************************************************************************
https://wokwi.com/projects/335071463215202900 - UltraSonic Sensor(extra)<br>
https://wokwi.com/projects/335073264458007124 - Buzzer + UltraSonic Sensor<br>
https://wokwi.com/projects/335075055329346132 - Buzzer + UltraSonic Sensor(Varying Instensity)<br>
https://wokwi.com/projects/335698029159907924 - Buzzer + Ultrasonic Sensor + LED<br>
https://wokwi.com/projects/335701186493547091 - Potentiometer + LED<br>
https://wokwi.com/projects/337602684471214674 - DHT22(Humidity and Temperature sensor)<br>
https://wokwi.com/projects/337604296859189842 - DHT22 + LCD(Humidity and Temperature sensor)<br>
https://wokwi.com/projects/340775764469219922 - LED_CHASER<br>
https://wokwi.com/projects/340776572602548818 - LDR<br>
https://wokwi.com/projects/340776926585029204 - LDR_LED<br>
https://wokwi.com/projects/340779619162522195 - IR_LED<br>

ESP32<br>
https://wokwi.com/projects/336966830711112275 - LED<br>
https://wokwi.com/projects/336967978479256147 - 3 LED<br>
https://wokwi.com/projects/340880463446934098 - RGB<br>
https://wokwi.com/projects/340882358612787796 - LCD<br>
https://wokwi.com/projects/340886369600537172 - Servo Motor + Pushbutton<br>
https://wokwi.com/projects/340888468071645780 - Servo Motor + Sliding Potentiometer<br>
https://wokwi.com/projects/340890155914101331 - Buzzer + Pushbutton_<br>
https://wokwi.com/projects/340890489300451922 - Buzzer + UltraSonic Sensor<br>
https://wokwi.com/projects/340890896679567955 - Potentiometer + LED<br>
https://wokwi.com/projects/340892440485429842 - DHT22<br>
https://wokwi.com/projects/340893919446303316 - LED CHASER<br>
https://wokwi.com/projects/340936317213868626 - LDR<br>
https://wokwi.com/projects/340936847717827156 - LDR + LED<br>
****************************************************************************************************************************

int led = 6;
int sound_digital = 7;
int sound_analog = A0;

void setup(){
  Serial.begin(9600);
  pinMode(led, OUTPUT);
  pinMode(sound_digital, INPUT);  
}

void loop(){
  int val_digital = digitalRead(sound_digital);
  int val_analog = analogRead(sound_analog);

  Serial.print(val_analog);
  Serial.print("\t");
  Serial.println(val_digital);

  if (val_digital == HIGH)
  {
    digitalWrite (led, HIGH);
    delay(3000);
    }
  else
  {
    digitalWrite (led, LOW);
    }
}
********************************************************************************************************************************************
1. Seven segment LED display example: Counter Reference : https://wokwi.com/arduino/libraries/SevSeg/SevSeg_Counter <br>
2. Analog Joystick with two axes (horizontal/vertical) and an integrated push button. Etch-a-sketch - A simple drawing game using a MAX7219 LED Dot Matrix Reference: https://wokwi.com/projects/296234816685212169
3. DHT22 on the ESP32 Reference: https://wokwi.com/projects/322410731508073042
4. Display distance on LCD screen with buzzer and LED  Reference 1: https://wokwi.com/projects/290056311044833800 Reference2: https://wokwi.com/projects/290043622233997832
5. Electronic Safe, powered by an Arduino Uno. Reference: https://wokwi.com/arduino/libraries/demo/electronic-safe
6. Arduino LED Graph Bar - Move the potentiometer knob to control the LEDs Reference:  https://wokwi.com/projects/309829489359061570
