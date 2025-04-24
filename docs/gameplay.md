# Gameplay Systems

## Table of Contents
- [Core Loop](#core-loop)
- [Controls Snapshot](#controls-snapshot)
- [Player Systems](#player-systems)
  - [Buffer (Health System)](#buffer-health-system)
  - [Glitch Powers](#glitch-powers)
  - [Debug Console](#debug-console)
  - [Restoration Lens](#restoration-lens)
- [Memory Leak Hazards](#memory-leak-hazards)
- [Backdoor System](#backdoor-system)
- [Progression Design](#progression-design)
- [Bug Bounty System](#bug-bounty-system)

## Core Loop

1. **EXPLORE**: Navigate through corrupted game-worlds, platforming and solving puzzles
2. **COLLECT**: Gather Buffs (health extensions) and debug fragments (collectibles)
3. **RESTORE**: Clear corruption nodes to gradually restore sections of each world
4. **CONFRONT**: Battle the world's Guardian (boss)
5. **ACQUIRE**: Gain the Guardian's Glitch Power upon victory
6. **WITNESS**: Watch the world heal in real-time (transition from glitched to restored visuals)
7. **PROGRESS**: Use new powers to access previously unreachable areas in other worlds

## Controls Snapshot

| Action | Input |
|--------|-------|
| Move / Jump | D-pad / A |
| Basic Attack | X |
| Use Glitch Power | Y (tap) / Hold to charge |
| Switch Power | Shoulder buttons |
| Enter Backdoor | Up + Y at fracture |
| Debug Console | B + Y |
| Quick Restart | Select + Start |

## Player Systems

### Buffer (Health System)
- HP bar visualized as a digital buffer meter
- Damage corrupts the buffer; healing restores it
- Collect Buffer Extensions (Buffs) to increase maximum capacity
- Special "Clean Code" resources flow from restored areas to provide temporary buffer boosts
- Restored sections generate passive buffer regeneration in their vicinity
- Visual feedback: Buffer integrity shown through decreasing glitch effects on Patch

### Glitch Powers
- Abilities gained from restored Guardians
- Both combat and traversal applications
- Can be combined for enhanced effects
- Powered by a regenerating Energy meter
- Advanced combinations unlock as more powers are acquired

### Debug Console
- Limited-use special ability that reveals the "code beneath the world"
- Temporarily highlights hidden paths, enemy weaknesses, and puzzle solutions
- Shows corruption nodes and restoration opportunities
- Creates a matrix-like view of the environment's true structure
- Strategic resource with cooldown timer

### Restoration Lens
- Real-time visual shift as areas are restored
- Transition from glitch art to pristine assets
- Accompanied by audio shifts from distorted to clean
- Creates powerful feedback loop for player progression
- Restoration spreads outward in visible waves from cleared nodes

## Memory Leak Hazards
- Environmental challenges that grow stronger the longer players remain in an area
- Visualized as increasing corruption that spreads from specific sources
- Creates urgency and rewards efficient exploration
- Different types require different strategies to counter
- Advanced levels feature memory leaks that can only be temporarily contained
- Strategic resource management becomes critical in heavily leaked areas

## Backdoor System

### Concept Overview
Backdoor Rooms represent secure access points where the Supervisor (ARCH-OS) can safely communicate with Patch away from Hack's corruption influence. These hidden chambers serve multiple gameplay and narrative functions:

- Story Development: The Supervisor gradually reveals the truth about the system, Patch's purpose, and Hack's origin
- Guidance System: Provides hints about upcoming challenges and how to use newly acquired powers
- Upgrade Mechanism: Offers enhancement modules for Patch's abilities and buffer capacity
- Safe Zones: Areas where the player can experiment with powers without enemy threats
- Collection Showcase: Displays collected Memory Fragments and other achievements

### Visual Design
- Backdoor Rooms appear as fractured "glitches" in the environment that shimmer subtly
- Inside, they manifest as clean, minimalist digital spaces with a blue-white aesthetic
- The Supervisor appears as a serene holographic interface with flowing code patterns
- Collected items and unlocked enhancements are displayed on virtual pedestals
- Small "windows" sometimes show glimpses of other connected worlds

### Access Mechanics
- Players locate hidden fractures in each world (approximately 3-5 per world)
- Accessing requires a specific input (Up + Y when near a fracture)
- Some backdoors are in plain sight while others require exploration or puzzle-solving
- Certain backdoors only become visible after acquiring specific powers
- Fast-travel network allows revisiting previously discovered backdoors

### Enhancement Types
- Buffer Extensions: Increases maximum health capacity, enhances recovery rate, provides specialized defensive capabilities
- Power Amplifiers: Extends duration of power effects, reduces energy consumption, adds secondary functions to existing powers
- System Utilities: Map function, memory scanner, corruption detector, emergency teleport
- Specialized Modules: World-specific enhancements, combination catalysts, passive abilities like double-jump, air-dash, or wall-slide

### Narrative Integration
- Early backdoors provide basic instruction and context
- Mid-game backdoors reveal deeper lore about the system and worlds
- Late-game backdoors expose the connection between Patch and Hack
- Final backdoors prepare Patch for the ultimate confrontation and potential reintegration

### Progression Design
- First backdoor is part of the tutorial
- Each world contains at least one "essential" backdoor
- Optional backdoors contain helpful but non-essential enhancements
- Special "deep access" backdoors require combining multiple powers to reach
- System Core contains the ultimate backdoor revealing the complete truth before the final battle

## Progression Design
- Non-linear World Selection: Players can tackle worlds in various orders
- Soft Gating: Certain areas require specific powers to access, suggesting an optimal path
- Retraversal Incentives: New powers open previously inaccessible areas in completed worlds
- Difficulty Scaling: Worlds have recommended order but adapt to player's current power level
- Ability Synergy: Later worlds feature puzzles requiring creative combinations of powers

## Bug Bounty System
- Optional secondary objectives in each world
- Tasks players with finding and fixing specific "bugs" beyond the main corruption
- Each completed bounty rewards unique upgrades or cosmetic effects
- Bounties escalate in complexity throughout the game
- Some require combinations of multiple powers to resolve
- Completing all bounties in a world enhances its Guardian's power 