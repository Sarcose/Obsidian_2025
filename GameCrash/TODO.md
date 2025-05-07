## 1. Core Foundations

-  Set up base project structure (assets/, classes/, systems/, config/, etc.)
-  Create `Entity` base class
-  Create `Space` base class (recursive space structure)
-  Create `Game` base class for game modes
- Create basic input handler (Input → Brain concept)
--

## 2. Identity Layer (Classes)

- Define `Actor` class (dynamic entities)
- Define `Item` class (passive pickups)
- Define `Mechanism` class (invisible scene logic)
- Define `Terrain` class (static geometry management)
- Define `Part` system (modular behavior attached to Actors)
- Define `Brain` abstraction (controllers for Actors and Players)
- Define `Overlay` base class for UI elements

## 3. Core Systems (ECS Layer)

-  Implement minimal ECS world (Entities, Components, Systems
-  Create MovementSystem (process velocity, apply forces)
-  Create CollisionSystem (integrate with physics backend)
-  Create RenderSystem (draw entities and terrain)
-  Create InputSystem (translate player input → movement/interaction intent)
-  Create AnimationSystem (optional for visual updates)

## 4. Physics Layer

-  Integrate `Bump` (AABB) physics system
-  Build physics interface abstraction (`PhysicsWorld`)
-  (Optional) Plan future `Slick` backend integration
## 5. Modular Layer (Patterns and Parts)

-  Implement Part attachment system for Actors
-  Build system to load/configure Patterns (data-driven entity setups)
-  Define a "recipe format" (e.g., Lua tables, JSON)
## 6. Spaces and World Structure

-  Allow Spaces to contain Entities
-  Allow Spaces to nest other Spaces
-  Manage ECS world per Space
-  Manage Physics world per Space
-  Build basic Space traversal API (moving Actors between Spaces)

## 7. Terrain System

-  Implement `TerrainLayer` within Spaces
-  Define Terrain shapes and collision proxy objects
-  Allow dynamic terrain modifications (optional: delayed until later)
-  Terrain queries (solid at point? overlap tests?)
## 8. UI and Overlay Systems

-  Build passive HUD system (UI reads ECS snapshot, never mutates
-  Overlay management system (menus, HUDs, popups)
-  Basic Camera system (centered on Actor, scalable)
## 9. Save/Load System

-  Define serialization contracts for:
    - ECS world state
    - Physics world state
    - Space structure
    - Entity modular Parts
-  Implement SaveSystem and LoadSystem
## 10. Game Mode/Scenario Bootstrapping

-  Define game mode document structure (gamemode config files)
-  Implement GameLoader to read and initialize based on document
-  Allow spaces, entities, overlays to be loaded/configured at game start
## Optional Phase: Future Systems

-  Pathfinding system (for RTS-style gameplay)
-  Selection/Grouping system (for RTS/multiplayer modes)
-  Fog of War/visibility system
-  Procedural generation system for levels or worlds
-  Dynamic construction/building system
-  Multiplayer handling (split input and multiple Brains)


## Notes

- Start simple: MVP = single Actor, single Space, static terrain, movement + collision.
- Build ECS and basic movement before modular Parts
- Physics integration should stay thin and replaceable.
- Serialization and save/load must be explicit per system.
- Modular behavior (Parts) must be truly declarative.