# MicroBit-Morse-Code-Assignment

/*
Assignment 1
Morse Code
28/05/2021
Version 8
*/

#include "MicroBit.h"

MicroBit uBit;

//Declaring new variable
int Lighty;

//Declaring new variable
char lightChar;

//Declaring new variable
int c

int main()
{

//Initialising microbit runtime
    uBit.init();
    
//To send a serial signal thorugh putty
    uBit.serial.baud(115200);

//Create while loop to inform light levels
    while(1)
    {
        
//This comand sends the light display to computer
     Lighty=uBit.display.readLightLevel();
        
// This will send the light level to the computer through serial communication
    lightChar= printf("light level is %lu\n", Lighty);
          uBit.serial.send(Lighty);
     
//Gives a 1 second pause
     uBit.sleep(1000);
     
     }
     
//Create while loop to inform if light levels over or under 10
 while (1)
 
 {
 //If the light level is less than 10
 if (Lighty<10)
 
 //It will send the light level to the computer through serial communication
 lightChar= printf("light level is %lu\n", Lighty);
 
 //And will produce the number 0
 lightChar=printf("0",lighty);
 uBit.serial.send(Lighty);
 
 //Gives a 1 second pause
 uBit.sleep(1000);
  
 //Else if the first statement is not true and light levels are over 10 then 
 else if (Lighty>10)
 
 //It will send through the light level to the computer
 lightChar= printf("light level is %lu\n", Lighty);
 
 //And will produce the number 1
 lightchar=printf("1",lighty);
 uBit.serial.send(Lighty);
 
 //Gives a 1 second pause
 uBit.sleep(1000);
 
 }
 
 //Creating a while loop to count pulse
 while(1)
 {
//If light is on >10
    if (uBit.io.P0.getDigitalValue()==1);
 
//Counter adds 1
    C++;

//Microbit displays whatever C is
    uBit.display.print(C);

//uBit pauses for 2 seconds after button pressed
    uBit.sleep(2000);
 }
 
 //Creating while loop
 while(1)
 {
//If light if off 10<
    if (uBit.io.P0.getDigitalValue()==0);
    
//Counter adds 1
    C++;
    
//Microbit displays whatever C is
    uBit.display.print(C);

//uBit pauses for 2 seconds after button pressed
    uBit.sleep(2000);
    
}    

const char* characters = "abcdefghijklmnopqrstuvwxyz0123456789";

const char* mappings[] = {
    ".-\0",     //a
    "-...\0",   //b
    "-.-.\0",   //c
    "-..\0",    //d
    ".\0",      //e
    "..-.\0",   //f
    "--.\0",    //g
    "....\0",   //h
    "..\0",     //i
    ".---\0",   //j
    "-.-\0",    //k
    ".-..\0",   //l
    "--\0",     //m
    "-.\0",     //n
    "---\0",    //o
    ".--.\0",   //p
    "--.-\0",   //q
    ".-.\0",    //r
    "...\0",    //s
    "-\0",      //t
    "..-\0",    //u
    "...-\0",   //v
    ".--\0",    //w
    "-..-\0",   //x
    "-.--\0",   //y
    "--..\0",   //z
    "-----\0",  //0
    ".----\0",  //1
    "..---\0",  //2
    "...--\0",  //3
    "....-\0",  //4
    ".....\0",  //5
    "-....\0",  //6
    "--...\0",  //7
    "---..\0",  //8
    "----.\0",  //9
};
