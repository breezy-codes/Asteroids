<p align="left">
    <img width="150px" src="https://github.com/thoth-tech/.github/blob/main/images/splashkit.png"/>
</p>

[![GitHub contributors](https://img.shields.io/github/contributors/thoth-tech/Asteroids?label=Contributors&color=F5A623)](https://github.com/thoth-tech/Asteroids/graphs/contributors)
[![GitHub issues](https://img.shields.io/github/issues/thoth-tech/Asteroids?label=Issues&color=F5A623)](https://github.com/thoth-tech/Asteroids/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/thoth-tech/Asteroids?label=Pull%20Requests&color=F5A623)](https://github.com/thoth-tech/Asteroids/pulls)
[![Forks](https://img.shields.io/github/forks/thoth-tech/Asteroids?label=Forks&color=F5A623)](https://github.com/thoth-tech/Asteroids/network/members)
[![Stars](https://img.shields.io/github/stars/thoth-tech/Asteroids?label=Stars&color=F5A623)](https://github.com/thoth-tech/Asteroids/stargazers)

# Asteroids 1.0

**Asteroids** is a top-down single player or co-op shooter that has you, the player, flying around and surviving an onslaught of rocks, and if you survive long enough, even bosses! Aim for a high score, don't lose your hearts before your friend, and manoeuvre around dangers and rack up that score!

## Game Overview

In **Asteroids**, you control a spaceship, dodging and shooting down waves of asteroids that fly across the screen. This game can be played solo or with a friend in co-op mode. The objective is simple: rack up points by destroying asteroids and bosses while avoiding collisions. Survive as long as possible and aim for the highest score!

## Running the Game

Ensure you have the latest version of the **SplashKit** library installed on your system. If you haven't installed **SplashKit**, follow the instructions in the [**SplashKit Installation Guide**](https://splashkit.io/installation/).

To launch the game, follow these steps:

1. **Navigate to the Game Directory**:
   - Open the MSYS2 terminal.
   - Change to the game directory by entering:
  
     ```bash
     cd '{path-to-asteroids-directory}'
     ```

     Replace `{path-to-asteroids-directory}` with the actual path where the **Asteroids** folder is located.

2. **Run the Game**:
   - Start the game by typing:

     ```bash
     skm dotnet run
     ```

   - The game will launch directly from the terminal.

## Basic Controls

All menu navigation and game controls are primarily set to Player 1 unless otherwise specified. The `ESC` key can be used anytime to exit the game.

### Player 1 Controls

| Key         | Action        |
|-------------|---------------|
| Up Arrow    | Move Forward  |
| Left Arrow  | Rotate Left   |
| Right Arrow | Rotate Right  |
| Ctrl        | Fire          |

### Player 2 Controls

| Key      | Action        |
|----------|---------------|
| S or R   | Move Forward  |
| D        | Rotate Left   |
| G        | Rotate Right  |
| A        | Fire          |

## Game Configuration

The configuration files for **Asteroids** can be found in the `/Resources/json` folder, where `Controls.json` and `Game_Config.json` allow for game customization:

### Key Configuration Files

1. **`Controls.json`**: Contains the key mappings used in **Asteroids**. This file can be edited to customize player controls.

2. **`Game_Config.json`**: Houses various settings that affect gameplay, display, and visual scaling.

   ```bash
    "fullscreen": true,
    "gameScale": 0.6,
    "no_boarder": false,
    "screen_height": 540,
    "screen_width": 960
    ```

3. The breakdown of the parameters in `Game_Config.json` is as follows:

   - **`fullscreen`**: Determines whether the game launches in full-screen mode (`true` for fullscreen, `false` for windowed).
   - **`gameScale`**: Adjusts the overall scaling of visual elements. If modified, ensure `screen_height` and `screen_width` are adjusted proportionally for visual fidelity.
   - **`no_boarder`**: When `fullscreen` is set to `false`, this parameter controls whether the standard window border (with minimize, maximize, and close buttons) is shown (`false`) or hidden (`true`).
   - **`screen_height` and `screen_width`**: Set the dimensions of the game window.

### Example Screen Resolutions and Game Scales

Below are examples of base game scale configurations. If you change `gameScale`, ensure `screen_height` and `screen_width` align to maintain consistent gameplay visuals:

- **Full Resolution**: `1600 x 900` (game scale `1`)
- **80% Resolution**: `1280 x 720` (game scale `0.8`)
- **60% Resolution**: `960 x 540` (game scale `0.6`) - current setting

For example:

```plaintext
Full res:                   1600 x 900,   game scale:     1
80% res:                    1280 x 720,   game scale:     0.8  →   1600*0.8 || 900*0.8
60% res: (current setting)  960 x 540,    game scale:     0.6  →   1600*0.6 || 900*0.6
```
