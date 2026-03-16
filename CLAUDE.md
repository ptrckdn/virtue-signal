# VIRTUE SIGNAL

## What This Project Is

A third-person 3D open-world satirical action game set in Landanstan, a fictional compressed London, 2026. GTA meets The Thick of It. The player lives under the Civility Index, a social credit system monitoring speech, behaviour, and association. The game satirises every political faction and cultural sacred cow in modern Britain. Nobody gets a pass.

The tone is serious underneath the comedy. Literary influences: Dostoyevsky (fixed idea meets human face), Graham Greene (virtue from compromised people), Flannery O'Connor (grace disguised as violence), Shakespeare (moments of stillness). The comedy influences: GTA radio, The Thick of It, Brass Eye, South Park, Papers Please.

Art style: GTA III era realism. Realistic proportions, PS2-era detail level. Simple enough to build fast, serious enough to carry deep storylines. NOT low-poly cartoon. NOT stylised. Characters need faces that can act.

## Engine and Stack

- Unreal Engine 5.7
- Lumen for dynamic lighting (district atmosphere is critical)
- Nanite for geometry
- MetaHuman for key emotional characters
- Chaos Vehicle for driving physics (arcade feel, not simulation)
- UMG for all UI (phone system, HUD, menus)
- Behaviour Trees for AI (police, NPCs)
- NavMesh for pedestrian pathfinding
- Mass Entity for crowd NPCs
- Niagara for particle effects (rain, muzzle flash, etc.)

Claude Code integration via UnrealClaude plugin (MCP server on port 3000, 20+ tools for actor manipulation, Blueprint editing, level management, materials).

## Project File Structure

```
VirtueSignal/                          # UE5 project root
  CLAUDE.md                            # This file
  docs/
    VIRTUE_SIGNAL_GAME_BIBLE.md        # Single source of truth for all design
    VIRTUE_SIGNAL_UE5_BUILD_PLAN.md    # Phased build plan with time estimates
    VIRTUE_SIGNAL_COMPOSTER_ARC.md     # Complete Composter faction arc (10 missions)
    LANDANSTAN.city                    # City layout description (districts, roads, landmarks)
    DESIGN_COUNCIL.md                  # Design principles
    VIRTUE_SIGNAL_WRITERS_ROOM_PROMPT.md
    VIRTUE_SIGNAL_PHONE_SYSTEM_PROMPT.md
  Content/
    Blueprints/
      Core/                            # Game-wide singletons and managers
        BP_GameMode.uasset
        BP_GameState.uasset
        BP_PlayerCharacter.uasset
        BP_PlayerController.uasset
      CivilityIndex/                   # The meter system
        BPC_CivilityIndex.uasset       # Actor component, float 0-100
        WB_CivilityIndexHUD.uasset     # HUD widget
        WB_ComplianceStatement.uasset  # Checkbox minigame popup
      Phone/                           # Phone UI system
        BPC_Phone.uasset               # Actor component
        WB_Phone.uasset                # Main phone widget
        WB_VirtueFeed.uasset           # Twitter clone app
        WB_WhatsThat.uasset            # WhatsApp clone app
        WB_Crypt.uasset                # Telegram clone app
        WB_LandanNews.uasset           # BBC clone app
        WB_CitizenshipReport.uasset    # Government score app
      Weapons/
        BPC_Shooter.uasset             # Shooting actor component
        BPC_Health.uasset              # Health/damage actor component
        E_Weapons.uasset               # Weapon type enumeration
      Vehicles/
        BP_DrivableVehicle.uasset      # Player-drivable vehicle base
        BP_TrafficVehicle.uasset       # AI traffic vehicle (spline-following)
      Police/
        BP_PoliceAI.uasset             # Police character
        BP_AIController_Police.uasset  # AI controller with behaviour tree
        BT_Police.uasset               # Behaviour tree (patrol/chase/fire)
        BD_Police.uasset               # Blackboard
        BPI_Police.uasset              # Interface (run, walk, fire)
        Tasks/                         # BT task blueprints
      NPCs/
        BP_NPC.uasset                  # Generic civilian
        BPI_NPC.uasset                 # NPC interface (scare, react)
      Missions/
        Shared/                        # S1-S5 shared missions
        Restorationist/                # R1-R10
        Composter/                     # L1-L10
        Centrist/                      # C1-C10
      Interact/
        BPC_Interact.uasset            # Interaction component (vehicle entry, etc.)
    Characters/
      MetaHumans/                      # Key emotional characters
      VolumeCrowd/                     # Tripo AI generated crowd characters
      Animations/                      # Shared animation assets, montages
    Environments/
      Districts/                       # Per-district assets and post-process volumes
      Landmarks/                       # AI-generated landmark meshes
      Props/                           # Street furniture, CCTV, lampposts
      SevenDials/                      # London Seven Dials photogrammetry pack (modular)
    Vehicles/
      Meshes/                          # Vehicle skeletal/static meshes
      Materials/
    Audio/
      Ambience/                        # Per-district ambient loops
      Weapons/
      Vehicles/
      UI/                              # Phone sounds, meter pings
      Music/                           # Chapel gregorian chant, etc.
      Voice/                           # ElevenLabs generated dialogue
    UI/
      Icons/
      Fonts/
    Input/
      IA_Fire.uasset
      IA_Interact.uasset
      IA_Phone.uasset
      IMC_Default.uasset               # Input mapping context
    Levels/
      Landanstan_Main.umap
      Testing.umap
```

