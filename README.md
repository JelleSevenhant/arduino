# arduino
project voor school
verkeerslicht

int  au=0;
byte drukknop=10;
byte groen1=1;
byte groen2=2;
byte groen3=3;
byte oranje1=4;
byte oranje2=5;
byte oranje3=6;
byte rood1=7;
byte rood2=8;
byte rood3=9;
void setup() {
pinMode(groen1,OUTPUT);
pinMode(groen2,OUTPUT);
pinMode(groen3,OUTPUT);

pinMode(oranje1,OUTPUT);
pinMode(oranje2,OUTPUT);
pinMode(oranje3,OUTPUT);

pinMode(rood1,OUTPUT);
pinMode(rood2,OUTPUT);
pinMode(rood3,OUTPUT);
pinMode(drukknop,INPUT);
}
void loop(){ 



  while(au == 1){
digitalWrite(groen1,HIGH);
digitalWrite(groen2,HIGH);
digitalWrite(groen3,HIGH);

  if(digitalRead(drukknop)){
    delay(300);
    au=0;
  }
delay(3000);

digitalWrite(groen1,LOW);
digitalWrite(groen2,LOW);
digitalWrite(groen3,LOW); 

digitalWrite(oranje1,HIGH);
digitalWrite(oranje2,HIGH);
digitalWrite(oranje3,HIGH);
  
  if(digitalRead(drukknop)){
    delay(300);
    au=0;
  }
delay(500);

digitalWrite(oranje1,LOW);
digitalWrite(oranje2,LOW);
digitalWrite(oranje3,LOW);

digitalWrite(rood1,HIGH);
digitalWrite(rood2,HIGH);
digitalWrite(rood3,HIGH);

  if(digitalRead(drukknop)){
    delay(300);
    au=0;
  }
delay(3000);
 
digitalWrite(rood1,LOW);
digitalWrite(rood2,LOW);
digitalWrite(rood3,LOW);
  
  if(digitalRead(drukknop)){
    delay(300);
    au=0;
  }
  }
while(au == 0){
 digitalWrite(groen1,LOW);
 digitalWrite(groen2,LOW);
 digitalWrite(groen3,LOW);

 digitalWrite(oranje1,LOW);
 digitalWrite(oranje2,LOW);
 digitalWrite(oranje3,LOW);

 digitalWrite(rood1,LOW);
 digitalWrite(rood2,LOW);
 digitalWrite(rood3,LOW);
 
if (digitalRead(drukknop)){
  delay(300);
  au=1;
}
}
}
