# Software Design

Continuing with the theme of modularity, our software was written to be expandable to any dimension of Connect-Four™ beyond a 6 x 6 design. The code was written in C for Texas Instrument's MSP 430 microcontroller which serves as the brains of the logic operation. Here is a flowchart showcasing how the program works.

<img class="center" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/flowchartt.jpg?raw=true" height="500">

# MSP 430
<img class="center" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/msp.png?raw=true" height="500">
In the MSP430, we utilized various pins to control the I/O of our system. We used six I/O pins for input from our buttons. We also used P1.7 to control the array of LEDs.

# Button Inputs
This project mostly relied on user input from buttons. However, an issue was that the buttons would bounce when pressed, which means the signal would rapidly fluctuate when a button was pressed. Since we are sampling continuously, when the buttons would be pressed it would sometimes rapidly send either 1 or 0 when the button was pressed, which caused the program to register multiple inputs from the user even if they only pressed the button once. Though this issue could be fixed with either hardware or software, our team ultimately decided to use the software solution considering our current materials, budget and timeline. This solution involved adding functions in our program that would process the signal when the button was pressed and debounce it. These functions sampled 8 bit values from the buttons and checked whether all the 8 bits were 1 or not. If all the bits were 1 then we registered the user input and lighted up the corresponding LED, otherwise we considered the button unpressed. Additionally, the previous button state was compared to the current button state to avoid registering multiple presses in the case where the user would hold the button for a long time.
<img class="center" src="https://cdn.discordapp.com/attachments/944292252920971304/1118007308895649892/image.png" height="500">


# Win Condition
When people play the board game version of Connect-Four™ they have to look for wins themselves, however for our project there are no missed wins. We designed our game to actively check for wins, which means that every time a user enters a token on the grid the program checks if the user won horizontally, vertically or diagonally. Even if the user doesn't realize they won, our program indicates to the user using their game color that they won. As soon as the user enters the token the program checks vertically then diagonally then horizontally and determines the user won, if the user won then the program does not accept input from the users for 3 seconds, then displays the winning user's color for 3 seconds and resets. 
Rough draft of this section
<li>Include TI MSP430 programming compenent (most to be written in hardware)</li>
<li>Include flowchart for code </li>
<li>Mention button debouncing fixed through software</li>
<li>Describe hardships with the programming, edge cases, bugs, etc</li>
<li>(include images of a bit of code, perhaps a GIF of a demonstration, and microcontroller itself in action)</li>
