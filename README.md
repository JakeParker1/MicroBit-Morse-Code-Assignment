# MicroBit-Morse-Code-Assignment

/*
Assignment 1
Morse Code
26/05/2021
Version 6
*/

#include "MicroBit.h"

MicroBit uBit;

//creating new variable
int Lighty;

//creating new variable
char lightChar;

//creating new variable
int c

int main()
{

//Initialising microbit runtime
    uBit.init();
    
//to send a serial signal thorugh putty
    uBit.serial.baud(115200);

//Create while loop to inform light levels
    while(1)
    {
        
//this comand sends the light display to computer
     Lighty=uBit.display.readLightLevel();
        
// this will send the light level to the computer through serial communication
    lightChar= printf("light level is %lu\n", Lighty);
          uBit.serial.send(Lighty);
     
//gives a 1 second pause
     uBit.sleep(1000);
     
     }
     
//Create while loop to inform if light levels over or under 10
 while (1)
 
 {
 //If the light level is less than 10
 if (Lighty<10)
 
 //it will send the light level to the computer through serial communication
 lightChar= printf("light level is %lu\n", Lighty);
 
 //and will produce the number 0
 lightChar=printf("0",lighty);
 uBit.serial.send(Lighty);
 
 //gives a 1 second pause
 uBit.sleep(1000);
  
  // Else if the first statement is not true and light levels are over 10 then 
 else if (Lighty>10)
 
     //it will send through the light level to the computer
 lightChar= printf("light level is %lu\n", Lighty);
 
 //and will produce the number 1
 lightchar=printf("1",lighty);
 uBit.serial.send(Lighty);
 
 //gives a 1 second pause
 uBit.sleep(1000);
 
 }
 
 //creating a while loop to count pulse
 while(1)
 {
//if external button is pressed
    if (uBit.io.P0.getDigitalValue()==1);
 
//Counter adds 1
    C++;

//Microbit displays whatever C is
    uBit.display.print(C);

//uBit pauses for 2 seconds after button pressed
    uBit.sleep(2000);
 }
 
 //Conversion from Morse Code to Alphabet & Numbers 
 //When light shows these sequences
morse = [".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ...
".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.", "...", ...
"-", "..-", "...-", ".--", "-..-", "-.--", "--..", ".----", "..---", ...
"...--", "....-", ".....", "-....", "--...", "---..", "----.", "-----"]
//It will produce its English translation as shown below
alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", ...
"m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "1", ...
"2", "3", "4", "5", "6", "7", "8", "9", "0"]
