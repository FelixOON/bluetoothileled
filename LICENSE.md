int data;
int led1=11;
int led2=12;
int led3=13;
void setup(){
  Serial.begin(9600);
    pinMode(led1,OUTPUT); 
    pinMode(led2,OUTPUT);
    pinMode(led3,OUTPUT);
}
  void loop(){
    if(Serial.available())
    {
      int data=Serial.read();
      delay(100);
      if(data=='1')  
    digitalWrite(led1,HIGH); 
    if(data=='2')
      digitalWrite(led1,LOW); 
       if(data=='3')  
    digitalWrite(led2,HIGH); 
    if(data=='4')
      digitalWrite(led2,LOW); 
       if(data=='5')  
    digitalWrite(led3,HIGH); 
    if(data=='6')
      digitalWrite(led3,LOW); 
      delay(100);
    }
  }
