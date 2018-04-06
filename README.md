# Trinket

**Datasheet**: https://cdn-learn.adafruit.com/downloads/pdf/introducing-trinket.pdf

Trinket board specs:

* USB bootloader with an LED indicator
* Mini USB jack for program uploading
* ~5.25K bytes available for use (2.75K taken for the bootloader
* Available in both 3V and 5V
* On-board 3.3V or 5.0V power regulator with 150mA output capability and ultra-low dropout
* Up to 16V input, reverse-polarity protection, thermal and current-limit protection
* Power with either USB or external output (such as a battery) - it'll automatically switch over
* On-board green power LED and red (pin #1) LED
* Reset button for entering the bootloader or restarting the program
* Hardware I2C / SPI capability for breakout & sensor interfacing
* Mounting holes, you can easily attach it to breadboard or plug it in your own circuit board!

## Prerequisites

To use the Trinket 5V you need to install some drivers.
First, connect your card to your computer, then install the drivers. You can find the drivers here: [Driver for Trinket](https://github.com/adafruit/Adafruit_Windows_Drivers/releases/download/2.2.0/adafruit_drivers_2.2.0.0.exe)

After that, open the arduino-1.6.4 folder and launch arduino.exe

If the drivers are well installed, you can select your card (tool->board: Adafruit Trinket 16MHz) and select the programmer (tool->programmer: USBtinyISP).

## Example

Try the following code to blink the led.
```
/*
  Blink
  Turns on an LED on for one second, then off for one second, repeatedly.
*/

// Pin 1 has an LED connected on most Trinket boards.
// give it a name:
int led = 1;

// the setup routine runs once when you press reset:
void setup() {
  // initialize the digital pin as an output.
  pinMode(led, OUTPUT);
}

// the loop routine runs over and over again forever:
void loop() {
  digitalWrite(led, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);               // wait for a second
  digitalWrite(led, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);               // wait for a second
}
```
