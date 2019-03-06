### Fasit: Styr LED fra Lampe

```
// denne variabelen holder på status på knappen
int buttonState = 0;

void setup()  {
  // pin 2 konfigureres til å gi signaler ut til LED (OUTPUT)
  pinMode(2, OUTPUT);
  // pin 2 konfigureres til å lese verdi (INPUT) fra knapp
  pinMode(3, INPUT);
}

void loop() {
    // les verdi på knapp (av eller på)
    buttonState = digitalRead(3);
    // hvis knapp er trykket inn
    if( buttonState == true ) {
      // tenn lampe
      digitalWrite(2, HIGH);  
      // vent 2 sekunder
      delay(2000);
      // slukk lampen
      digitalWrite(2, LOW);  
    }
}
```