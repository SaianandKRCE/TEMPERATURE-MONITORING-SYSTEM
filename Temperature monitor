#include <Wire.h>
#include <LiquidCrystal_I2C.h>


LiquidCrystal_I2C lcd(0x27, 16, 2); // I2C address, columns, rows
int sensorPin = A0; // LM35 output connected to A0

void setup() {
  lcd.begin(16,2);  // Initialize LCD
  lcd.backlight();  // Turn on LCD
  lcd.setCursor(0, 0);
  lcd.print("Temp Monitor");
  delay(500);
  lcd.clear();
  
}

void loop() {
  int sensorValue = analogRead(sensorPin);  // Read analog value from LM35
  float voltage = sensorValue * (5.0 / 1024.0); //Convert to voltage
  float temperatureC = voltage * 100.0; // Convert to temperature in celsius

  lcd.setCursor(0, 0);
  lcd.print(" ");
  lcd.print("Temp: ");
  lcd.print(temperatureC);  //Display temperature
  lcd.print(" C ");

  delay(2000);  //Refresh every 2 second
}
