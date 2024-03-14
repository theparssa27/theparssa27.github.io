# Hardware Design
Our hardware design starts with the NeoPixel PCBs! Retrofitted with four NeoPixel LEDs, the design for this PCB takes modularity into account. Their function is to illuminate our acrylic panels to serve as "tokens" shining red, green, or blue, indicating the piece that has been dropped onto the EE-Connect arena or when a win condition has been met. Our design serves great emphasis to scalability given its cleverly sleek design to be place on uniform surfaces. Power is delivered from the bottom pins, our data pin at the middle, and ground up top. <More to be added>

# NeoPixel
<img class="responsive" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/neopixel.png?raw=true" height="300">

# MCU PCB
Our second PCB created was the Central PCB. One purpose of this PCB was to provide a power source to the elements of our circuit. It was critical to include a DC Power Jack that received power from an power outlet using a power cord. Since the output of the DC Power Jack was 5V, and the microcontroller required 3.3V as a power source, a regulator was necessary to take 5V and emit a 3.3V output. Furthermore, the Central PCB includes Button pins and the LED pins required to allow the game to work as intended. These header was connect to the IC of the Microcontroller which was also located on the PCB. The IC was programmed to include the game logic.
  
<img class="responsive" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/i2.png?raw=true" height="400">
  
# Button Inputs
This project mostly relied on user input from buttons. However, an issue was that the buttons would bounce when pressed, which means the signal would rapidly fluctuate when a button was pressed. Since we are sampling continuously, when the buttons would be pressed it would sometimes rapidly send either 1 or 0 when the button was pressed, which caused the program to register multiple inputs from the user even if they only pressed the button once. Though this issue could be fixed with either hardware or software, our team ultimately decided to use the software solution considering our current materials, budget and timeline. This solution involved adding functions in our program that would process the signal when the button was pressed and debounce it. These functions sampled 8 bit values from the buttons and checked whether all the 8 bits were 1 or not. If all the bits were 1 then we registered the user input and lighted up the corresponding LED, otherwise we considered the button unpressed. Additionally, the previous button state was compared to the current button state to avoid registering multiple presses in the case where the user would hold the button for a long time.
<img class="responsive" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/i3.jpeg?raw=true" height="500">

