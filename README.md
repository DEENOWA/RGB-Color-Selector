# RGB-Color-Selector
This Arduino code controls an RGB LED connected to pins 9 (red), 10 (green), and 11 (blue), allowing the user to select a color to display via serial communication.
In the setup function, it initializes serial communication at 115200 baud and sets the LED pins as outputs, initially turning all LED components off using analogWrite with a value of 0. 
In the loop function, it prompts the user to input a color (RED, GREEN, BLUE, MAGENTA, CYAN, YELLOW) through the serial monitor. 
It reads the input as a string, trims whitespace, converts it to lowercase, and clears the serial buffer. 
Based on the input, it sets the RGB LED to display the selected color by adjusting the analogWrite values for the red, green, and blue pins: "red" sets red to 255 and others to 0; "green" sets green to 255 and others to 0; "blue" sets blue to 255 and others to 0; "magenta" sets red and blue to 255, green to 0; "yellow" sets red to 255, green to 25, and blue to 0; "cyan" sets green and blue to 255, red to 0. 
If the input doesn't match any valid color, it prints "Invalid Color Name!" to the serial monitor. 
The loop then repeats without any delay.
