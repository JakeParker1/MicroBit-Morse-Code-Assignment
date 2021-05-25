# MicroBit-Morse-Code-Assignment

/*
Assignment 1
Morse Code
25/05/2021
Version 4
*/

#include "MicroBit.h"

MicroBit uBit;

//creating new variable
int Lighty;

//creating new variable
char lightChar;

int main()
{
    uBit.init();
    //to send a serial signal
    uBit.serial.baud(115200);
    
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
     
//While this statement is true
 while (1)
 
 
 //If the light level is less than 10
 if (Lighty<10)
 {
 //it will send the light level to the computer through serial communication
 lightChar= printf("light level is %lu\n", Lighty);
 
 //and will produce the number 0
 lightchar=printf("0",lighty);
 uBit.serial.send(Lighty);
 
 //gives a 1 second pause
 uBit.sleep(1000);
  
  // If the first statement is not true and light levels are over 10 then 
 else if (Lighty>10)
 
     //it will send through the light level to the computer
 lightChar= printf("light level is %lu\n", Lighty);
 
 //and will produce the number 1
 lightchar=printf("1",lighty);
 uBit.serial.send(Lighty);
 
 //gives a 1 second pause
 uBit.sleep(1000);
 }
 }
 
 //Conversion from Morse Code to Alphabet & Numbers 
 //When light shows these sequences
morse = [".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ...
".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.", "...", ...
"-", "..-", "...-", ".--", "-..-", "-.--", "--..", ".----", "..---", ...
"...--", "....-", ".....", "-....", "--...", "---..", "----.", "-----"]
//It will produce its enlish translation as shown below
alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", ...
"m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "1", ...
"2", "3", "4", "5", "6", "7", "8", "9", "0"]
