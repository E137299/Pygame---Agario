# Pygame---Agario
Agar.io is an online multiplayer game that was first released in 2015. It was created by Matheus Valadares. The game is set in a petri dish, and players control a cell, represented by a circular object. The objective is to grow the cell by eating smaller cells and avoiding being eaten by larger cells.

The gameplay is relatively simple: players move their cells around the playing field, consuming smaller cells to increase their size. The larger a player's cell, the slower it moves. Players can split their cells into smaller pieces or eject mass to maneuver and interact with other players strategically.

## Enemy CLASS:

### Attributes:

- Radius - randomly selects a radius. The lower end of the range needs to be less than the player's radius and upper end of the range needs to be larger than the player's radius.
- Color - randomly selected
- Speed - The speed should be inversely proportional to the radius of the ball. The smaller the ball, the faster it travels and visa versa.
- Direction - randomly selected

### Methods:

- constructor - Each Enemy object will have: 
  1. a random location around playing area
  2. a random colors
  3. a randomly selected radius
  4. a random heading
- move() - The move method can be code in one of two ways.
  1. Opponents will travel in straight lines until hit edge of canvas and at which point they will reflect off of the boundary.
  2. Opponents will travel in straight lines. When they encounter can a boundary, they will reappear on the opposite side of canvas.
- collisionDetector() - returns True if the enemy object overlaps another object (Enemy or Food)
- grow() - This method allows the Opponent object to grow by the radius of the the object that it absorbs. The speed of the Enemy object should decrease propotionally with the radius of the Enemy object.

 

## FOOD CLASS:

### Attributes:
- color - randomly selected
- radius
### Method:
- constructor:
  1. random location on playing area
  2. random color

## PLAYER CLASS:
### Attributes:
- Radius
- Color
- Speed

### Methods:
- constructor
- move() - Two options:
  1. Use key presses to move player
  2. Have the player follow the cursor. The player should no go to the mouse immediately, but travel at a set speed to the mouses location.
- collisionDetector() - returns True if the player object overlaps another object (Enemy or Food)
- grow() - This method allows the Player to grow by the radius of the the object that it absorbs.It's speed should decrease as the player grows.

- bye() - If the player is killed, a "You lose!" message will appear.
  
## SUPPORTING FUNCTIONS 
- distance(object1, object2) - returns the distance between two objects. Pythagorean Theorem
- draw_grid() - draws a grid background on the Pygame window
