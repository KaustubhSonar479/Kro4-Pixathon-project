## Tools Used For Code And Logic
1) Chat gpt used for ideas, logic and prompt
2) lovable.dev for game developement
3) Bolt ai used for game prototype 
4) Stich for UI design
## Key Prompts for game 
1. "Build a 2.5D browser puzzle platformer called 'Think Beyond' with Three.js, deterministic physics, and neon-noir aesthetic." -> *Core Loop & Engine*
2. "Implement Level 1 ('The Lying Floor') where platforms labeled SAFE crack and fall, while DANGER platforms are solid." -> *Mechanics (Level 1)*
3. "Implement Level 2 gravity switch triggered by pressing 'E' on an interactable pedestal, inverting player jumping and Y velocity." -> *Mechanics (Level 2)*
4. "Rework Level 3 Memory Trap: make the pattern more forgiving and dynamically generate a randomized illuminated false path on each level load/restart." -> *Puzzle Polish & Dynamic Levels*
5. "Create a zero-dependency Web Audio API sound synthesizer for procedural ambient music, jump blips, gravity hum, and death glitch sound." -> *Audio Engine*
6. "Add an ancient-stone Dungeon Devil styled title menu, death counter HUD, and a 60-second replayable victory sequence." -> *UI & Game Juice*

## When AI Got It Wrong 
* **The Issue:** The procedural level generator for Level 3 initially randomized traps without checking if an alternate open path remained passable, occasionally making the gap between safe platforms wider than the player's maximum jump distance.
* **How We Caught It:** Playtesting failed repeatedly on seed iterations where two adjacent rows were both blocked by generated traps.
* **The Fix:** Added a path-validation rule guaranteeing at least one safe platform per column with horizontal jump gap $\le 3.5$ units.

## Key Prompts for ui 
1. "Build a 2.5D browser puzzle platformer called 'Trust Nothing' with Three.js, deterministic physics, and neon-noir aesthetic." -> *Core Loop & Engine*
2. "Upgrade the main menu UI to a neon-fantasy 2.5D dungeon aesthetic: #080B12 charcoal stone, cyan (#00E5FF) and electric purple (#A855F7) magical runes, torchlight contrast, medieval distressed typography, and a 4-button vertical stack with cut-corner borders." -> *Feel & Design (UI)*
3. "Implement Level 1 ('The Lying Floor') where platforms labeled SAFE crack and fall, while DANGER platforms are solid." -> *Mechanics (Level 1)*
4. "Implement Level 2 gravity switch triggered by pressing 'E' on an interactable pedestal, inverting player jumping and Y velocity." -> *Mechanics (Level 2)*
5. "Rework Level 3 Memory Trap: make the pattern more forgiving and dynamically generate a randomized illuminated false path on each level load/restart." -> *Puzzle Polish & Dynamic Levels*
6. "Create a zero-dependency Web Audio API sound synthesizer for procedural ambient music, jump blips, gravity hum, and death glitch sound." -> *Audio Engine*

## When AI Got It Wrong
* **The Issue:** When prompted to design the title screen, the AI generated a SaaS landing page layout featuring rounded pill buttons, white cards, and full-screen gradient blur rather than an atmospheric PC game main menu.
* **How We Caught It:** Visual inspection showed standard web elements that broke the dark dungeon immersion.
* **The Fix:** Reprompted with strict constraints: removed rounded corners, enforced cut-corner borders, added CSS letter-spacing and text-shadow glows, and layered in stone background textures and torchlight contrast.

##Game link 
https://thinkkbeyondd.lovable.app
