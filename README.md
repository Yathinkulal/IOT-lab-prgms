# IOT-lab-pgms<br>
1.ultrasonic<br>
const int trigPin = 12;<br>
const int echoPin = 14;<br>
<br>
//define sound velocity in cm/uS<br>
#define SOUND_VELOCITY 0.034<br>
#define CM_TO_INCH 0.393701<br>

long duration;<br>
float distanceCm;<br>
float distanceInch;<br>
<br>
void setup() {<br>
  Serial.begin(115200); // Starts the serial communication<br>
  pinMode(trigPin, OUTPUT); // Sets the trigPin as an Output<br>
  pinMode(echoPin, INPUT); // Sets the echoPin as an Input<br>
}<br>
<br>
void loop() {<br>
  // Clears the trigPin<br>
  digitalWrite(trigPin, LOW);<br>
  delayMicroseconds(2);<br>
  // Sets the trigPin on HIGH state for 10 micro seconds<br>
  digitalWrite(trigPin, HIGH);<br>
  delayMicroseconds(10);<br>
  digitalWrite(trigPin, LOW);<br>
  <br>
  // Reads the echoPin, returns the sound wave travel time in microseconds<br>
  duration = pulseIn(echoPin, HIGH);<br>
  <br>
  // Calculate the distance<br>
  distanceCm = duration * SOUND_VELOCITY/2;<br>
  <br>
  // Convert to inches<br>
  distanceInch = distanceCm * CM_TO_INCH;<br>
  <br>
  // Prints the distance on the Serial Monitor<br>
  Serial.print("Distance (cm): ");<br>
  Serial.println(distanceCm);<br>
  Serial.print("Distance (inch): ");<br>
  Serial.println(distanceInch);<br>
  <br>
  delay(1000);<br>
}<br>
