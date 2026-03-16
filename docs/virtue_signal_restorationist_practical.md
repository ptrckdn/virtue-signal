# VIRTUE SIGNAL: Restorationist Arc -- Practical Build

## PRODUCTION PHILOSOPHY

**Reuse everything.** The game has one city. Missions reuse the same locations with different objectives. The chapel is one building used 20+ times. The hotel is one building used 4 times. The pub is one building used throughout. Tommy's chicken shop alley is one alley. Build locations once, use them many times.

**Story lives in the gaps.** Margaret, Yusuf, Father Brennan don't need dedicated story missions. They exist in the healing visits, the ambient world, and the moments between missions. The player sees Margaret at the chapel because they go there for health. Yusuf appears at the chapel because the game places him there from Act 3 onward. These aren't cutscenes. They're NPCs in a location the player already visits.

**Missions are gameplay. Story is texture.** No mission exists to deliver a story beat. Every mission exists to be fun. The story beats happen around the missions, in the chapel, on the phone, in overheard dialogue, in environmental details.

**Build in layers.** Layer 1: the mission works as pure gameplay (chase, stealth, puzzle, etc). Ship that. Layer 2: add NPC dialogue and ambient detail. Layer 3: add the deeper story connections (Margaret's photo, Yusuf in the chapel). Each layer can be added independently. The game works at Layer 1. It's good at Layer 2. It's great at Layer 3.

---

## THE RESTORATIONIST MISSION LIST

15 missions total. 5 shared (everyone plays these). 10 faction-specific.

### SHARED MISSIONS (Acts 1-2, all factions play these)

These are the missions from the curated list that every player does regardless of faction.

| # | Name | Type | Duration | What You Do |
|---|------|------|----------|-------------|
| S1 | New Arrival | Puzzle/Social | 8-12 min | Intake form, pronoun memory test, choose protest or comply on the final checkbox |
| S2 | The Flat | Chase | 5-8 min | Drive to your flat, approved vs shortcut routes, police checkpoint |
| S3 | The Workshop | Social/Puzzle | 6-10 min | Q&A with hidden cop, spot the code in the slides, type your commitment |
| S4 | First Offence | Chase/Combat | 8-12 min | Pub incident, police arrive, choose to intervene or not, foot chase to Network meeting point |
| S5 | The Signal | Stealth/Chase/Survival | 15-20 min | The big showcase mission. Steal power cell, drive through Westminster, broadcast, survive 60 seconds at BLACK, escape |

**Production note:** These 5 missions are built once and used for all 7 faction paths. Biggest investment, biggest payoff. S5 (The Signal) is the vertical slice that proves the game works.

---

### RESTORATIONIST MISSIONS (Acts 2-5)

After S5, the player commits to the Restorationists. From here, the missions are faction-specific.

---

#### R1: "The Chicken Shop"
**Act 2. First Restorationist mission.**

**Type:** Social + Stealth
**Duration:** 8-10 minutes
**Location:** The alley behind the shut chicken shop, Elephant & Castle. Then a Restorationist community hall.

**What you do:**
Meet Tommy Lemon. He's in disguise (delivery driver uniform). He talks fast. He gives you a burner phone and a list of three addresses. "These are our people. They need to know about Saturday's meeting. The meeting location changes every time because I'm banned from everywhere."

Go to three addresses in Elephant & Castle. Knock on doors. Give the message. Each door is a micro-encounter:

- **Door 1:** An old man. He's been Restorationist for years. He gives you tea. He talks for 90 seconds about the old days. You can't skip this. He's lonely. This is the only visitor he's had this week. (Production: one room interior, one NPC, 3 lines of dialogue.)

- **Door 2:** A young woman. She's nervous. She checks the street before letting you in. She takes the message and closes the door. (Production: doorway only, one NPC, 1 line of dialogue.)

- **Door 3:** Nobody's home. But a neighbour is watching from across the street. They clock you. They might report you. +2 Civility Index. (Production: exterior only, one NPC at a window.)

Then go to the community hall. Tommy's there. Twenty people. Cheap chairs. A whiteboard. Tommy gives a speech about the referendum campaign. The player listens. Margaret is making tea.

**Story beat:** Margaret introduces herself. "You must be new. Sit down, love. Biscuit?" That's it. No backstory. No reveal. She's just an old woman with biscuits. The player will see her again. And again. And again.

**Production cost:** LOW. Three door-knock encounters (one interior, one doorway, one exterior). One community hall interior. Reuse Elephant & Castle street assets.

---

#### R2: "The Leaflet Run"
**Act 2.**

**Type:** Chase (multi-phase)
**Duration:** 12-15 minutes
**Location:** Three districts: Elephant & Castle, Shoreditch, Westminster.

**What you do:**
Distribute referendum leaflets at three drop points. Each point is a different challenge:

- **E&C (friendly territory):** Hand them out at a market. Social: convince 3 out of 5 stallholders to display them. Some say yes, some say no, one threatens to report you. 3 minutes.

- **Shoreditch (hostile territory):** Leave bundles in hidden spots. Stealth: place 5 bundles without being caught on CCTV. Coffee shop bathroom, community board, inside free newspapers. 4 minutes.

- **Westminster (maximum danger):** Motorcycle delivery. Throw bundles from the bike while police pursue. Pure chase. 4 minutes.

**Story beat:** None in the mission itself. But when you return to the community hall afterward, Margaret says: "I saw your leaflets at the market. The stallholder at the veg stand, that's my friend Doreen. She said you were very polite. Good lad." Margaret tracks your work through her social network. She notices everything.

**Production cost:** MEDIUM. Three districts already exist. The motorcycle chase needs a vehicle and police AI. The market and Shoreditch stealth reuse existing environments.

---

#### R3: "The Ambulance"
**Act 3.**

**Type:** Chase
**Duration:** 5-8 minutes
**Location:** Elephant & Castle to hospital.

**What you do:**
The mission from the stress test. Stabbing victim. Can't wait for ambulance. Drive them to hospital. Civility Index pings every red light. The passenger talks. Halfway: police checkpoint on fast route, go through or go around.

**Story beat:** The stabbing victim is someone from the Restorationist community. The player knows them from the hall. Not well. Just a face. But it's a face they recognise. This makes the drive personal, not abstract.

After the mission: the player visits the hospital. The victim is alive. A nurse tells you visiting hours. You can come back or not. If you come back, 30 seconds of bedside conversation. "Cheers, mate. They're saying I'll be out Thursday. You should've seen the other bloke." Light. Normal. A person you helped who's going to be fine.

**Production cost:** LOW. One driving route. One hospital interior (small, reusable). Passenger audio.

---

#### R4: "The Dispatch"
**Act 3.**

**Type:** Puzzle
**Duration:** 8-10 minutes
**Location:** Police station (undercover).

**What you do:**
The knife crime vs speech crime dispatcher mission. Undercover as a police dispatcher for one shift. Ten calls come in: violent crimes and Civility Index violations. Limited units. Allocate resources. At shift end, see your stats vs the system's preferred allocation.

**Story beat:** One of the calls is from your street. A domestic disturbance near Margaret's flat. You can prioritise it (a car gets there in 3 minutes) or follow protocol (it's low priority, response time 40+ minutes). If you prioritise it: Margaret is fine, it was next door, but she was frightened. If you follow protocol: Margaret was frightened for 40 minutes and called you afterward: "Where were the police? I could hear him shouting through the wall."

