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

### Function 1: flooring (Parameters: width and length of the room )
1. Set up the function so that it takes in the two required variables as parameters.  Then call the function using the appropriate keypress.
2. Use a cost of $1.88/square ft for your carpet.
3.  Calculate the total Square Feet of floor in the room.
4.  Calculate the total and **print** the total price into the display box.
```
Your total square feet is ___
Our carpeting price per square foot is $____
Your carpeting cost will be $___
```


### Function 2: paint (Parameters: width, length, and height of the room )
1. Set up the function so that it takes in the three required variables as parameters.  Then call the function using the appropriate keypress.
2. Use a cost of $26.50/gallon for paint.
3. Calculate the total square footage for your four walls.
4. Calculate the number of gallons of paint it will take.
 - You should look up the ceiling function for how to round up if you want to make it more realistic.  (You can not buy part of a can of paint.)  
5. Calculate and print the cost into the display box as follows.
```
The total square footage of your four walls and the ceiling is __
This requires ___ gallons of paint.
Price per gallon is $___
Your total for paint will be $___
```
### Function 3: hotTub ( Parameters: width and length of the room)
Our store sells the following **CIRCULAR** hot tubs.  We will assume that they will purchase the **LARGEST** of the three that would fit in their room.

| Model          | Diameter (including walking space) | Price  |
|----------------|------------------------------------|--------|
| Petite Piscine | 10 feet (3.05 metres)              | $2100  |
| Medium         | 14 feet (4.27 metres)              | $4000  |
| Biggest Bubbly | 18 feet (5.49 metres)              | $6100  |
| No hottub avaliable | If less than 10 feet or 3.05 metres             | $-  |

1.  Set up the function so that it takes in the two required variables as parameters.  Then call the function using the appropriate keypress.
2.  Based on their room dimensions, tell them the price of the largest of the 3 hot tubs they can fit in the room.
   - Note that there is a subtle trick to figuring out the hot tub size.  Remember it must be a perfect circle. the `dist()` function will help you
    - 5% will be permanently lost if you recommend the wrong tub or a tub that does not fit in the room.  Be thoughtful about what is recommended and test it thoroughly.

```
The largest hot tub that will fit in your room is the Medium Masterpiece It costs $4000
```

## Next 10% - Fourth Option
Add a 4th option to the menu with a new method and calculation of your choice. Think about other things you might want to calculate (rolls of wall paper, etc.).  Pass in only the measurements you need but feel free to ask for extra information if needed (such as asking for a fence height or a rug shape).

## Next 10% - Not Allowing Zeros 
Currently, if the user chooses one of the purchase options before entering the dimensions of the room, then everything calculates based on zero.  

Alter your keypress function OR the purchase functions so that the display box is blank if any of the dimensions are zero.  (Alternatively, you could print an error message.)

## Final 10% - Paint and/or Carpet Options
You will get these marks if you can show that you attempted this challenge, not to succeed.

Modify your functions to present the user with some paint and/or flooring options. 
1. They should choose from the usual menu
2. If they choose flooring or paint you give them one more choice of TYPE of flooring or paint. This could be accomplished with an additional window.prompts, new keypresses or even by adding buttons (most people use an additional window.prompt because it is way easier).
    -  Do you want our deluxe carpet for $2.05 per square foot or our hardwood at $5.60 per square foot.
3. You only need to apply this to ONE of the flooring or paint, not both.
4. Once the user has selected their sub-option, their flooring and paint costs should be calculated using the appropriate price. 

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
