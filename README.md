# DC-Motor-Speed-control
Controlling the speed of a DC motor is generally achieved by adjusting the voltage supplied to the armature, modifying the magnetic field flux, or using Pulse Width Modulation (PWM)

int potentiometer = A0;
int motorPin = 3;

void setup()
{
  Serial.begin(9600);
  pinMode(potentiometer, INPUT);
}

void loop()
{
  int value = analogRead(potentiometer)/4;
  Serial.println(value);
  analogWrite(motorPin, value);
}