A small choice. Not flagged. Not tracked visibly. But the player made it.

**Production cost:** LOW. UI-based mission. One screen with incoming calls. No 3D environment needed beyond the station desk. Voice audio for the calls.

---

#### R5: "The Rally"
**Act 3.**

**Type:** Combat + Chase
**Duration:** 12-15 minutes
**Location:** Hackney. Open street.

**What you do:**
Big Restorationist rally. Counter-protest by Composters. Three-way riot: Patriots vs Composters vs police. Escort a whistleblower NPC out of the riot zone. Optional: grab evidence from a police van on a side street.

**Story beat:** Margaret is at the rally. She shouldn't be (she's 73, she's recently been in hospital) but she wouldn't miss it. During the riot, the player sees Margaret in the crowd. She's not in danger but she's confused and frightened. The player can go to her (costs time, the whistleblower is waiting) or proceed with the mission (Margaret finds her own way out). If you go to her: she grabs your arm. "I'm fine, I'm fine. Go. Do what you need to do." She pushes you away. She's fine. But you went to check.

**Production cost:** MEDIUM. Crowd combat is the most expensive mechanic. But this mission is reused across factions (Composter and Patriot arcs also have a rally mission at the same location). Build it once.

---

#### R6: "The Motability Run"
**Act 3.**

