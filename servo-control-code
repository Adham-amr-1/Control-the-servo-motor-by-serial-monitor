#include <Servo.h>
int pos  = 0;
int led  = 2;
int serv = 3;
char data;
Servo myservo; 
void ledblink();
void setup() {
  // put your setup code here, to run once:
  pinMode(led,OUTPUT);
  myservo.attach(serv);
  Serial.begin(9600);
}

void loop() {
  // put your main code here, to run repeatedly:
  data = Serial.read();
  if (data == 'Z' || data == 'z' ){ //Z refers to zero position
    myservo.write(0);
   ledblink();
 }     
  else if (data == 'R' || data == 'r'){ //R refers to the right-angle
   myservo.write(90);
   ledblink();
   ledblink();

 }     
  else if (data =='c' || data == 'C' ){ // C refers to the cycle of servo
   myservo.write(180);
   ledblink();
   ledblink();
   ledblink();
 }     
}
void ledblink(){ //blink led
  digitalWrite(led,HIGH);
  delay(500);
  digitalWrite(led,LOW);
  delay(500);
}
