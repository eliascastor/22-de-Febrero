# 22-de-Febrero
led rgb
int bt1=3;
int bt2=4;
int bt3=5;
int ledr=6;
int ledg=7;
int ledb=8;
bool e1;
bool e2;
bool e3;

void setup() {
  Serial.begin(9600);
  pinMode (bt1, INPUT_PULLUP);
  pinMode (bt2, INPUT_PULLUP);
  pinMode (bt3, INPUT_PULLUP);
  pinMode (ledr, OUTPUT);
  pinMode (ledg, OUTPUT);
  pinMode (ledb, OUTPUT);
  //

}

void loop() {
  e1=digitalRead(bt1);
  e2=digitalRead(bt2);
  e3=digitalRead(bt3);
 
 if(e1 && e2 && e3){
 digitalWrite(ledr, LOW);
 digitalWrite(ledg, LOW);
 digitalWrite(ledb, LOW);
}
if(!e1 && e2 && e3){
 digitalWrite(ledr, HIGH);
 digitalWrite(ledg, LOW);
 digitalWrite(ledb, LOW);
}
if(e1 && !e2 && e3){
 digitalWrite(ledr, LOW);
 digitalWrite(ledg, HIGH);
 digitalWrite(ledb, LOW);
}
if(e1 && e2 && !e3){
 digitalWrite(ledr, LOW);
 digitalWrite(ledg, LOW);
 digitalWrite(ledb, HIGH);
 }
 if(!e1 && !e2 && e3){
 digitalWrite(ledr, HIGH);
 digitalWrite(ledg, HIGH);
 digitalWrite(ledb, LOW);
}
if(!e1 && e2 && !e3){
 digitalWrite(ledr, HIGH);
 digitalWrite(ledg, LOW);
 digitalWrite(ledb, HIGH);
}
if(e1 && !e2 && !e3){
 digitalWrite(ledr, LOW);
 digitalWrite(ledg, HIGH);
 digitalWrite(ledb, HIGH);
}
if(!e1 && !e2 && !e3){
 digitalWrite(ledr, HIGH);
 digitalWrite(ledg, HIGH);
 digitalWrite(ledb, HIGH);
}
 
  

}
