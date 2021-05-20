# MicroBit-Morse-Code-Assignment

/*
Assignment 1
Morse Code
20/05/2021
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
    
/*Conversion from Morse Code to Alphabet & Numbers*/
morse = [".-", "-...", "-.-.", "-..", ".", "..-.", "--.", "....", "..", ".---", "-.-", ".-..", "--", "-.", "---", ".--.", "--.-", ".-.", "...", "-", "..-", "...-", ".--", "-..-", "-.--", "--..", ".----", "..---", "...--", "....-", ".....", "-....", "--...", "---..", "----.", "-----"]
alphabet = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "1", "2", "3", "4", "5", "6", "7", "8", "9", "0"]


