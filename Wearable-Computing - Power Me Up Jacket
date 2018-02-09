# Wearable-Computing - Power Me Up Jacket 
int led1 = 4; //Blue 
int led2 = 7; //Green 
int led3 = 10; //White
int led4 = 13; //Front red
const int Reed = 2;
//const int Reed2 =11;
//int Reedvalue2 = 0;
int Reedvalue = 0;
int fadeRate = 50;
boolean State = false; //determines the Led 


void setup() {
pinMode (led1, OUTPUT);
pinMode (led2, OUTPUT);
pinMode (led3, OUTPUT);
pinMode (led4, OUTPUT);
pinMode (Reed, INPUT); 
//pinMode (Reed2, INPUT);
Serial.begin(9600);
}

void fade(){
for (int fadeValue = 0 ; fadeValue <= 250; fadeValue += 10) {
analogWrite(led1, fadeValue);
analogWrite(led2, fadeValue);
analogWrite(led3, fadeValue);
analogWrite(led4, fadeValue);
delay(fadeRate);
digitalWrite(led1, HIGH);
digitalWrite(led2, HIGH);
digitalWrite(led3, HIGH);
digitalWrite(led4, HIGH);

}}

void fadeoff(){
for (int fadeValue = 250; fadeValue >= 0; fadeValue -= 10) {
analogWrite(led1, fadeValue);
analogWrite(led4, fadeValue);
analogWrite(led7, fadeValue);
analogWrite(led8, fadeValue);
delay(fadeRate);
}}

void loop() {
Reedvalue = digitalRead(Reed); 
//Reedvalue2 = digitalRead(Reed2); 
if(Reedvalue == HIGH){
if (State == false) {
fade();

}

else{
fadeoff();
}
State = !State;  // keep the state and switch variable
}}

//http://www.instructables.com/topics/How-to-use-a-boolean-in-Arduino/
//http://asil-arduino.blogspot.ca
