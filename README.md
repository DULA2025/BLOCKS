Bejeweled-Style Match-3 Game
A simple Bejeweled-style match-3 game built using Phaser 3.80.1. The game features a 10x10 grid of colored gems, where players swap adjacent gems to create matches of three or more, earning points and triggering visual and sound effects. The game uses HTML-generated sound effects via the Web Audio API for a lightweight experience without external audio files.
Features

10x10 Grid: A fully populated grid of gems in five colors (red, blue, green, yellow, purple).
Gem Swapping: Click to select a gem and swap it with an adjacent gem (up, down, left, or right).
Match-3 Mechanics: Match three or more gems horizontally or vertically to remove them and earn points (10 points per gem).
Cascading Gems: After matches are removed, gems fall to fill empty spaces, and new gems spawn from the top.
Visual Effects:
Gems have a 3D effect with solid color fills, beveled edges, and shadows.
Explosion particle effect when gems are matched and removed.


Sound Effects:
Generated via Web Audio API (no external files needed):
Short beep for swapping gems.
Ascending tone for making matches.
Low-frequency burst for explosion effects.




Score Display: Points are displayed below the canvas in dark yellow.

Installation

copy index.html from (https://github.com/DULA2025/BLOCKS/index.html) open in browswer and play.


How to Play

Objective: Swap adjacent gems to create matches of three or more gems of the same color, either horizontally or vertically, to earn points.
Controls:
Click a gem to select it (it will scale up).
Click an adjacent gem (up, down, left, or right) to swap them.
If the swap creates a match, the gems will disappear with an explosion effect, you’ll earn points, and new gems will fall from the top.
If the swap doesn’t create a match, the gems will swap back automatically.


Scoring:
Each gem in a match is worth 10 points.
The score is displayed below the game canvas in dark yellow.


Sound Effects:
A beep plays when gems are swapped.
An ascending tone plays when a match is made.
A burst sound plays for each matched gem during the explosion effect.



Technologies Used

Phaser 3.80.1: A JavaScript game framework for rendering the game canvas, handling sprites, and managing game logic.
Web Audio API: Used to generate simple sound effects (beeps, tones, bursts) directly in the browser, eliminating the need for external audio files.
HTML5/JavaScript: Core technologies for the game structure and logic.
CSS: Basic styling for centering the game canvas and displaying the score.

File Structure
bejeweled-match3-game/
├── index.html    # Main game file containing HTML, CSS, and JavaScript
└── README.md     # This file

Customization

Sound Effects: Modify the sound generation functions (playSwapSound, playMatchSound, playExplosionSound) in index.html to adjust frequencies, durations, or oscillator types for different effects.
Example: Change oscillator.type = 'sine' to oscillator.type = 'square' for a retro sound.


Visuals: Adjust the gem colors in GEM_COLORS or the particle effects in the particles configuration to change the visual style.
Gameplay: Modify GRID_SIZE, TILE_SIZE, or the scoring system (e.g., points per gem) to alter the game difficulty or layout.

Known Issues

Sound Playback: Some browsers require user interaction to enable audio playback due to autoplay policies. The game generates sounds in response to user actions (swapping, matching), which should work in most cases, but if no sound is heard:
Ensure your browser’s audio is not muted.
Test in a different browser (e.g., Chrome, Firefox).


Performance: The game is lightweight, but generating many sound effects simultaneously (e.g., multiple explosions) might cause slight performance hiccups on low-end devices.

Future Improvements

Add a background image or gradient to enhance the visual appeal.
Implement a high score system using local storage.
Add a mute button to toggle sound effects on/off.
Introduce special gems or power-ups for additional gameplay variety.

License
This project is licensed under the MIT License. Feel free to use, modify, and distribute it as you wish.
Contributing
Contributions are welcome! Please submit a pull request or open an issue to suggest improvements or report bugs.

Created on May 13, 2025
