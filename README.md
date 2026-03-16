# Virtue Signal

A third-person 3D open-world satirical action game set in **Landanstan**, a fictional compressed London, 2026. GTA meets *The Thick of It*. The player lives under the **Civility Index**, a social credit system monitoring speech, behaviour, and association. The game satirises every political faction and cultural sacred cow in modern Britain. Nobody gets a pass.

Art style: GTA III-era realism. Serious enough to carry deep storylines, simple enough to build fast.

## Core Mechanic: The Civility Index

A 0-100 meter with four zones that reshape the entire game world:

| Zone | Range | Feel |
|------|-------|------|
| GREEN | 0-25 | Boring compliance. NPCs polite with dead eyes. Best content locked. |
| AMBER | 26-50 | The sweet spot. Underground contacts, interesting missions, comedy police sketches. |
| RED | 51-75 | Action movie. Active pursuit, helicopters, bridge checkpoints. |
| BLACK | 76-100 | Full manhunt. Triggered by story missions. Temporary. Surviving earns permanent rewards. |

## Tech Stack

| Layer | Tool |
|-------|------|
| Engine | Unreal Engine 5.7 |
| Lighting | Lumen (dynamic, per-district atmosphere) |
| Geometry | Nanite |
| Key Characters | MetaHuman |
| Vehicle Physics | Chaos Vehicle (arcade, not sim) |
| UI | UMG (phone system, HUD, menus) |
| AI | Behaviour Trees + NavMesh + Mass Entity |
| Particles | Niagara |
| AI Coding | Claude Code + UnrealClaude MCP plugin |
| Voice | ElevenLabs |
| 3D Generation | Tripo AI / Meshy (characters, vehicles, landmarks) |

## Build Phases

| Phase | Description | Est. Hours |
|-------|-------------|------------|
| 0 | Driving -- Chaos Vehicle on flat plane, arcade tuning | 2-4 |
| 1 | One London Block -- Lumen lighting, rain, atmosphere test | 3-5 |
| 2 | Landanstan City Generation -- Full 2.4km x 1.6km city from .city file | 6-10 |
| 3 | Walk/Drive Loop -- Character movement + vehicle enter/exit | 4-6 |
| 4 | Characters -- 5 MetaHumans + 10 Tripo volume characters | 8-12 |
| 5 | Civility Index -- Meter system, zone broadcasts, HUD, CCTV detection | 8-12 |
| 6 | Traffic & Pedestrians -- AI vehicles on splines, NavMesh pedestrians | 8-12 |
| 7 | Phone System -- 5 reactive apps (Virtue, WhatsThat, Crypt, LandanNews, Citizenship Report) | 12-16 |
| 8 | The Chapel -- Father Brennan, healing mechanic, the bell | 4-6 |
| 9 | Three Demo Missions -- Pronoun Test, The Ambulance, The Occupation | 18-24 |
| 10 | AI Landmarks -- Parliament, The Shard, Tower Bridge, etc. | 4-6 |
| 11 | AI Vehicles -- Black cab, double-decker, police BMW, Transit, etc. | 4-6 |
| 12 | Sound & Polish -- Per-district ambience, sirens, rain, UI sounds | 6-10 |

**Total estimate: 89-131 hours.** Five critical gates determine go/no-go at key milestones.

## The City: Landanstan

Compressed fictional London -- 2.4km x 1.6km. Westminster 200m from council estates. The Shard visible from Parliament. 12 districts, each with distinct faction control, building style, lighting, and CCTV density. The Thames runs east-west with 5 bridges as police chokepoints. The geographic compression IS the satire.

## Design Documents

| Document | Description |
|----------|-------------|
| [Game Bible](docs/virtue_signal_game_bible.md) | **The source of truth.** Concept, Civility Index, phone system, 6 factions, 23 hot-button topics, 20 best missions, all endings. |
| [UE5 Build Plan](docs/VIRTUE_SIGNAL_UE5_BUILD_PLAN.md) | 13 phases, time estimates, critical gates, Claude Code session starters. |
| [Landanstan City Layout](docs/LANDANSTAN.city) | District definitions, roads, Thames, bridges, landmarks, building fill rules, atmospheres. |
| [Composter Arc](docs/VIRTUE_SIGNAL_COMPOSTER_ARC.md) | Complete left-wing faction arc. 10 missions, 5 key characters. |
| [Restorationist Practical](docs/virtue_signal_restorationist_practical.md) | Restorationist faction implementation details. |
| [Design Council](docs/DESIGN_COUNCIL.md) | Design principles from top game designers, applied per-system. |
| [Phone System Prompt](docs/VIRTUE_SIGNAL_PHONE_SYSTEM_PROMPT.md) | Phone system content generation spec. |
| [Phone Content](docs/virtue_signal_phone_content.md) | Written phone app content. |
| [Writers Room Prompt](docs/VIRTUE_SIGNAL_WRITERS_ROOM_PROMPT.md) | Writing guidelines and tone reference. |
| [Two Faction Launch](docs/virtue_signal_two_faction_launch.md) | Scoped launch plan with Restorationist + Composter arcs. |
| [The Grid](docs/virtue_signal_grid.md) | Mission/topic cross-reference grid. |
| [Master & Margarita](docs/virtue_signal_master_margarita.md) | Literary analysis and structural inspiration. |
| [The Gym Mission](docs/virtue_signal_mission_the_gym.md) | Detailed mission design for The Gym. |

## Current Status

**Pre-implementation.** All design documents are complete. Phase 0 (Driving) is the next step.

## Contributing

Feature branches and PRs via Claude Code for web. Each task should produce one working system, tested in the Testing level before city integration. See [CLAUDE.md](CLAUDE.md) for full coding conventions and session guidelines.
