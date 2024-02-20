# 20.1.9-Assignment-Home-Renos

Your goal is to create a program that could be found at a kiosk at Hardware Superstore.  It will make calculations for a single room in the house.

## Setting up
- Create a new Javascript file called 20.1.9-Assignment-Home-Renos
- On the next page is the exact code needed to start the program.  Copy that code into the file.
- Read through the code carefully to see how it is structured.

## Global Variables
This assignment requires 3 global variables (`roomWidth`, `roomLength`, & `roomHeight`). No other global variables are allowed and these variables must be passed in as parameters where requested.

## Next 70% - Base Functionality
Begin by asking the user for the `roomWidth`, `roomLength`, & `roomHeight` of the room, triggered with the 'e'.  Using 3 consecutive `window.prompts`, ask the user for these 3 values, and set the global variables.

Function 1: flooring (Parameters: width and length of the room )
- Set up the function so that it takes in the two required variables as parameters.  Then call the function using the appropriate keypress.
- Use a cost of $1.88/square ft for your carpet.
- Calculate the total Square Feet of floor in the room.
- Calculate the total and print the total price into the display box.

Function 2: paint (Parameters: width, length, and height of the room )
- Set up the function so that it takes in the three required variables as parameters.  Then call the function using the appropriate keypress.
- Use a cost of $26.50/gallon for paint.
- Calculate the total square footage for your four walls.
- Calculate the number of gallons of paint it will take.
- Calculate and print the cost into the display box.

Function 3: hotTub ( Parameters: width and length of the room)

| Model          | Diameter (including walking space) | Price  |
|----------------|------------------------------------|--------|
| Petite Piscine | 10 feet (3.05 metres)              | $2100  |
| Medium         | 14 feet (4.27 metres)              | $4000  |
| Biggest Bubbly | 18 feet (5.49 metres)              | $6100  |
| No hottub avaliable | If less than 10 feet or 3.05 metres             | $-  |

- Set up the function so that it takes in the two required variables as parameters.  Then call the function using the appropriate keypress.
- Based on their room dimensions, tell them the price of the largest of the 3 hot tubs they can fit in the room.

## Next 10% - Fourth Option
Add a 4th option to the menu with a new method and calculation of your choice.

## Next 10% - Not Allowing Zeros 
Alter your keypress function OR the purchase functions so that the display box is blank if any of the dimensions are zero.

## Final 10% - Paint and/or Carpet Options
Modify your functions to present the user with some paint and/or flooring options.

## Start code
```
let roomwidth = 0;
let roomlength = 0;
let roomheight = 0;

function setup() {
    createCanvas(800, 800);
    background(200,190,80);
    textSize(12);
    stroke(0,0,150);
    strokeWeight(5);
    fill(0);
    rect(50, 25, 700, 175);
    noStroke();
    fill(255);
    textSize(40);
    text("Home Emporium", 70, 70);
    textSize(14);
    text("Press e to enter your room dimensions", 70, 100);
    text("Then...", 70, 130);
    text("Press f to purchase flooring.",70, 150);
    text("Press p to purchase flooring.", 70, 170);
    text("Press t to purchase an indoor hot tub.", 70, 190);   
}//end setup

function draw() {
   //leave draw empty
}//end draw

function keyPressed() {
    //background rectangle
    stroke(0,0,150);
    strokeWeight(5);
    fill(0);
    rect(50, 220, 700, 500);
    noStroke();
    fill(255);
    textSize(14);
}//end keyPressed

function mousePressed() {
    print("MouseX: " + mouseX +"     MouseY: " + mouseY  );
}//end mousePressed
```
