# Rain Run

Simple Java game allowing user to control a character using keyboard input, where the user must make quick decisions to navigate a terrain.

To run:
1. Download this repository.
2. Run the file RainRunGUI.java

```
cd path/to/rain-run
javac RainRunGUI.java
java RainRunGUI
```

## Change log

* Angelina - Modified RainRun and RainRunPanel for modularity. Assumes that FallingObjects all contain the method: public void moveDown(int speed);
* Angelina - Updated the FallingObject & Character interfaces, and PowerUp class to reflect that change
* Mara - Update backend classes (MyCharacter, Monster)
* Mara - FallingObject interface needs to be implemented by Monster - all things that fall are FallingObjects in this game.
* Mara - Added png files to images, for MyCharacter (minion) and rain drops (2 dimensions)
* Angelina - Changed the way falling objects are added such that the space between falling objects stays approximately the same

## Data Structures

* Hash Tables for storing the hit rules
* Vector to store FallingObjects 
* Hash Tables for scores 


## To Do

### Mara

### Angelina

### Isabel

* Create a main menu to start the game from.
* When a game has ended, insert a button they can press to return to the main menu.
* Create a rules panel explaining the rules of the game, to link from the main menu.

### Hunter

* DeadPanel 
* FallingObject
* Start slides 

### Other 

* [Optional] Allow the user to choose what color their character should be, and/or different themes.
* [Optional] Include "themes" / "levels" in our game, where periodically the background / monster colors change.


## Technical specifications

### Character - DONE (Angelina)
* Character interface specifies what properties Characters have
* Think of each object appearing on RainRunPanel as a Character / sometimes a FallingObject

### FallingObject - DONE
* maybe: create a new class for all Characters that fall (monsters, powerups)

### MyCharacter - Mara
* Attributes: died; health;

### Monster - Mara
* Attributes: moveDown();

### RainRun
* Attributes: score; time; scoreInc; speed; monsters / powerUps (maybe Vector<FallingObject>); addElInterval; increaseSizeInterval; increaseSpeedInterval;

### PowerUp
* Method: moveDown(int speed) <-- probably wants to zig zag differently based on speed


## Rules

1. You control the character at the bottom using the left/right or A/D keys.
2. Avoid the falling monsters in blue.
3. Catch different powerups to gain special advantages! 
4. Over time the monsters will start to get bigger and the game will start to move faster.
5. The game ends when you lose each of your 3 lives.

## Notes

1. Monsters move straight down.
2. Bigger monsters move faster - watch out!
3. Powerups zig zag.

## Powerups

![alt text][health]

**Health Powerup**

Will give you one additional life if you have less than 3 lives currently, as well as giving you a bonus 10 points.

![alt text][speed]

**Speed Powerup**

Will increase the pace of the game, and will also increase the amount your score increases by each time interval.

![alt text][umbrella]

**Umbrella Powerup**

Gives you a free 50 extra points!

[health]: images/heart2.png "Health Powerup"
[speed]: images/speed2.png "Speed Powerup"
[umbrella]: images/umbrella2.png "Umbrella Powerup"
