### Fasit: Styr LED med potmeter


```
int potPin = 0;
int ledPin = 8;
void setup() {
  pinMode(potPin,INPUT);
  pinMode(ledPin,OUTPUT);
  Serial.begin(9600);
}

void loop() {
  
  int potValue = analogRead(potPin);
  int highValue = (potValue/1024.0)*1000.0;
  int lowValue = 1000-highValue;

  digitalWrite(ledPin,HIGH);
  delayMicroseconds(highValue);
  digitalWrite(ledPin,LOW);
  delayMicroseconds(lowValue);
} 
```
