# DHT-AND-HUM
include <SimpleDHT.h>
int pinDHT11=A0;
SimpleDHT11 dht11(pinDHT11); 

void setup() {
//put your setup code here, to run once:
Serial.begin(9600);
delay(500);
Serial.print("DHT11 Temperature and Humidity\n\n");
delay(1000);
}

void loop() {
  // put your main code here, to run repeatedly:
byte temperature=0;
byte humidity=0;
dht11.read(pinDHT11,&temperature,&humidity,NULL);
Serial.print("Temperature & Humidity :");
Serial.print((int)temperature);
Serial.print("*c&");
Serial.print((int)humidity);
Serial.print("%H\n\n");
delay(2000);
}
![photo_2021-04-14_21-02-24](https://user-images.githubusercontent.com/80913347/114737774-f8b78800-9d64-11eb-9711-f0479c35ef07.jpg)
