# Chrome Dinosaur Game

This repository contains a simple Java implementation of the Chrome Dinosaur Game, a clone of the offline game that appears in Google Chrome when there's no internet connection. The game is built using Java's `Swing` library for GUI elements and animations. The dinosaur can jump over cacti and the game ends if the dinosaur collides with a cactus. 

## Features

- **Dinosaur Movement**: The dinosaur can jump using the spacebar and run along the ground.
- **Cactus Obstacles**: Random cacti appear from the right, moving towards the dinosaur.
- **Game Over and Restart**: The game stops when the dinosaur collides with a cactus and can be restarted with a spacebar press.
- **Score Display**: The score is continuously displayed, showing how long the dinosaur survives.
  
## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/chrome-dinosaur-game.git
   cd chrome-dinosaur-game
   ```

2. Make sure you have Java installed on your machine. If not, install Java:
   ```bash
   sudo apt install openjdk-11-jdk
   ```

3. Compile and run the game:
   ```bash
   javac ChromeDinosaur.java
   java ChromeDinosaur
   ```

## Controls

- **Spacebar**: Jump or restart the game after "Game Over".

## Classes and Logic

### 1. **ChromeDinosaur (Main Class)**

   - **Board Setup**: The game board has a fixed width and height, with a background color and dimensions defined.
   - **Image Loading**: Dinosaur and cacti images are loaded using `ImageIcon`.
   - **Timers**: Two timers are used:
     - `gameLoop`: Handles game updates and repainting.
     - `placeCactusTimer`: Spawns new cacti at random intervals.
   - **KeyListener**: The spacebar key triggers a jump or restarts the game.

### 2. **Block (Inner Class)**

   - Represents game objects like the dinosaur and the cacti. Each block has properties like position, size, and image.

### 3. **Game Logic**

   - **Dinosaur Jumping**: Gravity is applied to the dinosaur's velocity. The jump is triggered with spacebar.
   - **Cactus Movement**: Cacti move from right to left, and their positions are updated every frame.
   - **Collision Detection**: The game detects when the dinosaur collides with a cactus, triggering "Game Over."

### 4. **Scoring**

   - The score increments as long as the game continues without a collision.

## Assets

- **Images**: The game uses the following images, located in the `./img/` directory:
  - `dino-run.gif`: Dinosaur running animation.
  - `dino-dead.png`: Image shown when the dinosaur dies.
  - `dino-jump.png`: Image shown when the dinosaur jumps.
  - `cactus1.png`, `cactus2.png`, `cactus3.png`: Different cactus images for variety.

## To Do

- Add sound effects.
- Implement more dinosaur animations.
- Add difficulty progression as the game progresses.

## Screenshot


![Screenshot (1158)](https://github.com/user-attachments/assets/840791b9-be0d-4b7f-9d0d-9f6c2e105e59)

## License

This project is open-source and can be modified and distributed freely. Feel free to modify and distribute as needed. 

---

Enjoy the game! 🎮
