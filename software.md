# Software Design

# Flowchart
Continuing with the theme of modularity, our software was written to be expandable to any dimension of Connect-Four™ beyond a 6 x 6 design. The code was written in C for Texas Instrument's MSP 430 microcontroller which serves as the brains of the logic operation. Here is a flowchart showcasing how the program works.
<img class="center" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/flowchartt.jpg?raw=true" height="500">

# MSP 430
<img class="center" src="https://github.com/theparssa27/theparssa27.github.io/blob/main/pictures/msp.png?raw=true" height="500">
In the MSP430, we utilized various pins to control the I/O of our system. We used six pins (P2.0, P2.1, P2.2, P1.2, P1.3, and P1.4) as our input buttons. We also used P1.5, P1.6, and P1.7 to control the array of LEDs.

# Button Inputs
This project mostly relied on user input from buttons. However, an issue faced was that the button's ordered weren't debounced already. Thus using the buttons as is would sometimes cause an user to accidentally play two turns. Though this issue could be fixed with either a hardware ot software solution, our team ultimatelyd decided to use a software solution. This solution involved the button to be sampled for a short period of time. After the button was sampled...

Rough draft of this section
<li>Include TI MSP430 programming compenent (most to be written in hardware)</li>
<li>Include flowcahrt for code </li>
<li>Mention button debouncing fixed through software</li>
<li>Describe hardships with the programming, edge cases, bugs, etc</li>
<li>(include images of a bit of code, perhaps a GIF of a demonstration, and microcontroller itself in action)</li>