**Type:** Social (assessment) + Chase
**Duration:** 10-12 minutes
**Location:** Assessment centre, then open road.

**What you do:**
The stress-tested version. Quick assessment (90 seconds of dialogue, hidden scoring). Get the car. Use it for a Restorationist supply run. Chase with unique vehicle quirks: speed limiter, inward camera, swinging disability badge blocking your view.

**Story beat:** Tommy needs the car for the referendum campaign. "We need a vehicle that doesn't trace back to us. Motability cars are registered to individuals, not organisations. Get one." The player is committing benefit fraud for the cause. It's wrong. It's also funny. And it works. And nobody questions it because questioning Motability is a Civility Index offence.

**Production cost:** LOW-MEDIUM. One small interior (assessment room). One custom vehicle with specific physics (badge swing, speed limiter). Chase reuses road network.

---

#### R7: "The Chapel" (not a mission, a location that evolves)
**Running through Acts 2-5.**

**This is not a discrete mission.** It's a location the player visits for health that changes over time. Production builds it once and swaps NPC placement and dialogue per act.

| Act | Who's There | What Happens |
|-----|------------|--------------|
| Act 2 | Father Brennan, Margaret, regular parishioners | Margaret invites the player. "Come on, love." Normal. Healing works. Readings are comfortable. |
| Act 3 (early) | Same plus Yusuf appears at the back | Margaret stiffens. "What's HE doing here?" Father Brennan introduces Yusuf after Mass. One conversation. 60 seconds. |
| Act 3 (mid) | Yusuf is a regular. Margaret tolerates him. | Yusuf's daughter draws on hymn sheets. Margaret watches her. Says nothing. Once: "She's a good drawer, that one." That's all. |
| Act 3 (late) | Margaret is absent (hospital) | Father Brennan mentions it. "Margaret's not well. She'd appreciate a visit." Optional: visit Margaret in hospital. 60-second bedside scene. |
| Act 4 | Margaret's pew is empty. Yusuf is still there. | If player warned Yusuf: he nods at the player. His daughter waves. If player didn't: Yusuf is gone. |
| Act 5 | Emptier. Father Brennan, fewer parishioners. | Father Brennan says Mass to a smaller congregation. The building is the same. The people are fewer. |

**Production cost:** LOW. One interior built once. NPC placement swaps per act. 8-10 short dialogue lines across the whole game. No cutscenes. Just people in a room.

---

#### R8: "The Hotel"
**Act 3.**

