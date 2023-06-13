# Hardware Design
Our hardware design starts with the NeoPixel PCBs! Retrofitted with four NeoPixel LEDs, the design for this PCB takes modularity into account. Their function is to illuminate our acrylic panels to serve as "tokens" shining red, green, or blue, indicating the piece that has been dropped onto the EE-Connect arena or when a win condition has been met. Our design serves great emphasis to scalability given its cleverly sleek design to be place on uniform surfaces. Power is delivered from the bottom pins, our data pin at the middle, and ground up top. <More to be added>

<img src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/neopixel.png?raw=true" height="300">
  
Our second PCB created was the Central PCB. One purpose of this PCB was to provide a power source to the elements of our circuit. It was critical to include a DC Power Jack that received power from an power outlet using a power cord. Since the output of the DC Power Jack was 5V, and the microcontroller required 3.3V as a power source, a regulator was necessary to take 5V and emit a 3.3V output. Furthermore, the Central PCB includes Button pins and the LED pins required to allow the game to work as intended. These header was connect to the IC of the Microcontroller which was also located on the PCB. The IC was programmed to include the game logic.
  
<img class="center" src="https://cdn.discordapp.com/attachments/944292252920971304/1118009558946828288/image.png" height="400">

...
Rough draft of this section
<li>Describe the TI MSP430 microcontroller</li>
<li>Debugging power issues causing bugs </li>
<li>Button configurations </li>
<li>(include images of MCU, buttons, a GIF could work for final product)</li>
