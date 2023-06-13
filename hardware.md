# Hardware Design
Our hardware design starts with the NeoPixel PCBs! Retrofitted with four NeoPixel LEDs, the design for this PCB takes modularity into account. Their function is to illuminate our acrylic panels to serve as "tokens" shining red, green, or blue, indicating the piece that has been dropped onto the EE-Connect arena or when a win condition has been met. Our design serves great emphasis to scalability given its cleverly sleek design to be place on uniform surfaces. Power is delivered from the bottom pins, our data pin at the middle, and ground up top. <More to be added>

<img src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/neopixel.png?raw=true" height="300">
  
Our second PCB created was the main PCB. The main purpose of the main PCB was to provide a power source for the elements of our circuit. Thus is was critical to include a DC Power Jack that recieved power from an power outlet using a power cord. Since the ouput of the DC Power Jack was 5V, and the microntroller was required 3.3V as a power source, a regulator was necessary to take 5V and emit a 3.3V source. Furthermore, the main PCB includes Button pins and the LED pins required to allow the game to work as intended. These header was connect to the IC of the Microntroller which was also located on the PCB.
...
Rough draft of this section
<li>Describe the TI MSP430 microcontroller</li>
<li>Debugging power issues causing bugs </li>
<li>Button configurations </li>
<li>(include images of MCU, buttons, a GIF could work for final product)</li>
