# 2D World Engine Overview
These abstractions help shape the interaction between players, items, rooms, and challenges within the virtual environment.
#### Phase 1: World Generation
- Implement a random world generator that creates different but reproducible maps based on a given seed value.
- The generated world should be stored and returned as the output(`saveWorld` and `loadWorld`).
- Create entities such as our user avatars and items implemented in 2-D virtual worlds(`Player`,`Room`, `Monster`.etc).
#### Phase 2: Interactivity
- Introduce a player avatar that can move using `WASD` controls.(North, South, East and West).
- Implement game saving and loading functionality.
- Implement avatar's interaction behaviors with accessible objects in the room.
#### Additional Features:
- A main menu allowing players to select New Game (N), Load Game (L), and Quit (Q).
## 📌 Breakdown
### 🧙🏻Player(Avatar)
The one and only we control form command line window to interact with the current virtual world.
**Attributes**:
- **Score**: Based on collected items and solved puzzles.
- **Health**: Ranges from **100 to 0**; dropping to **0** causes the player to "sleep."
- **Inventory**: Contains items, but has a **weight limit**.
**Actions**:
- Moves **North, South, East, West** between rooms.
- Picks up, drops, and uses items.
- Encounters **Monsters** and **Puzzles**.
###  🏹Room
Defines spaces that the player can walk through or between the open pathways.
- Includes: fixtures(non-interactive), items, puzzles and monster(interactive).
- Players cannot walk through walls, items, fixtures, puzzles and monsters.