**Type:** Stealth
**Duration:** 10-12 minutes
**Location:** Community Welcome Centre (the hotel on the player's street).

**What you do:**
The inspector mission from the stress test. The real inspector cancelled. You walk in pretending to be them. Tour the building. Photograph conditions. Photograph the contract (£600/week). Photograph the manager's correspondence with the property company.

**Story beat:** The player has walked past this building for the entire game. Now they're inside it. Yusuf's world. Not as a friend. As a spy. They see his corridor. They see his door. They might see his daughter's drawing taped to the wall. The building they've been campaigning to shut down has people inside it and now the player has seen them.

This isn't a story beat the game underlines. The player walks through the hotel photographing evidence and the evidence includes human beings. The game just shows what's there.

**Production cost:** MEDIUM. One building interior. Multiple rooms. NPCs in rooms (families, children, the manager). Reusable for other faction arcs (Composter visits for different reasons, Network visits for evidence).

---

#### R9: "The Occupation"
**Act 4. The critical mission.**

**Type:** Stealth + Physical + Choice
**Duration:** 15-20 minutes
**Location:** The same hotel.

**What you do:**
Tommy's plan. Night operation. Get into the hotel. Chain the doors. Hoist the Restorationist flag on the roof. Do it before dawn.

**Phase 1 (Stealth):** Approach at night. Avoid security cameras and the night guard. Get to the doors. Chain them. 5 minutes.

**Phase 2 (The Choice):** Before you chain the last door, your phone buzzes. You can check it or ignore it.

If you check it: it's a message from Yusuf (if you've met him through the chapel). "Something is wrong. Men outside. My daughter is afraid." The player is standing at the door of the building Yusuf lives in, holding a chain.

If you haven't met Yusuf (never went to chapel, or went but didn't engage): no message. The mission proceeds without the choice. The occupation happens. The story is simpler. Still functional. But smaller.

**If the choice exists:**

Option A: Chain the door. Proceed to the roof. Hoist the flag. The occupation succeeds. +15 faction rep. Tommy celebrates. The families inside are displaced. Yusuf's message goes unanswered.

Option B: Don't chain the door. Call Yusuf. Tell him to get his family out the back exit in the next 3 minutes. This triggers a TIMED STEALTH sequence: the player must hold the back exit clear (distract the other Restorationists, redirect them, stall) while Yusuf gets his family out. Then chain the door and proceed to the roof. The occupation still happens. One family escaped. Tommy doesn't know. But the player's hesitation at the door cost time, and the flag goes up 4 minutes late, which means the police arrive sooner and the escape from the roof is harder.

Option B is the harder mission. The player who does the right thing gets a harder game.

**Phase 3 (Physical):** Climb to the roof. Hoist the flag. The same mechanics as Fly the Flag. Wind, exposure, helicopter flyovers.

**Phase 4 (Escape):** Get off the building. Get clear. Police response at RED or BLACK. Chase.

**Story beat:** This mission is the story. The gameplay IS the choice and the consequences. No cutscene. No speech. A phone buzzing at a door. A chain in your hand. A message from a man whose daughter draws on hymn sheets.

**Production cost:** MEDIUM-HIGH. This is a tentpole mission. The hotel interior is already built (R8). The roof climb reuses Fly the Flag mechanics. The choice branches add complexity. The timed stealth variant (holding the back door) is the most expensive new element. Worth it. This is the mission the Restorationist arc is built around.

---

#### R10: "The Aftermath"
**Act 5. Final Restorationist mission before the faction ending.**

**Type:** Walking + Environmental + Social
**Duration:** 8-10 minutes
**Location:** Elephant & Castle. The chapel. The pub.

**What you do:**
This is a quiet mission after the storm. The referendum has passed. Repatriation is underway. The player walks through their neighbourhood. The game wants them to SEE what happened.

