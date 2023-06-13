# Software Design

Continuing with the theme of modularity, our software was written to be expandable to any dimension of Connect-Four™ beyond a 6 x 6 design. The code was written in C for Texas Instrument's MSP 430 microcontroller which serves as the brains of the logic operation. Here is a flowchart showcasing how the program works.

<img class="responsive" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/flowchartt.jpg?raw=true" height="500">

# MSP 430
<img class="responsive" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/msp.png?raw=true" height="250">
In the MSP430, we utilized various pins to control the I/O of our system. We used six I/O pins for input from our buttons. We also used P1.7 to control the array of LEDs.

# Win Condition
When people play the board game version of Connect-Four™ they have to look for wins themselves, however for our project there are no missed wins. We designed our game to actively check for wins, which means that every time a user enters a token on the grid the program checks if the user won horizontally, vertically or diagonally. Even if the user doesn't realize they won, our program indicates to the user using their game color that they won. As soon as the user enters the token the program checks vertically then diagonally then horizontally and determines the user won, if the user won then the program does not accept input from the users for 3 seconds, then displays the winning user's color for 3 seconds and resets. The game continues until the board is full or a user wins, whichever comes first. If a user wins on the last token filling up the board then their win is prioritized and the program displays their color rather than blue and resets. 