## Key Design Documents

Read these before making any design or implementation decisions:

1. `docs/VIRTUE_SIGNAL_GAME_BIBLE.md` -- THE source of truth. Contains: concept, design principles, Civility Index design (all four zones), phone system (5 apps with content), all 6 factions with characters, the chapel, 23 hot-button topics, 20 best missions, faction arc structures, Barrage controlled opposition arc, hidden virtue system, all endings. If the bible says one thing and anything else says another, the bible wins.

2. `docs/VIRTUE_SIGNAL_UE5_BUILD_PLAN.md` -- Phased build plan. 13 phases, 89-131 hours total. Contains specific Claude Code session starters and the five critical gates.

3. `docs/LANDANSTAN.city` -- City layout. Districts, roads, the Thames, bridges, landmarks, building fill rules, district atmospheres, Mission 5 route. NOTE: This file still references Unity conventions in the generation instructions at the bottom. Ignore those. Use UE5 equivalents (X = east, Y = north in UE5. Use Unreal units where 1 unit = 1 cm, so multiply all metre values by 100).

4. `docs/VIRTUE_SIGNAL_COMPOSTER_ARC.md` -- Complete left-wing faction arc. 10 missions, 5 key characters (Zane, Seren, Dele, Professor Hartley, Rio).

## The Civility Index (Core Mechanic)

This is the game's central system. Everything revolves around it. Get it right.

The meter is a comedy engine, NOT a punishment system. It runs 0-100 with four zones:

- GREEN (0-25): Boring. NPCs polite with dead eyes. Best content unavailable. The player WANTS to leave this zone.
- AMBER (26-50): The sweet spot. Where the game lives. Underground contacts appear, interesting missions unlock, police interactions are 30-second comedy sketches.
- RED (51-75): Action movie. Active pursuit. Helicopters. Big missions require RED.
- BLACK (76-100): Boss level. Triggered by specific story missions, not accumulation. Temporary (3-5 minutes, then decays). Full manhunt. Surviving earns permanent rewards.

The intended rhythm: AMBER > RED > AMBER > RED > BLACK > RED > AMBER. Like a heartbeat.

Implementation: Blueprint actor component (BPC_CivilityIndex). Single float. Broadcasts events on threshold crossings (25, 50, 75). All world systems subscribe to these events.

Going up: missions (+3 to +15), restricted areas (+1 to +5), dialogue choices (+1 to +3), CCTV detection (+1), faction association (+1 to +3).
Going down: natural decay -1 every 5 minutes, chapel healing -2 to -5, disguises (stop rise), safe houses -2, Compliance Statements -5.

## The Phone System

Replaces GTA's radio as ambient world-building. Pull up with button press. Time does NOT pause. You can get caught scrolling during a police chase.

