# Control-servo-motor-using-PWM.#include<Servo.h>

int servoPin=9;
int servoPos=165;
Servo myServo;

void setup() {
  // put your setup code here, to run once:
Serial.begin(9600);
myServo.attach(servoPin);
}

void loop() {
  Serial.println("What Angle for the servo? ");
  while (Serial.available()==0) {
  }
  servoPos=Serial.parseInt();
myServo.write(servoPos);
}

