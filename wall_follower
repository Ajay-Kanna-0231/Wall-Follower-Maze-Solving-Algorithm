void setup()
{
  pinMode(12, OUTPUT);
  pinMode(2,OUTPUT);
  pinMode(4,INPUT);
  pinMode(13, OUTPUT);
  pinMode(3,OUTPUT);
  pinMode(5,INPUT);
  pinMode(6,OUTPUT);
  pinMode(7,INPUT);
  Serial.begin(9600);
}

void loop()
{
long dur;
long dis;
long tocm;
  
digitalWrite(2,LOW);
delayMicroseconds(2);
digitalWrite(2,HIGH);
delayMicroseconds(10);
digitalWrite(2,LOW);
dur=pulseIn(4,HIGH);
Serial.println(dur);
tocm=microsecondsToCentimeters(dur);
  
long dur2;
long dis2;
long tocm2;
  
digitalWrite(3,LOW);
delayMicroseconds(2);
digitalWrite(3,HIGH);
delayMicroseconds(10);
digitalWrite(3,LOW);
dur2=pulseIn(5,HIGH);
Serial.println(dur2);
tocm2=microsecondsToCentimeters(dur2);
  
long dur3;
long dis3;
long tocm3;
int right;
int left;
  
digitalWrite(6,LOW);
delayMicroseconds(2);
digitalWrite(6,HIGH);
delayMicroseconds(10);
digitalWrite(6,LOW);
dur3=pulseIn(7,HIGH);
Serial.println(dur3);
tocm3=microsecondsToCentimeters(dur3);
  
  
if(tocm3>=150 and tocm2>=150 and tocm>=150){
  if(right > 0){
    digitalWrite(12,HIGH);
    digitalWrite(13,LOW);
  }
  else if(left > 0){
    digitalWrite(13,HIGH);
    digitalWrite(12,LOW);
   }
 }    
 
  
else{  
 
 right = 0;
 left = 0;
  
 if(tocm3>=150){
   
  if(tocm<=150 or tocm2<=150)
  {
    digitalWrite(12,HIGH);
    if(tocm<=150 and tocm2>=150){
      left++;
    }
    else if(tocm>=150 and tocm2<=150){
      right++;
    }
  }
  else
  {
    digitalWrite(12,LOW);
  }
  

  if(tocm2<=150 or tocm<=150)
  {
    digitalWrite(13,HIGH);
  }
  else
  {
    digitalWrite(13,LOW);
  }
 }
  
  
  if(tocm3<=150 and tocm<=150 and tocm2>=150)
  {
    digitalWrite(12,HIGH);
    digitalWrite(13,LOW);
  }
  else if(tocm3<=150 and tocm2<=150 and tocm>=150)
  {
    digitalWrite(13,HIGH);
    digitalWrite(12,LOW);
  }
  else if(tocm3<=150 and tocm2<=150 and tocm<=150)
  {
    digitalWrite(13,LOW);
    digitalWrite(12,LOW);
  }
 }
}  
    

long microsecondsToCentimeters(long microseconds)
{
return microseconds / 29 / 2;
}
