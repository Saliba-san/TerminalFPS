# Terminal-textbased Oldschool FPS

This project is an implementation for ncurses of a FPS that runs on the terminal, all rendered in text (ascii + UTF-8). It's highly based on the video from javidx9, the OneLoneConder (https://www.youtube.com/watch?v=xW8skO7MFYw).

## Controls

### Movement
w and s -> horizontal movement
q and e -> strafing in the vertical axis
a and d -> rotating the player

### Godlike Controls
Left and Right (arrow-keys) -> move walls of a row
Down and Up (arrow-keys) -> select row

### Exit
o -> exits the game
get hit by a wall while moving it -> exits the game

## Parameters

The most interesting parameters to modify are the global variables in the CmdFPS.cpp file, "nScreenWidth" is the width of the screen; "nScreenHeight" is the height; "fSpeed" is the movement speed of the character; "fStepSize" is to change the step of the ray casting, decreasing it gives better resolution; "nMapWidth" and "nMapHeight" are the width and size of the map, the drawing of the map is modifieble inside the main() in the "map" string, '#' representing walls and '.' representing blank space.

## Compiling and Executing

For this project to work, you will need the ncurses library (libncurses5-dev) and to give the flag "-lncursesw" to the compiler. Like in the exemple of compiling and running bellow:

```bash
g++ -o CmdFPS CmdFPS.cpp -lncursesw
./CmdFPS
```
You will probably need to resize your terminal font-size or window-size to match the program nScreenWidth and nScreenHeight, alternatively, you can change the value of these variables in the CmdFPS.cpp file. Also, depending on your terminal emulator speed, you will have to change the fSpeed variable so it plays nicely on your terminal.

## Some C O O L images

![first print](prints/1.png?raw=true)
![second print](prints/2.png?raw=true)

