# flappybird_using_lua
# Fifty Bird Game README.md

This README.md file provides an overview and explanation of the code for the game "Fifty Bird." The game is a Flappy Bird clone, where the player controls a bird and navigates it through a series of pipes, trying to score as many points as possible.

## Getting Started

### Prerequisites

To run the Fifty Bird game, you need to have [LÖVE2D](https://love2d.org/) installed on your system. LÖVE2D is a framework for creating 2D games and applications using Lua scripting language.

### Running the Game

1. Download and install LÖVE2D from [here](https://love2d.org/).
2. Clone or download the repository containing the Fifty Bird game code.
3. To start the game, drag and drop the folder containing the game files onto the LÖVE2D executable, or run the following command in the terminal:

```bash
love /path/to/fifty-bird-game
```

## Game Description

Fifty Bird is a 2D side-scrolling game where the player controls a bird. The goal is to navigate the bird through a series of pipes by tapping the 'spacebar' to keep the bird airborne. The player earns points by successfully passing through the gaps between the pipes. Colliding with the pipes or the ground will end the game.

## Controls

- Tap the 'spacebar': Make the bird flap and fly upwards.
- 'Escape': Quit the game.

## Code Structure

The Fifty Bird game is built using Lua and organized into several modules:

### Main.lua

- This file is the entry point of the game and contains the `love.load()`, `love.update()`, `love.draw()`, and `love.keypressed()` functions.
- The `love.load()` function is used to initialize the game, including setting up fonts, sounds, and screen settings.
- The `love.update()` function is called every frame and updates the game logic, including scrolling background and pipes, updating the state machine, and handling keyboard input.
- The `love.draw()` function is called every frame to render the game, including the background, pipes, bird, and UI elements.
- The `love.keypressed()` function handles keyboard input, allowing the player to control the bird and quit the game.

### Push.lua

- This file is a library called Push that handles resolution and scaling for different screen sizes.
- It is used to maintain a consistent virtual resolution while allowing the game to be displayed on various screen sizes.

### Class.lua

- This file is another library called Class that provides Object-Oriented Programming capabilities.
- It is used to define the `Bird`, `Pipe`, and `PipePair` classes.

### States

The game uses a state machine to manage different game states:

1. `TitleScreenState`: The title screen state displayed when the game starts or is restarted.
2. `CountdownState`: A countdown before the game starts.
3. `PlayState`: The main gameplay state where the bird navigates through the pipes.
4. `ScoreState`: The state shown when the game is over, displaying the player's score.

### Fonts and Sounds

- The game uses four different fonts for different UI elements and sound effects for jumping, collision, scoring, and background music.

## Game Logic

1. Scrolling Background: The game has a scrolling background effect to create a sense of motion while the bird stays in the center.

2. Pipes: The pipes are generated randomly at different heights, creating gaps for the bird to pass through.

3. Bird Control: The player can control the bird's altitude by tapping the 'spacebar', which makes the bird flap and fly upwards.

4. Collision: The game detects collisions between the bird and the pipes or ground, ending the game if a collision occurs.

5. Scoring: The player earns points each time the bird successfully passes through a gap between the pipes.

## Acknowledgments

The Fifty Bird game code was created by Harsh Gupta(Desparete Enuf). The game is inspired by Flappy Bird and built using the LÖVE2D framework. It makes use of external libraries for resolution handling (Push) and object-oriented programming (Class). The fonts and sound effects used in the game have separate licensing terms and are not covered under this license.

## License

This project is licensed under the [MIT License](LICENSE). You are free to modify and distribute the code, but please provide proper attribution to the original creator. Sound files used in this project have separate licensing terms and are not covered under this license.
