# WEATHER-DETECTOR

This project is used to detect the temp and humidity of the environment .By using the arduino uno and dht22 sensor 

##Components
  Arduino Uno
  DHT22 sensor
  Jumper wire

#Aim
  By the help of DHt22 sensor to detect the humidity and temperature

#Project
 <img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/397e793f-7ac3-4f0d-b1ff-578849c386eb" />

![Image](https://github.com/user-attachments/assets/dedc068e-97e6-4a89-aaec-b7c96524f425)

![Image](https://github.com/user-attachments/assets/6e473c78-36ed-4ab4-855a-da73c4284eba)

##Code 

#include "DHT.h"

#define DHTPIN 13
#define DHTTYPE DHT22

DHT dht (DHTPIN,DHTTYPE);
 
void setup(){
  Serial.begin(9600);
  dht.begin();
}
void loop(){
  delay(2000);
  float humidity =dht.readHumidity();
  float temperature =dht.readTemperature();
  
  if(isnan(humidity)|| isnan(temperature) ){
    Serial.println("failed to read ")
    return ;

 
 }
  Serial.print("Humidity:");
  Serial.print(Humidity);
  Serial.print("%\t");
  Serial.print("Temperature:");
  Serial.print(temperature);
  Serial.print("C");
}
#Final conculsion
   This project can be used to detect the temperature and humidity 