The walk is structured: the player has three destinations (pub, chapel, Margaret's flat) and the route between them is the mission. Along the route:

- Estate agent windows: prices dropping. "REDUCED" stickers everywhere.
- A removal van: a family moving out. Not immigrants. A British family. They can't afford the area anymore because their employer left the country.
- The hotel: empty. A "FOR SALE" sign. The buyer: a company name the player will recognise from the Barrage investigation. An Old Guard shell company.
- The homeless man from Topic 22: still in the same doorway. The hotel is empty and he's still outside. Nothing changed for him.

**At the pub:** Tommy's there. Fewer people. He's drinking alone. "We won," he says. He doesn't sound like he won. The TV shows property prices falling. A news ticker: "Overseas investment fund acquires 340 residential units in South London."

**At the chapel:** Father Brennan. Smaller congregation. He says Mass. He reads the gospel. The player heals one last time.

If Yusuf is there: his daughter shows the player a drawing. It's the chapel. She drew it from memory.

If Yusuf is gone: his pew is empty. Father Brennan glances at it during the reading. That's all.

**At Margaret's flat:** Margaret is dead. She died in hospital. A neighbour tells you. The funeral was Tuesday. You missed it.

Her flat is being cleared. The player can enter. On the mantelpiece: the wedding photo. Margaret and her husband. 1978. The player sees it. The game doesn't comment.

On the kitchen table: a note in Margaret's handwriting. It's a list. Shopping items. Milk, bread, teabags, biscuits. The last thing she wrote was a shopping list. Life at its most ordinary. The player can pick it up or leave it.

**Production cost:** LOW. Walking route through existing streets. Three existing interiors (pub, chapel, flat). Swapped environmental details (estate agent signs, removal van, FOR SALE sign on hotel). Margaret's flat is one small room with a photo and a note.

---

## TOTAL MISSION COUNT AND PRODUCTION COST

| Mission | Type | Duration | Cost | New Assets Needed |
|---------|------|----------|------|-------------------|
| S1: New Arrival | Puzzle/Social | 10 min | LOW | Processing centre interior, 6 NPCs |
| S2: The Flat | Chase | 6 min | LOW | Vehicle, satnav audio |
| S3: The Workshop | Social/Puzzle | 8 min | LOW | Workshop room interior |
| S4: First Offence | Chase/Combat | 10 min | LOW-MED | Pub interior, foot chase route |
| S5: The Signal | Multi-type | 18 min | HIGH | Power depot, library, broadcast equipment |
| R1: Chicken Shop | Social/Stealth | 9 min | LOW | 1 room interior, 3 doorway encounters |
| R2: Leaflet Run | Chase (multi) | 13 min | MED | Motorcycle, market stalls |
| R3: Ambulance | Chase | 6 min | LOW | Hospital room, passenger audio |
| R4: Dispatch | Puzzle | 9 min | LOW | UI screen, call audio |
| R5: Rally | Combat/Chase | 13 min | MED | Crowd combat (shared across factions) |
| R6: Motability Run | Social/Chase | 11 min | LOW-MED | Assessment room, custom vehicle |
| R7: Chapel | Location | Ongoing | LOW | 1 interior, NPC swaps per act |
| R8: Hotel | Stealth | 11 min | MED | Hotel interior (shared across factions) |
| R9: Occupation | Stealth/Physical/Choice | 18 min | MED-HIGH | Roof climb, choice branch, timed stealth |
| R10: Aftermath | Walking/Social | 9 min | LOW | Environmental swaps, Margaret's flat |

**Total play time (Restorationist arc):** Approximately 2.5-3 hours of faction-specific content on top of 2-3 hours of shared content. 5-6 hours total for one playthrough.

**Shared assets across factions:** The hotel interior (R8) is used by Composter, Network, and Centrist arcs. The rally (R5) is used by Patriot and Composter arcs. The chapel (R7) is used by everyone. The hospital is used by NHS missions across factions.

---

## HOW TO BUILD THIS QUICKLY AND BEAUTIFULLY

### The "Beautiful" Part

**Invest art budget in five things:**

1. **The chapel interior.** This is the most-visited location in the game. It needs to be beautiful. Stone, light through stained glass, candle glow, the red sanctuary lamp. The player should feel something when they walk in. Not because of a story beat. Because the room is beautiful. Build it once, make it perfect.

2. **The city at different times of day.** Landanstan at dawn, midday, dusk, night. The same streets looking different. The occupation mission (R9) is at night. The aftermath walk (R10) is at dusk. The leaflet run (R2) is in daylight. Lighting does more for mood than any amount of asset work.

3. **The faces.** Margaret's face. Yusuf's face. Father Brennan's face. Tommy's face. These characters need to look like people, not game characters. Invest in facial modelling and expression for the 5-6 key NPCs. Everyone else can be standard quality.

4. **The hotel interior.** The contrast between its former life (wedding venue) and its current use (families in conference rooms) needs to be visible. A chandelier above a family sleeping on camp beds. A "CONGRATULATIONS" banner partially torn down. Old grandeur, current misery.

5. **Margaret's flat.** One room. But every object tells a story. The wedding photo. The shopping list. A calendar with doctor's appointments. A chair with an indent from forty years of the same person sitting in it. A mug with a tea stain that's been there for weeks because nobody's been home to wash it. This room is 30 seconds of gameplay and it should make the player pause.

### The "Quickly" Part

**Reuse, reuse, reuse.**

- The city is one map. Every mission uses it. Build the map first. Everything else is missions placed in the map.
- Interiors are modular. The community hall, the pub, the hospital room, the assessment centre, Margaret's flat: these are all variations on "small room with stuff in it." Build a kit of walls, floors, furniture. Dress each room differently.
- The hotel interior is one building used 4+ times across faction arcs. Build it once with the wedding venue remnants. Swap NPCs for different missions.
- The chapel is one room for the entire game. Build it once. Swap NPC placement per act.
- Chase sequences use the road network. Build the road network with chase AI. Every chase mission is a different route on the same roads.
- The rally/riot is one crowd combat system used for 3+ faction missions. Build the crowd mechanics once.

**Layer the story content last.** The missions work as pure gameplay first. Margaret's dialogue, Yusuf's appearance at the chapel, the wedding photo, the shopping list: these are late additions. They're text, audio, and NPC placement. Cheap to add. Transformative in effect.

**What you DON'T build:**

- Cutscenes. Zero. Everything happens in-engine, in real time, interruptible.
- Multiple cities. One city. One map. Factions control districts, not separate worlds.
- Complex branching. The Occupation (R9) has one meaningful branch. Everything else is linear with optional micro-choices the game quietly notes.
- Unique mechanics per mission. Every mission uses combinations of 7 existing mechanics (chase, stealth, combat, puzzle, physical, social, survival). No mission invents a new system.

---

## THE PRODUCTION PIPELINE

### Phase 1: The Map
Build Landanstan. Districts, roads, buildings (exterior). CCTV cameras, checkpoints, landmarks. This is the foundation everything sits on.

### Phase 2: The Mechanics
Build the 7 gameplay systems: driving/chase AI, stealth/CCTV detection, combat, puzzle UI, climbing/physical, heist coordination, survival timer. Test them in isolation.

### Phase 3: The Shared Missions (S1-S5)
Build the 5 shared missions. These are the vertical slice. If these are fun, the game works. If they aren't, nothing else matters.

### Phase 4: Key Interiors
Build the reusable interiors: chapel, hotel, pub, community hall, police station, government office, hospital room. These are used across all faction arcs.

### Phase 5: Faction Missions
Build faction-specific missions using the map, the mechanics, and the interiors. The Restorationist arc (R1-R10) is 10 missions, of which 6 are LOW cost (reusing everything built in phases 1-4) and 4 are MEDIUM cost (one new location or mechanic each).

### Phase 6: The Story Layer
Add NPC dialogue, environmental details, the chapel evolution, Margaret's photo, Yusuf's appearances, the phone content, the quiet choices. This is text, audio, and NPC placement. It's the cheapest phase and the one that transforms the game from good to great.

### Phase 7: The Ending
Build the faction epilogue (the aftermath walk), the optional death mission, the mirror, the bell, the number. One mission, shared structure, faction-specific details.

---

## WHAT MAKES THIS BEAUTIFUL

It's not the graphics. It's the accumulation.

The player visits the chapel 15-20 times. They see Margaret there 8 times. They see Yusuf arrive. They see Margaret's pew empty. They see Yusuf's daughter drawing.

None of these moments are dramatic. None of them are cutscenes. None of them demand attention. They're just THERE. Week after week (in game time), mission after mission, the same room, the same people, the same readings.

And then one of them is gone. And the pew is empty. And the game doesn't say a word. The player feels it because they earned it through repetition. They know this room. They know who sits where. The absence is felt because the presence was real.

That's beautiful. Not because of rendering or lighting or music. Because the game respected the player's time and attention and built something genuine with it.

Margaret. The pew. The photo. The shopping list. The bell.

That's the game.
