# VIRTUE SIGNAL: Unreal Engine 5 Build Plan
## ASAP Timeline

---

## Setup (Tonight, While UE5 Installs)

While Unreal downloads (~30-50GB), do these in parallel:

1. **Sign up for Tripo AI** ($20/month) - https://www.tripo3d.ai/
2. **Sign up for Midjourney** ($10/month) - character and building concept art
3. **Sign up for 3DAI Studio** ($14/month) - multi-model access for props
4. **Download Mixamo** account (free) - https://www.mixamo.com/
5. **Install UnrealClaude plugin** - https://github.com/Natfii/UnrealClaude
   This gives Claude Code direct access to the UE5 editor: actor spawning, Blueprint editing, level management, materials, 20+ MCP tools
6. **Buy City Builder: London from Fab** ($25) - https://www.fab.com/listings/ee3da367-42cd-412b-bd9f-89c0c9c891de
   Check Fab (Epic's marketplace) for UE5 version. If not available, the prefabs still import via FBX.
7. **Put these files in your project root:**
   - LANDANSTAN.city (already written)
   - VIRTUE_SIGNAL_GAME_BIBLE.md (already written)
   - VIRTUE_SIGNAL_COMPOSTER_ARC.md (already written)
   - DESIGN_COUNCIL.md (already written)

---

## The Stack

| Layer | Tool | Why |
|-------|------|-----|
| Engine | Unreal Engine 5.7 | Lumen lighting, Nanite geometry, MetaHuman faces, best visual quality |
| AI coding | Claude Code + UnrealClaude plugin | Natural language to editor commands, 130+ operations |
| City generation | Claude Code reads .city file, generates via CLAUDIUS/UnrealClaude | Procedural placement from description |
| Buildings | City Builder: London prefabs + AI-generated landmarks (Meshy/Tripo) | London-specific architecture |
| Characters | Tripo (text-to-rigged-3D) + Mixamo (animations) OR MetaHuman (key characters) | Realistic proportions for serious tone |
| Vehicles | Tripo/Meshy text-to-3D (black cab, police BMW, bus, etc.) | UK-specific vehicles don't exist on marketplaces |
| Vehicle physics | Chaos Vehicle (UE5 built-in) or marketplace equivalent | Built into engine |
| Writing | Already done (game bible, arcs) | The hard work is finished |
| Voice | ElevenLabs AI voice generation | Key characters only |
| Sound | Freesound.org + AI generation | Ambient London, sirens, rain, the bell |

---

## Phase 0: Driving (Day 1)

**Goal:** A car driving around a flat plane in UE5. Chase camera. Does it feel like GTA III?

**Actions:**
1. Create new UE5 project (Third Person template, Lumen enabled)
2. Claude Code via UnrealClaude: "Create a flat ground plane 500m x 500m. Add a Chaos Vehicle with arcade handling. Chase camera 8m behind, 4m above. WASD + mouse controls. Make the car slide on turns."
3. UE5 has Chaos Vehicle built in. Tune for arcade feel: reduce tire friction, increase engine torque, add drift threshold
4. Drive. Tune. Drive. Tune.

**Gate:** Does it feel fun? If yes, proceed. If no, tune until it does.

**Time:** 2-4 hours

---

## Phase 1: One London Block (Day 1-2)

**Goal:** One city block with London buildings. Drive through it. Does it feel like London?

**Actions:**
1. Import City Builder: London assets into UE5
2. Claude Code: "Build a crossroads. Two roads, 14m wide, crossing at centre. Place London brick terrace buildings along all four road edges, 3-4 storey. Add pavements. Add 4 lampposts. Add 2 CCTV cameras on building corners."
3. Enable Lumen. Set overcast sky. Add light fog. Set colour grading to desaturated cold blue-grey.
4. Add rain particle system (UE5 Niagara, plenty of free templates on Fab)
5. Add wet road material (UE5 has built-in wet surface shaders)
6. Night mode: sodium orange street lights, blue-white CCTV LEDs, building windows lit via City Builder's interior mapping shader

**The atmosphere test:** Drive through this block at night in the rain with Lumen lighting. Does it feel oppressive? Does it feel like Landanstan? Lumen does the heavy lifting here.

**Time:** 3-5 hours

---

## Phase 2: Landanstan City Generation (Day 2-4)

**Goal:** The full 2.4km x 1.6km city. Driveable. Districts feel different.

**Actions:**
1. Claude Code reads LANDANSTAN.city
2. Generates a Python/Blueprint editor script that:
   - Lays road splines from the .city road definitions
   - Extrudes road meshes along splines (UE5 Spline Mesh Component)
   - Places City Builder: London prefabs along roads per district rules
   - Creates the Thames as a water plane with river material
   - Places bridge meshes at defined positions
   - Sets Lumen lighting per district (Post Process Volumes per zone)
   - Adds CCTV placeholder meshes at density defined per district
   - Adds parked vehicles along roads
   - Adds lampposts
3. Run generator. Screenshot. Fix. Iterate.
4. Place landmark placeholder cubes at defined positions (with labels: "PARLIAMENT", "THE SHARD", etc.)

**District lighting (Lumen does this beautifully):**
- Westminster: cold blue-white, harsh LED, maximum visibility
- Mayfair: warm white, ornate fixtures, gentle
- The City: blue corporate, glass reflections
- Shoreditch: warm orange, industrial pendants
- Brixton: sodium orange, residential warmth
- Elephant & Castle: cold sodium, concrete echo
- Canary Wharf: sterile blue-white, wind between towers

**Time:** 6-10 hours (this is the biggest single task)

---

## Phase 3: Walk/Drive Loop (Day 4-5)

**Goal:** Player walks, enters cars, drives, exits cars. The GTA loop.

**Actions:**
1. Third Person Character (UE5 template gives you this)
2. Vehicle enter/exit: Area trigger near cars, interaction prompt, character hides, camera tweens to chase cam, vehicle controls activate
3. Reverse to exit: character appears at driver door
4. All parked cars and traffic cars are enterable
5. Camera system: on foot (spring arm, 5m behind) and in vehicle (spring arm, 8m behind, velocity tracking)

**UE5 advantage:** The Third Person template already has walking, running, jumping. You're adding vehicle entry on top of a working character, not building from scratch.

**Time:** 4-6 hours

---

## Phase 4: Characters (Day 5-7)

**Goal:** Key characters exist in the world. They can carry the writing.

**Two paths, use both:**

**Path A: MetaHuman (for key emotional characters)**
- Father Brennan, Margaret, Yusuf, Helen Cross, Sir Keith Harmer
- MetaHuman Creator is free, built into UE5
- Create faces that can act. These characters carry Dostoyevsky weight.
- 30-60 minutes per character in MetaHuman Creator
- Import to project, apply Mixamo or UE5 mannequin animations

**Path B: Tripo AI (for volume characters)**
- Police officers, civilians, pedestrians, faction NPCs
- Text prompt to rigged humanoid in minutes
- Import FBX, apply animations
- 10-15 minutes per character

**For the demo:** 5 MetaHumans (key characters) + 10 Tripo characters (crowds, police, traffic). Total: maybe 8-10 hours across two days.

**Time:** 8-12 hours

---

## Phase 5: Civility Index (Day 7-8)

**Goal:** The meter. GREEN/AMBER/RED/BLACK. The world changes.

**Actions:**
1. Blueprint singleton: CivilityIndex. Float 0-100. Broadcasts events on threshold crossings.
2. HUD widget: vertical colour bar, zone name, notification popups
3. CCTV detection: rotating cone (spot light + overlap volume), triggers +1 on detection
4. District-based triggers: entering Westminster = faster accumulation
5. Natural decay: -1 every 5 minutes
6. Zone behaviours:
   - GREEN: NPCs normal, no police interest
   - AMBER: police slow near player, random stop-and-search (30-second comedy sketch)
   - RED: pursuit AI, 2-3 police cars, checkpoints on bridges
   - BLACK: helicopter, 4-5 cars, full manhunt (temporary, decays)
7. Compliance Statement: UI popup with absurd checkboxes, -5 per tick

**Time:** 8-12 hours

---

## Phase 6: Traffic and Pedestrians (Day 8-9)

**Goal:** The city breathes. 10-15 traffic cars, 15-20 pedestrians.

**Actions:**
1. Traffic: spawn AI vehicles on road splines. Follow path. Stop at junctions. Stealable.
2. Pedestrians: NavMesh on pavements. Walk between waypoints. State machine: WALK, IDLE, FLEE, REACT.
3. Police: same as traffic but with pursuit behaviour tree. Activated by CivilityIndex events.
4. NPC pooling: spawn within 150m of player, despawn beyond.

**UE5 advantage:** Mass Entity system for crowds. Behaviour Trees built into engine. NavMesh built in. No third-party traffic system needed.

**Time:** 8-12 hours

---

## Phase 7: Phone System (Day 9-11)

**Goal:** The five apps. The comedy engine. The ambient world-building.

**Actions:**
1. Phone UI as UMG widget (UE5's UI system). Pull up with button press. Time does NOT pause.
2. Virtue feed: scrollable list, posts filtered by meter level and mission progress
3. WhatsThat: message threads, triggered by game state. Family chat.
4. Crypt: same as WhatsThat with encryption visual. Download moment (+10 meter).
5. LandanNews: headlines reactive to game state. The disappeared article.
6. Digital Citizenship Report: score display, infraction log, snitch button.
7. Content: pull from game bible. Pressmore posts every 30 seconds. Trunk reposts. Harmer committee-drafted copy. Mum can't find the remote.

**This is mostly UI and writing, not 3D.** The phone system costs the same in any engine. Already well-designed in the bible.

**Time:** 12-16 hours

---

## Phase 8: The Chapel (Day 11-12)

**Goal:** One interior. Father Brennan. The healing mechanic. The bell.

**Actions:**
1. Small stone church interior. Pre-war. Survived the Blitz and the Civility Index.
2. AI-generate the interior in Meshy/Tripo or build from UE5 primitives + Fab assets
3. Father Brennan: MetaHuman. Old. Irish. Tired. 15 lines total.
4. Healing mechanic: enter chapel, meter decays -2 to -5, health restores
5. Optional confession booth: dialogue options based on what the player has actually done
6. The bell: one sound effect. AudioComponent. Triggered at irregular intervals. Not on the map.
7. Gregorian chant ambient audio (low volume, subtle)

**Time:** 4-6 hours

---

## Phase 9: Three Demo Missions (Day 12-16)

### Mission 1: The Pronoun Test (S1)
Processing centre. 6 NPCs. Each tells the player their pronouns. The player must remember them 20 hours later. Form UI with dropdown. Comedy through bureaucratic absurdity.
**Time:** 4-6 hours

### Mission 2: The Ambulance (R3)
Drive to hospital. Passenger bleeding. Civility Index pinging because the route passes through restricted areas. The checkpoint choice: go through (fast, +meter) or around (slow, passenger worsening). Dialogue from the passenger during the drive.
**Time:** 6-8 hours

### Mission 3: The Occupation (R9)
Stealth approach to the asylum hotel. Phone buzzes at the door: Yusuf's message. Chain the door (betray Yusuf, easier mission) or hold the back exit (betray Tommy, harder mission). Neither choice is clean. The O'Connor moment.
**Time:** 8-10 hours

---

## Phase 10: AI Landmarks (Day 16-17)

**Goal:** Replace placeholder cubes with real London landmarks.

**Actions:**
1. Generate each landmark in Midjourney (concept art)
2. Feed into Meshy/Tripo for 3D conversion
3. Import FBX to UE5
4. Place at defined positions from .city file
5. Parliament, The Shard, Tower Bridge, St Paul's, the Eye, Buckingham Gates, the Brutalist Tower, Composter HQ, The Library, Power Depot, Merchant Tower

**Time:** 4-6 hours (2-5 minutes per landmark, plus import and placement)

---

## Phase 11: AI Vehicles (Day 17-18)

**Goal:** UK vehicles that read as London.

Generate in Meshy/Tripo:
- Black cab (TX4 shape)
- Red double-decker bus
- Met Police BMW X5 (battenburg livery)
- Marked police Vauxhall estate
- Ford Transit van
- Vauxhall Astra hatchback
- BMW 3 series
- Beat-up Corsa
- Ambulance (Mercedes Sprinter)
- Delivery moped

**Time:** 4-6 hours

---

## Phase 12: Sound and Polish (Day 18-20)

**Actions:**
1. City ambience per district (Freesound.org)
2. Sirens, rain, traffic hum, wind
3. The bell (one clean recording)
4. Meter ping sound
5. Phone notification sounds
6. Engine sounds per vehicle type
7. Collision impacts
8. Gregorian chant for chapel
9. ElevenLabs voice generation for Father Brennan's 15 lines, Margaret's key lines, the Compliance Statement announcer
10. Final lighting pass per district
11. Film the demo. The Ambulance mission start to finish. 90 seconds.

**Time:** 8-12 hours

---

## Total Estimate

| Phase | Hours |
|-------|-------|
| 0: Driving | 2-4 |
| 1: One block | 3-5 |
| 2: Full city | 6-10 |
| 3: Walk/drive | 4-6 |
| 4: Characters | 8-12 |
| 5: Civility Index | 8-12 |
| 6: Traffic/NPCs | 8-12 |
| 7: Phone system | 12-16 |
| 8: Chapel | 4-6 |
| 9: Three missions | 18-24 |
| 10: Landmarks | 4-6 |
| 11: Vehicles | 4-6 |
| 12: Sound/polish | 8-12 |
| **TOTAL** | **89-131 hours** |

At 6 hours/day: **15-22 days.**
At 10 hours/day (crunch): **9-13 days.**

---

## The Critical Path

Everything else can wait. These are the gates:

**Gate 1 (Day 1):** Does the car feel good? If no, nothing else matters.
**Gate 2 (Day 4):** Does the city feel like London? If no, iterate on buildings and lighting.
**Gate 3 (Day 8):** Does the meter create comedy? If the world doesn't change interestingly across GREEN/AMBER/RED, the core mechanic fails.
**Gate 4 (Day 14):** Does the Ambulance mission make you feel something? If the passenger bleeding while your meter pings doesn't create tension, the game doesn't work.
**Gate 5 (Day 16):** Does the Occupation choice land? If chaining the door on Yusuf's family doesn't make the player pause, the Dostoyevsky layer isn't working.

If all five gates pass, you have a game. Everything after is scale.

---

## Claude Code Session Starters

### Tonight (after UE5 installs):

```
Read the LANDANSTAN.city file in the project root.
Create a new UE5 level called Landanstan_Prototype.
Add a flat landscape 2400m x 1600m.
Add a Chaos Vehicle pawn with arcade handling:
- High engine torque
- Low tire friction for drifting
- Chase camera 8m behind, 4m above
Place the vehicle at position (1200, 800, 100).
Add a directional light simulating overcast London sky.
Add exponential height fog, light grey, density 0.02.
Let me drive.
```

### Day 2 (city generation):

```
Read LANDANSTAN.city.
Write an Editor Utility Blueprint or Python script that:
1. Creates road splines from the road definitions
2. Extrudes road meshes along each spline (14m wide for major, 8m for minor)
3. Creates pavement meshes on both sides (2.5m wide)
4. For each district, reads the building style and height range
5. Along every road within that district, places placeholder box meshes
   (correct width, depth, height per building_widths table)
   with the district's colour as material
6. Creates a water plane for the Thames from the river path points
7. Places bridge meshes at the 5 defined bridge positions
Run it. Show me what we get.
```

---

## What You Don't Build (For Now)

- Browser version (Steam demo first, phone web app handles the "try instantly" hook)
- AI dialogue / Unrestricted Speech Licence (post-launch)
- Faction arcs beyond Restorationist (post-demo)
- Full 7 endings (post-demo)
- Multiplayer (never, probably)
- Mobile (never)

---

## Files Ready to Go

Already written, in your outputs folder:
- LANDANSTAN.city (city generation source file)
- VIRTUE_SIGNAL_GAME_BIBLE.md (single source of truth)
- VIRTUE_SIGNAL_COMPOSTER_ARC.md (second faction arc)
- VIRTUE_SIGNAL_WRITERS_ROOM_PROMPT.md (comedy generation)
- VIRTUE_SIGNAL_PHONE_SYSTEM_PROMPT.md (phone app content)
- DESIGN_COUNCIL.md (design principles for AI agents)

The writing is done. The city is designed. The tools are identified. Now build.
