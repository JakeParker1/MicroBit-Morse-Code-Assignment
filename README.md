# MicroBit-Morse-Code-Assignment

/*
Assignment 1
Morse Code
24/05/2021
Version 1
*/

#include "MicroBit.h"

MicroBit uBit;

/*Triggering the MicroBit Light Sensor*/
MicroBitEvent
MICROBIT_ID_DISPLAY
MICROBIT_DISPLAY_EVT_LIGHT_SENSE

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
    
    lightChar= printf("light level is %lu\n", Lighty);
     
     uBit.serial.send(Lighty);
     }
     
     //While this statement is true
     while true:
     
     //If the light level is less than 10
     if (Lighty<10)
     {
         //it will send through the light level to the computer
     lightChar= printf("light level is %lu\n", Lighty);
     
      uBit.serial.send(Lighty);
      
      }
      // If the first statement is not true and light levels are over 10 then 
     else if (Lighty>10)
     {
         //it will send through the light level to the computer
     lightChar= printf("light level is %lu\n", Lighty);
     
     uBit.serial.send(Lighty);
     
     }
     
