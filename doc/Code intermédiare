 * Ce code ne fonctionne pas à cause d'un mauvais fonctionnement des capteurs en analogique.
 
 
#include <Wire.h>
#include <Adafruit_GFX.h>
#include<Adafruit_SSD1306.h>
#define SCREEN_WIDTH 128 // OLED display width, in pixels
#define SCREEN_HEIGHT 64 // OLED display height, in pixels
#define OLED_RESET 4 
Adafruit_SSD1306 display(OLED_RESET);

const char analogPinD = 0;
const char analogPinG = 1;
const char pinLedD = 8;
const char pinLedG = 10;
void setup() {
  Wire.begin();
  display.begin(SSD1306_SWITCHCAPVCC, 0x3C);
  pinMode(analogPinD, INPUT);
  pinMode(analogPinG, INPUT);
  pinMode(pinLedD, OUTPUT);
  pinMode(pinLedG, OUTPUT);
  Serial.begin(9600);


  
}
void displayCross(){
  delay(500);
   int D = analogRead(analogPinD);
  int G = analogRead(analogPinG);
  display.clearDisplay();
  display.setTextColor(WHITE);
  display.setTextSize(1);
  display.setCursor(0,0);
  display.print("Seelence : ");
  display.setCursor(0,10);
  display.print("Droite : ");
  display.print(analogRead(analogPinD)); 
  display.setCursor(0,20);
  display.print("Gauche : ");
  display.print(analogRead(analogPinG )); 
  Serial.println(D);
  Serial.println(G);
  delay(100);
}
void displayCross2(){
  int D = analogRead(analogPinD);
  int G = analogRead(analogPinG);
  if (D > G){
    if (D > 30){
      digitalWrite(pinLedD, 1);
      display.setCursor(0,70);
      display.print( "===>");
    }
    else{
     
    }
  }
  if (D < G){
        if (G > 30){
      digitalWrite(pinLedG, 1);
      display.setCursor(0,70);
      display.print( "<===");
  }
 

     


}}
      
void loop() {
  displayCross();
  displayCross2();
  display.display();
}