Five apps: Virtue (Twitter clone), WhatsThat (WhatsApp clone), Crypt (Telegram clone, +10 meter to download), LandanNews (BBC clone), Digital Citizenship Report (government score app, can't delete).

All content is reactive to meter level and mission progress. See game bible Part 3 for full content specifications.

Implementation: UMG widgets. BPC_Phone actor component on player. The phone is the comedy engine. Pressmore posts every 30 seconds. Trunk reposts. Harmer committee-drafted copy. Mum's family chat. The disappeared article. All in the bible.

## The City: Landanstan

Compressed fictional London. 2.4km x 1.6km (240,000 x 160,000 Unreal units). NOT real London geography. Westminster 200m from council estates. The Shard visible from Parliament. The geographic compression IS the satire.

12 districts, each with distinct faction control, building style, lighting colour temperature, CCTV density, and atmosphere. See LANDANSTAN.city for full specifications.

The Thames runs roughly east-west across the lower third. 5 bridges act as chokepoints (police checkpoints at RED/BLACK).

Critical: the Seven Dials photogrammetry pack provides modular London building pieces (shopfronts, facades, street furniture). These get REARRANGED into Landanstan's fictional layout. They are not placed to recreate real London streets.

## Coding Conventions

### Blueprint Naming
- BP_ for actor Blueprints: `BP_PoliceAI`, `BP_DrivableVehicle`
- BPC_ for actor components: `BPC_CivilityIndex`, `BPC_Phone`, `BPC_Shooter`
- BT_ for behaviour trees: `BT_Police`
- BD_ for blackboards: `BD_Police`
- BPI_ for Blueprint interfaces: `BPI_Police`, `BPI_NPC`, `BPI_Vehicle`
- WB_ for widgets: `WB_Phone`, `WB_CivilityIndexHUD`
- E_ for enumerations: `E_Weapons`, `E_CivilityZone`
- IA_ for input actions: `IA_Fire`, `IA_Interact`, `IA_Phone`
- IMC_ for input mapping contexts: `IMC_Default`
- ABP_ for animation blueprints: `ABP_Vehicle`
- Task_ for behaviour tree tasks: `Task_Patrol`, `Task_ChaseTarget`, `Task_Fire`
- GM_ for game modes: `GM_SinglePlayer`
- PC_ for player controllers: `PC_Default`

### Architecture Principles
- Use actor components for reusable systems. BPC_Shooter, BPC_Health, BPC_CivilityIndex, BPC_Phone, BPC_Interact should all be components attachable to any actor.
- Police AI and player share BPC_Shooter and BPC_Health. Write once, attach to both.
- Use Blueprint interfaces for cross-actor communication (BPI_Police for run/walk/fire, BPI_NPC for scare/react, BPI_Vehicle for drive).
- CivilityIndex is a singleton component on the player that broadcasts events. Other systems subscribe. They don't poll.
- The phone system is pure UI. It reads game state but does not own game state.
- Missions are self-contained Blueprint actors placed in the level with trigger volumes for activation.

### C++ Usage
- Prefer Blueprints for gameplay logic. This project prioritises iteration speed.
- Use C++ only when Blueprint performance is insufficient (tick-heavy systems, large-scale NPC management).
- If writing C++, use UPROPERTY for all Blueprint-exposed variables, prefix interfaces with I (IInteractable), and always add UFUNCTION(BlueprintCallable) for functions that Blueprints need.

### General Rules
- Every system must be testable in the Testing level before integration into the main city.
- Placeholder meshes are fine. Grey boxes with correct collision are better than no collision and pretty models.
- 1 Unreal unit = 1 centimetre. When the .city file says "80m river width", that's 8000 Unreal units.
- All measurements in the .city file are in metres. Convert to centimetres for UE5.

## Characters

Two tiers:

MetaHuman (key emotional characters): Father Brennan, Margaret, Yusuf, Helen Cross, Sir Keith Harmer, Tommy Lemon, Zane Polansky, Carol Whitfield. These carry the writing. They need faces that can act.

Volume characters (Tripo AI / Mixamo): Police officers, civilians, pedestrians, faction NPCs. Generated from text prompts, rigged, animated via Mixamo or UE5 mannequin retargeting.

All characters use the UE5 mannequin skeleton (SK_Mannequin / UE5 Manny/Quinn) or are retargeted to it. This ensures animation sharing across all characters.

## Vehicles

Arcade handling. GTA III feel. Not simulation. Chaos Vehicle with:
- High engine torque
- Low tire friction for drifting
- Chase camera 8m behind, 4m above

UK-specific vehicles: black cab, red double-decker bus, police BMW X5 (battenburg), Ford Transit, Vauxhall Astra, beat-up Corsa, ambulance, delivery moped. Generated via Tripo/Meshy text-to-3D.

Vehicle enter/exit: interaction prompt near driver door, character hides, camera tweens to chase cam, vehicle controls activate. All parked and traffic vehicles should be enterable.

## Police AI

Behaviour tree with two primary states: PATROL and CHASE.

PATROL: walk between random NavMesh points within radius. Wait 3 seconds at each point. Default state.

CHASE: triggered when police sees player (Pawn Sensing component, visual angle ~85 degrees) OR hears gunfire (noise emitter on player) OR player is Wanted and visible. Run toward target, stop at ~500 units (shooting distance), fire.

Police behaviour is driven by Civility Index zone:
- GREEN: patrol only, ignore player
- AMBER: patrol, occasional stop-and-search (comedy sketch, not combat)
- RED: active pursuit, 2-3 police cars, bridge checkpoints
- BLACK: helicopter, 4-5 cars, full manhunt

Police check the player's Civility Index via BPI_Player interface before engaging.

## What NOT To Build (Scoped Out)

- Browser/WebGL version (no UE5 WebGL export; phone system is a separate React web app)
- AI dialogue / Unrestricted Speech Licence (post-launch feature, requires ElevenLabs + LLM integration)
- Faction arcs beyond Restorationist and Composter (post-demo)
- All 7 endings (post-demo; build Restorationist ending first)
- Multiplayer
- Mobile
- Procedural city generation at runtime (city is baked in editor via generation script)

## Current Build Status

Phase 0 (Driving) has not started. UE5 project needs to be created.

All design documents are complete. The writing is done. The city is designed. The build plan is written. Implementation begins now.

Priority order:
1. Chaos Vehicle on flat plane (Gate 1: does driving feel fun?)
2. One London block with Lumen lighting (Gate 2: does it feel like London?)
3. Full city generation from .city file
4. Walk/drive loop (character + vehicle entry/exit)
5. Civility Index system
6. Traffic and pedestrians
7. Phone system
8. Chapel
9. Three demo missions (Pronoun Test, Ambulance, Occupation)

## Task Scoping for Async Sessions

When working on this project via Claude Code for web (async, fire-and-forget):

- Read this file and the relevant design doc BEFORE writing any code.
- Each task should produce ONE working system or feature, not half of two.
- Create the system in the Testing level first. Integration into the main city is a separate task.
- Always create or update a test Blueprint that demonstrates the feature working.
- Commit with descriptive messages: "Phase 5: Implement CivilityIndex BPC with zone broadcasts and HUD widget"
- If a task depends on another system that doesn't exist yet, stub it with a simple interface. Don't block.
- The game bible is the authority on design intent. Don't invent new mechanics or change existing ones without explicit instruction.
- When in doubt about a design decision, choose the option that is simpler, funnier, or more like GTA III.

## Reference Implementation

The YouTube tutorial "How to Create GTA in Unreal Engine 5" (channel: Unreal University) builds a complete GTA-like game covering: motion matching locomotion, weapon overlay system, phone widget with animations, wanted star system, vehicle enter/exit, police AI with behaviour trees, traffic vehicles on splines, NPC scare reactions, and Mass AI crowds. The implementation patterns in that tutorial map closely to our Phase 0-9 systems. It uses Blueprint-only, no C++.

Key patterns from the tutorial that apply here:
- Game Animation Sample migration for motion matching (third person character)
- Actor components for modular systems (shooter, health, phone, wanted)
- Blueprint interfaces for cross-actor communication
- Behaviour trees for police AI (patrol/chase with Pawn Sensing)
- Spline-following traffic vehicles with random car model assignment
- UMG widget with open/close animations for the phone
- Sphere trace for shooting, applied damage interface for hit detection
- Skeleton mesh retargeting for multiple character models sharing one animation set

## GitHub Repository

github.com/ptrckdn/flagged-game

Main branch. No branching strategy yet. Claude Code for web sessions should create feature branches and open PRs.
