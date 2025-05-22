
# File Structure
(draft)

```
GameCrashEngine/
├── assets/ #(engine level)
│   ├── sprites/                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── audio/                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── fonts/                                                                            [ ] [ ] [ ] [ ] [ ]
│   └── levels/                                                                            [ ] [ ] [ ] [ ] [ ]
│
├── classes/              
│   ├── Entity.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── Actor/                                                                            [ ] [ ] [ ] [ ] [ ]
│   │   ├── Actor.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   │   └── Part/                                                                            [ ] [ ] [ ] [ ] [ ]
│   │       ├── JumpPart.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   │       ├── FlightPart.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   │       └── AttackPart.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── Item.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── Mechanism.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── Terrain.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   ├── Brain/                                                                           [ ] [ ] [ ] [ ] [ ]
│   │   ├── PlayerBrain.lua                                                                            [ ] [ ] [ ] [ ] [ ]
│   │   ├── AIBrain.lua                                                                                       [ ] [ ] [ ] [ ] [ ]
│   │   └── ScriptedBrain.lua                                                                                 [ ] [ ] [ ] [ ] [ ]
│   ├── Overlay/                                                                                              [ ] [ ] [ ] [ ] [ ]
│   │   ├── HUD.lua                                                                                           [ ] [ ] [ ] [ ] [ ]
│   │   └── Menu.lua                                                                                          [ ] [ ] [ ] [ ] [ ]
│   ├── Gamemode/                                                                                             [ ] [ ] [ ] [ ] [ ]
│   │   └── Gamemode.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│   └── Space/                                                                                                [ ] [ ] [ ] [ ] [ ]
│       ├── Space.lua                                                                                         [ ] [ ] [ ] [ ] [ ]
│       ├── TerrainLayer.lua                                                                                  [ ] [ ] [ ] [ ] [ ]
│       └── Camera.lua                                                                                        [ ] [ ] [ ] [ ] [ ]
│
├── systems/                                                                                                  [ ] [ ] [ ] [ ] [ ]
│   ├── ECS.lua                                                                                               [ ] [ ] [ ] [ ] [ ]
│   ├── MovementSystem.lua                                                                                    [ ] [ ] [ ] [ ] [ ]
│   ├── CollisionSystem.lua                                                                                   [ ] [ ] [ ] [ ] [ ]
│   ├── InputSystem.lua                                                                                       [ ] [ ] [ ] [ ] [ ]
│   ├── AnimationSystem.lua                                                                                   [ ] [ ] [ ] [ ] [ ]
│   ├── RenderSystem.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│   ├── PartSystem.lua                                                                                        [ ] [ ] [ ] [ ] [ ]
│   └── SaveSystem.lua                                                                                        [ ] [ ] [ ] [ ] [ ]
│
├── physics/                                                                                                  [ ] [ ] [ ] [ ] [ ]
│   ├── BumpPhysics.lua                                                                                       [ ] [ ] [ ] [ ] [ ]
│   ├── SlickPhysics.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│   └── PhysicsWorld.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│
├── lib/                                                                                                      [ ] [ ] [ ] [ ] [ ]
│   ├── bump/                                                                                                 [ ] [ ] [ ] [ ] [ ]
│   └── slick/                                                                                                [ ] [ ] [ ] [ ] [ ]
│
├── Game/                                                                                                     [ ] [ ] [ ] [ ] [ ]
│   ├── modes/                                                                                                [ ] [ ] [ ] [ ] [ ]
│   │   ├── mode1/                                                                                            [ ] [ ] [ ] [ ] [ ]
│   │   │   ├── entities/                                                                                     [ ] [ ] [ ] [ ] [ ]
│   │   │   ├── spaces/                                                                                       [ ] [ ] [ ] [ ] [ ]
│   │   │   ├── overlays/                                                                                     [ ] [ ] [ ] [ ] [ ]
│   │   │   ├── scripts/                                                                                      [ ] [ ] [ ] [ ] [ ]
│   │   │   └── config/ #config specific to a mode.                                                           [ ] [ ] [ ] [ ] [ ]
│   │   │       ├── controls.lua                                                                              [ ] [ ] [ ] [ ] [ ]
│   │   │       ├── settings.lua                                                                              [ ] [ ] [ ] [ ] [ ]
│   │   │       └── startup.lua #load assets for a mode here.                                                 [ ] [ ] [ ] [ ] [ ]
│   │   ├── mode2/
│   │   └── ...
│   ├── assets/ #assets are *available* irrespective of mode.                                                 [ ] [ ] [ ] [ ] [ ]
│   |   ├── sprites/                                                                                          [ ] [ ] [ ] [ ] [ ]
│   |   ├── audio/                                                                                            [ ] [ ] [ ] [ ] [ ]
│   |   ├── fonts/                                                                                            [ ] [ ] [ ] [ ] [ ]
│   |   └── cutscenes/                                                                                        [ ] [ ] [ ] [ ] [ ]
│   └── config/ #config for the overall game, overridden by modes.                                            [ ] [ ] [ ] [ ] [ ]
│       ├── controls.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│       ├── settings.lua                                                                                      [ ] [ ] [ ] [ ] [ ]
│       └── startup.lua                                                                                       [ ] [ ] [ ] [ ] [ ]
│
├── data/                                                                                                     [ ] [ ] [ ] [ ] [ ]
│   ├── saves/                                                                                                [ ] [ ] [ ] [ ] [ ]
│   └── temp/                                                                                                 [ ] [ ] [ ] [ ] [ ]
│
├── main.lua                                                                                                  [ ] [ ] [ ] [ ] [ ]
└── README.md                                                                                                 [ ] [ ] [ ] [ ] [ ]

```