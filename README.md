# AddOnSpot
A shitty add-on (SAO) that has a light that changes between red, yellow, and green.

## Description
The intended purpose for this SAO is for people to be able to indicate their social boundries in public settings. The inspiration for this project comes from a [tweet](https://twitter.com/k8em0/status/1156100010657718272) by [k8emo](https://twitter.com/k8em0) and a [project](https://medium.com/@elkentaro/ledify-you-life-color-changing-tiara-build-f12cb3d7741) by [elkentaro](https://twitter.com/elkentaro).

The three colours of light (red, yellow, and green) can be used by the user to indicate three different things:
* red means that they not want anyone to approach them at that time,
* yellow means that they are only open to people they know approaching them, 
* green means that they are open to anyone coming up to say 'hi!'.

## Design Considerations
* This SAO was designed to control the LEDs in two ways depending on what the user desires. :

  * The first (and suggested) way to control the LEDs is with the two switches that are provided on the SAO. One of the switches turns on the red LED and the other turns on the green LED. If the user turns on both of the switches the LED will be yellow.
  
  * The second way to control the LEDs is from the board the SAO is attached to. Controlling the LEDs on the SAO from the board it is attached to can be done through the GPIO1 and GPIO2 pins (pins 1&2 on the rectangular connector in the schematic). If the user wants to control the LEDs with the GPIO pins, they will need to populate the resistors between the GPIO pins and the LEDs. The reason that the resistors from the GPIO pins are not populated by default is because sometimes GPIO pins are pulled up by default. If the connection point from the GPIO pins were between the switches and their resistors, the LEDs would always be dimly on, thus making it difficult to display just red or just green, or to turn the SAO off. 

* The switches that were chosen were picked for their extended actuator length. The hope is that an extended actuator length will make it easier for people with long fingernails using the SAO to turn the lights on and off. 
