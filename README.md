# Locked Doors — Gameplay Systems Prototype

**Unreal Engine 5.4 | Blueprints | First-person interaction and environmental puzzles**

*Locked Doors* is a coursework-based gameplay prototype and a work-in-progress puzzle-game concept. It demonstrates interactive objects, physics-driven puzzle mechanics, reusable Blueprint actors, and an explorable level. It is **not a completed or commercially released game**.

## Project overview

The player explores rooms, moves objects, and uses color-coded cubes and pressure plates to unlock doors. The original GAM-303 project was revisited for GAM-495 to make puzzle interactions clearer and improve the presentation and structure of the level.

### Implemented systems

- First-person movement, jumping, and left-mouse-button interaction
- Blueprint interaction interface for doors, furniture, and puzzle objects
- Contextual **LMB – Interact** HUD prompt, displayed when looking at an actor that implements the interaction interface
- Physics-based pickup, dropping, and pressure-plate puzzle interactions
- Colored puzzle cubes, unlocking doors, and progression toward an exit
- Reusable interactive furniture, including a cupboard assembled from child actor components and a chest of drawers
- Configurable material colors for furniture and environmental objects
- A main-menu level with Play, Controls, Credits, and Quit options

**Interaction-prompt limitation:** The current prompt identifies objects that implement the interaction interface; it does not yet account for every object's locked, open, or otherwise unavailable state.

## GAM-495 refinement

The refinement plan focused on clearer puzzle progression, more reliable interactions, better player guidance, and testing the door/puzzle flow. The revised version includes:

1. **Level redesign:** Reworked the room layout and expanded the furnished environment while keeping the focus on gameplay systems.
2. **Reusable furniture:** Organized cupboard doors and drawers into reusable Blueprint actor assemblies rather than repeatedly placing separate pieces.
3. **Customizable materials:** Added parameterized color materials for furniture and surfaces.
4. **Contextual player feedback:** Added an on-screen interaction prompt using a camera-forward line trace and the existing Blueprint interaction interface.
5. **Puzzle review:** Revisited and tested color-block and door interactions in the updated level.

The main-menu controls and rules remain available to explain the objective. The project intentionally retains simple geometry and visual styling so the focus stays on gameplay programming rather than finished art.

## Updated gameplay demonstration

[Watch the refined Locked Doors gameplay demonstration](Locked_Doors_Refined_Demo_720p.mp4)

The video shows the current prototype rather than the earlier GAM-303 level.

## Screenshots — refined version

### Contextual interaction prompt

![Interaction prompt displayed while looking at the chest of drawers](Screenshot%202026-11-12%20223513.png)

### Main menu

![Main menu with Play, Controls, Credits, and Quit buttons](Screenshot%202026-11-12%20223616.png)

### Interactive cupboard and hidden cube

![Open cupboard showing a red puzzle cube](Screenshot%202026-11-12%20223652.png)

### Cube-operated door puzzle

![Red cube on a pressure plate near an opened doorway](Screenshot%202026-11-12%20223711.png)

## Tools and demonstrated skills

| Tools | Skills demonstrated |
| --- | --- |
| Unreal Engine 5.4 | Engine workflow, level layout, and gameplay prototyping |
| Blueprints and Blueprint Interfaces | Modular actors, event-driven interactions, and puzzle logic |
| UMG | Main-menu and contextual interaction UI |
| Unreal Engine materials and modeling tools | Reusable furniture, customizable materials, and prototype environments |
| Git and GitHub | Version control, feature branches, merges, and documentation |

## Open and test

1. Install **Unreal Engine 5.4**.
2. Clone or download this repository.
3. Open `MyProject.uproject` in Unreal Engine.
4. Open the **MainMenu** level to start with the menu; if opening the gameplay map directly, use **FinalProject**.
5. Use **Play In Editor** to try the movement, furniture interactions, and color-block puzzles.

The creator has tested the key gameplay interactions in the updated level. The repository contains the Unreal project sources and assets, **not a packaged standalone game**.

## Development and learning

The original coursework established the interaction and puzzle systems; the GAM-495 iteration focused on improving the player experience and making the project easier to demonstrate. Adding contextual prompts required investigating Blueprint interfaces, nested actors, collision detection, and camera line traces. One particularly useful debugging lesson was correcting a vector-by-vector multiplication that unintentionally zeroed parts of the camera direction; multiplying the forward vector by a single distance value fixed unreliable detection.

The redesigned furniture also provided practice with Child Actor Components and material parameters. The separate portfolio repository retains a cleaner project history, while the original academic version is preserved privately.

## Scope and attribution

This is an educational prototype created as coursework by Ryan Mills and later refined for GAM-495 with development assistance. Unreal Engine and any engine-provided assets remain subject to Epic Games' applicable terms; this repository does not grant rights to third-party assets.

**Publication status:** Kept private pending review of course requirements and any applicable asset redistribution restrictions.
