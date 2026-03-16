# VIRTUE SIGNAL: Game Bible v1.0

## Master Design Document -- Consolidated

*This document is the single source of truth. It supersedes all previous files.*

---

# PART 1: THE GAME

## Concept

VIRTUE SIGNAL is a third-person 3D open-world satirical action game set in Landanstan, a fictional compressed London, 2026. Think GTA meets The Thick of It. Browser-first with a native Steam release planned.

The player lives under the Civility Index, a social credit system that monitors speech, behaviour, and association. The game satirises every political faction, every cultural sacred cow, and every institutional hypocrisy in modern Britain. Nobody gets a pass.

**The subscription model IS the satire:** Free players get multiple-choice scripted dialogue. Paying subscribers ($2.99/month "Unrestricted Speech Licence") can type or say anything to any NPC, with AI generating responses in character. You are literally paying for the right to speak freely in a game about speech being criminalised.

## Design Principles

1. **Fun first, offensive second, satirical third.** If a mechanic isn't fun, no amount of clever writing saves it.
2. **The mute test.** Every mission must be fun with the dialogue muted. If it's not, add gameplay or cut it.
3. **Topic first, game second, satire sprinkled.** Start with a hot-button topic. Design a game that USES the topic. Layer the comedy on top.
4. **Show, don't tell.** The two-tier system is visible in gameplay. Nobody explains it.
5. **Equal opportunity destruction.** Every faction, race, class, gender, sexuality, religion, and political position gets it.
6. **The deep layer is optional.** A player who rushes through should rate the game 8/10 for gameplay. A player who pays attention gets 10/10.
7. **Never explain the joke.** Trust the player.
8. **Clips drive sales.** Every mission should produce a moment worth recording.
9. **The controversy IS the marketing.**
10. **Go further than you think you should.** If everyone in the room is comfortable, it's too safe.

## Tone References

The Thick of It, GTA radio stations, Papers Please, South Park, Black Mirror, Brass Eye, The Day Today, Chris Morris. On the literary side: Graham Greene, Dostoevsky, Flannery O'Connor.

---

# PART 2: THE CIVILITY INDEX (THE METER)

## The Meter Is a Comedy Engine, Not a Punishment System

The meter runs 0-100 with four tiers. It doesn't restrict gameplay. It CHANGES gameplay. Higher meter = more absurd world = better stories.

### GREEN (0-25): Boring

The world is aggressively, oppressively normal. NPCs are polite with dead eyes. "What a wonderful day for civic responsibility!" The best missions and the funniest content are unavailable. The underground won't trust you. GREEN is the tutorial zone of the soul. The player WANTS to leave.

### AMBER (26-50): The Sweet Spot

Where the game lives. Underground contacts appear. The interesting missions unlock. Police stop-and-searches are 30-second comedy sketches, not punishment. The phone lights up with memes. The dating app gets weird. NPC reactions are entertaining. Most players settle here naturally.

### RED (51-75): Action Movie

GTA 3-star wanted level. Active pursuit. Helicopters. Police dispatch: "Suspect is considered ideologically unpredictable. Do NOT let him TALK TO YOU." The big missions (heists, broadcasts, set-pieces) require RED. The player visits for spectacle, then drifts back to AMBER.

### BLACK (76-100): Boss Level

Triggered by specific story missions, not accumulation. Temporary (3-5 minutes, then decays). Full manhunt, maximum absurdity, your mum calling during the chase. Surviving it earns a permanent reward (vehicle, safe house, disguise).

### How the Meter Moves

**Going up (natural, through fun things):** Completing missions (+3 to +15), entering restricted areas (+1 to +5), brave/funny dialogue choices (+1 to +3), CCTV detection (+1 per camera), faction association (+1 to +3).

**Going down (fast, through gameplay):**
- Natural time decay: -1 every 5 minutes of play (the most important change; the meter self-corrects)
- Healing at the chapel: -2 to -5 plus health
- Disguises: stops the meter rising while worn (burns over time)
- Safe houses: small reduction on entry (-2)
- Compliance Statements: 10-second checkbox minigame at police stations (-5). The checkboxes are the joke.

### The Intended Rhythm

AMBER > RED > AMBER > RED > BLACK > RED > AMBER. Like a heartbeat. The meter oscillates. The player rides it.

---

# PART 3: THE PHONE

The phone is the game's ambient world-building system. It replaces GTA's radio. Pull up with a button press. Time does NOT pause. You can get caught scrolling during a police chase.

## App 1: Virtue (Twitter/X clone)

The social media feed. Reactive to meter level and mission progress.

**GREEN:** Bland feed. Memes, outrage, celebrity drama.
**AMBER:** Posts about "someone flagged in your area." Follower count drops. Government ads increase.
**RED:** Player's face appears in "HAVE YOU SEEN THIS PERSON?" posts. Pressmore live-threads about you.
**BLACK:** Account suspended. Only government messaging visible.

**Key character feeds:**
- **Piers Pressmore:** Posts every 30 seconds. Contradicts himself constantly. "FREE SPEECH is under attack. (This post complies with the Digital Communications Act 2025, Section 4.)"
- **Donald Trunk:** Reposts Network content. Every endorsement costs the Network support. Network begs him to stop. "They're very humble. LOVE that about them!"
- **Sir Keith Harmer:** Every post reads like committee-drafted copy. "Let me be very clear." [That's the entire post. 12K reposts.]
- **Nigel Barrage:** Pub selfies geotagged at members' clubs in Mayfair.
- **Prince Edmund & Duchess Clarity:** Comments always disabled.
- **Zane Polansky:** Verified via old HypnoBoost corporate account.

Plus 20+ memes, government promoted posts that increase with meter level, and mission-reactive content (after the Signal broadcast, the entire feed changes for 48 hours).

## App 2: WhatsThat (WhatsApp clone)

Mission briefings, faction contacts, casual NPC conversations. Blue ticks the government can see. Contacts go silent at AMBER+.

**The family group chat:** Mum, Dad, Sister. Completely mundane. Mum can't find the remote. Dad had an earring in 1987. Sister jokes about the Civility Index and Mum panics. At AMBER, Mum texts: "Your dad says your thing has gone orange. What does orange mean?"

## App 3: Crypt (Telegram clone)

Encrypted messaging. Network only.

**The download moment:** The app store has a government warning. Downloading it adds +10 to the meter. If the player hesitates for 10+ seconds, the Network handler texts: "That hesitation you're feeling right now? That's the whole game. That's what the Index does. It makes you police yourself before they have to."

At BLACK level: messages appear with "[DECRYPTED BY DIGITAL SAFETY COMMISSION]" headers. The encryption was compromised from the start.

## App 4: LandanNews (BBC News clone)

Headlines reactive to game state. Early game: bland, reassuring. Mid game: cracks showing. Late game: barely holding together. Endgame: reporting on the player's downfall.

The disappeared article: "Who Funds Civic Futures?" Tap it. "This article has been removed pending review. If you accessed this article before removal, this has been noted on your Digital Citizenship Record."

## App 5: Digital Citizenship Report

Government app. Can't delete it. Shows current score with a smiley/neutral/frowning/skull face. Lists every infraction with timestamps. "Tips to improve your score" that get more threatening as the meter rises. A "Report a concern" snitch button: report any NPC, get -2 on your meter, they get +3 on theirs.

Push notifications appear over gameplay: "Your Civility Index has risen above the community average. This has been noted."

Terms and Conditions include: "By continuing to exist within Landanstan, you agree to ongoing monitoring."

---

# PART 4: FACTIONS

## 1. The Centrists (Government)

Led by **Sir Keith Harmer** (Starmer composite). Procedural authoritarians. Every monstrous act done with complete bureaucratic propriety. NPCs talk exclusively in press release language.

**Key Centrist characters:**
- **Sir Keith Harmer:** "Let me be very clear" before every authoritarian act.
- **Helen Cross:** Deputy Director, Department for Community Safety. The Grand Inquisitor. Not evil. Genuinely believes. Has data to prove the system works. Designed the AMBER threshold to justify the budget.
- **Carol Whitfield:** Community Liaison Officer. Processes 200 intakes a month with genuine warmth. "Welcome to Landanstan!" She's who the Centrist player becomes.
- **Martin Hale:** Former Centrist staffer who left. Living in Bermondsey. Looks tired. "The system isn't evil. That's why I couldn't stay. You can't fight fog."
- **David:** Current Centrist staffer. Former Network. "Helen recruited you, didn't she? She does that. I was Network, two years ago. Now I write Compliance Recommendations. Forty a day."

## 2. The Patriots (Controlled Opposition)

Led by **Nigel Barrage** (Farage composite). Secretly funded by Civic Futures Foundation, a Centrist think tank. He exists to make resistance look stupid. Always on TV. Never achieves anything.

**Key Patriot characters:**
- **Nigel Barrage:** Pint permanently attached. Controlled opposition stooge. Has a performance review with his handlers.
- **Zia Merchant:** Pakistani-heritage co-owner. Bought the position with a million-pound donation. Genuinely believes. "I came here with nothing. I built everything myself. That's not a contradiction. That's the whole point."

## 3. The Composters (Green/Activist Left)

Led by **Zane Polansky** (composite). Right about everything, effective at nothing. Old wellness brand "HypnoBoost" sold boob enlargement hypnosis. Faded billboards haunt him.

## 4. The Old Guard (Conservative Establishment)

**Lady Blackwood** (Clinton composite dynasty). Offshore accounts, charity galas, never gets stopped by police. Her portfolio includes the asylum hotels. She profits from both sides of every policy.

## 5. The Liberators (Far-Left/Antifa)

Trust fund revolutionaries. Live in Brixton in houses their parents bought. Quote theory they haven't read. Revolution scheduled around brunch. Not wrong about the system. Too comfortable to fight it.

## 6. The Restorationists (Right-Wing Populist)

Based in Elephant & Castle council estates. Correct diagnosis of every problem. Cannot organise a response.

**Key Restorationist characters:**
- **Tommy Lemon:** (Robinson composite). Permanently banned from every district. Appears in disguises. Texts from burner phones. "oi its tommy / dont save this number / meet me behind the chicken shop"
- **Margaret:** 73. Former dinner lady. Widow. Makes the tea. Casually racist in the way that doesn't come from malice. Her late husband was Jamaican. Her children are mixed-race. "She's a good drawer, that one" (about Yusuf's daughter).
- **Yusuf:** Syrian. Syriac Catholic. Former civil engineer. Lives in the Community Welcome Centre. Can't work. Knows the Latin Mass responses. His daughter draws on hymn sheets.

## 7. The Network (Underground Resistance)

Operate from hidden locations. The only faction that's genuinely dangerous to the system. Use forbidden iconography. The player's primary allies in shared missions.

---

# PART 5: THE CHAPEL

One healing location for all factions. A small Catholic church in Landanstan. Pre-war stone. Survived the Blitz and the Civility Index.

**Father Brennan:** Old. Irish. Tired. Opens the door in the morning, closes it at night. Says Mass. Hears confessions. Doesn't give missions, doesn't join factions, doesn't fight the system. 15 lines of dialogue across the entire game.

On the Civility Index: "They've built a system that knows everything you've done. We had one of those already. Ours is older and the paperwork's simpler."

**Each faction relates to the chapel differently:**
- **Restorationist:** Trad Cath. Kneels, knows every response. This is home.
- **Composter:** Lapsed. Knows the rituals but feels like a fraud. Keeps coming back.
- **Centrist:** Cafeteria Catholic. Christmas and Easter. Takes the comfortable bits.
- **Patriot:** Cultural Catholic. Defends the Church's right to exist without submitting to it.
- **Old Guard:** Establishment Catholic. Ampleforth-educated. Donated the roof.
- **Liberator:** Angry apostate. Arms crossed. Hates being here. Can't stop coming.
- **Network:** Seeker. Curious about any system that competes with the state.

**The healing mechanic:** Visit the chapel, restore health. Takes 10-30 seconds. The player can heal and leave in 10 seconds or stay longer. The deep content (Father Brennan's occasional lines, other NPCs present, the evolving congregation) rewards staying but never demands it. The chapel evolves across acts: new NPCs appear, others disappear, the congregation changes.

**The confession booth:** Optional. No gameplay reward. The game offers dialogue options based on what the player has actually done. Father Brennan doesn't judge. He reframes. Player: "I reported someone to lower my score." Brennan: "And did it work?" Player: "Yes." Brennan: "The score went down. What about the rest of it?"

---

# PART 6: HOT-BUTTON TOPICS

The game covers 23 satirical topics. Each is a game concept first, a joke second. The grid crosses each topic with 7 gameplay types (Chase, Stealth, Combat, Puzzle, Physical, Heist, Survival) to generate 161 mission seeds.

## The 23 Topics

1. Pronouns / gender identity
2. Grooming gangs / institutional failure
3. COVID / lockdown compliance (origin story for the Civility Index)
4. Knife crime vs speech crime (resource allocation)
5. Ozempic / body positivity (class-based health)
6. Immigration / follow the money (who profits from both sides)
7. NHS / three-tier healthcare
8. AI replacing humans
9. Cancel culture / the pile-on
10. Trans athletes
11. Housing crisis
12. Religion / selective enforcement
13. Dating apps / surveillance
14. Cost of living (persistent economic mechanic)
15. Performative allyship / white liberals
16. Manosphere / male loneliness
17. University / safe spaces
18. Celebrity activism / Hollywood hypocrisy
19. Tax avoidance / offshore money
20. Addiction / drugs
21. Motability / disability benefits gaming
22. Asylum hotels / the trap
23. Brain drain / wealth flight / the Dubai exodus

Each topic has a full grid entry with 7 gameplay ideas, NPC dialogue, environmental detail, radio content, loading screen jokes, and connections to other topics.

---

# PART 7: THE BEST MISSIONS

## Stress-Tested and Approved (diverse across gameplay types)

| # | Name | Type | Topic | Why It Works |
|---|------|------|-------|-------------|
| 1 | The Pronoun Test | Social | Gender | Margaret. Memory game with 20-hour consequences |
| 2 | The Ambulance | Chase | Knife crime | Civility Index pinging while someone bleeds |
| 3 | The Motability Run | Chase | Motability | Police chase in a taxpayer-funded disability car |
| 4 | The Drum Circle | Stealth | HypnoBoost | Timing your heist to bongos, moved upstairs |
| 5 | The Office | Heist | Knife vs speech | Office heist during team lunch, dual-objective |
| 6 | Fly the Flag | Physical | Free speech | All flags equally illegal |
| 7 | The Date | Chase | Dating | Flirting while evading police |
| 8 | The Queue | Puzzle | NHS | Deliberately boring (that's the joke) |
| 9 | The Dispatch | Puzzle | Knife crime | Allocate police to violence vs speech |
| 10 | The Inspector | Stealth | Asylum hotels | Horror of perfect compliance |
| 11 | The Supply Teacher | Stealth | Brain drain | Private school as emigration academy |
| 12 | The Three-Way Riot | Combat | Rally | Organic paint vs SUPPORT OUR TROOPS placard |
| 13 | The Billboards | Physical | Ozempic | Price comparison as guerrilla art |
| 14 | The Playground | Physical/Combat | Asylum hotels | Fistfight over a swing set |
| 15 | The Crisis Manager | Social | Cancel culture | Bust your arse, it blows over anyway |
| 16 | The Budget | Puzzle | Cost of living | Revolutionary who can't afford lunch |
| 17 | The Interview | Social | Media | Three-meter juggle on live TV |
| 18 | The Accountant | Heist | Brain drain | Hiding behind a fridge during a house move |
| 19 | The Broadcast | Survival | Multiple | Statistics read over a fistfight |
| 20 | The Occupation | Stealth/Physical/Choice | Asylum hotels | Yusuf's message at the door |

---

# PART 8: FACTION STORY ARCS

## Structure

Acts 1-2 (5 shared missions) are identical for all players. The faction split happens mid-Act 3. Acts 3-5 are 60% shared, 40% faction-specific. Each faction path has 10-14 unique missions leading to its ending.

**Every faction ending follows the same principle: the faction gets what it wants. The victory is a catastrophe.**

## The 7 Endings (summary)

| Faction | Victory | Catastrophe | New Meter Name |
|---------|---------|-------------|----------------|
| Restorationist | Repatriation flights | Economic collapse, foreign buyout of London | National Loyalty Score |
| Composter | Green utopia enacted | Infrastructure collapse, gated green zones, blackouts | Community Harmony Score |
| Centrist | Stability maintained | Managed decline, player absorbed into the system | Same Civility Index |
| Patriot | Barrage becomes PM | Nothing changes, new puppet installed | Community Confidence Tracker |
| Old Guard | Financial takeover | Class system formalised openly | Same Index, different algorithm |
| Liberator | Revolution succeeds | Each faction territory recreates the Index under a new name | Revolutionary Commitment Assessment |
| Network | Information freed | Messy, imperfect, human freedom | Meter stays but stops working |

The meta-thesis: it doesn't matter which side you pick. The system adapts. The only path that breaks it (Network) doesn't try to replace it.

## Restorationist Arc (fully designed)

**The character arc (Dostoevsky/Greene method):**

The player starts with a fixed idea ("My people are being abandoned"). The game puts PEOPLE in front of that idea. Not arguments. Faces.

- **Act 2:** Join the Restorationists through Tommy. Meet Margaret at the community hall. She makes the tea. She's lovable and casually racist. The player loves her anyway.
- **Act 3:** Meet Yusuf at the chapel. Syrian Catholic. Engineer who built bridges. Can't work. Knows the Latin responses. His daughter draws on hymn sheets. The player's ideology meets a specific face.
- **Act 3b:** Margaret's secret. Her late husband was Jamaican. Wedding photo on the mantelpiece. Her children are mixed-race. She's not a hypocrite. She's a contradiction. Both things are Margaret.
- **Act 4:** The Occupation. Tommy plans to seize the asylum hotel. The player knows Yusuf's family is inside. The phone buzzes at the door. Chain the door (betray Yusuf, succeed) or hold the back exit (betray Tommy, harder mission). Neither choice is clean.
- **Act 5:** The Aftermath. Walking through the changed neighbourhood. The hotel empty and bought by Old Guard shell companies. Margaret dead. Her flat. The photo. The shopping list. Milk, bread, teabags, biscuits.

**Missions:** R1 Chicken Shop (Social), R2 Leaflet Run (Chase x3), R3 Ambulance (Chase), R4 Dispatch (Puzzle), R5 Rally (Combat), R6 Motability Run (Chase), R7 Chapel (evolving location), R8 Hotel inspection (Stealth), R9 Occupation (Stealth/Physical/Choice), R10 Aftermath (Walking).

## Centrist Arc (fully designed)

**The character arc:** Absorption through comfort. The player joins the system for safety (GREEN score, salary, flat). Each mission is a small, logical, defensible compromise. By the end, they can't point to the moment they were absorbed.

**Key beats:**
- Helen Cross recruits them after the Signal broadcast with an offer of instant GREEN
- Processing Civility Index reports becomes satisfying (the UI is designed to feel good)
- The Conference: building a predictive compliance model from data about people like you
- Helen's memo: the AMBER threshold was moved from 30 to 25 for budget reasons
- The Minister's dinner: Harmer explains the system with complete logical consistency, and he's right
- The Resignation: process someone you care about, or walk out

**Critical fix:** Action missions inserted between social/puzzle missions (home visit chase, transport ambush, dawn raid, surveillance tail). The Centrist arc alternates office and field so it passes the mute test.

**Missions:** C1 First Day (Puzzle), C1b Home Visit (Chase), C2 Team Lunch (Social, short), C3 The Report (Puzzle), C3b Transport (Driving/Combat), C4 Workshop Assessment (Social), C5 Promotion Interview (Social), C5b The Raid (Tactical), C6 Martin's Flat (Walking), C7 Conference (Puzzle), C7b Surveillance (Stealth), C8 The Minister (Social), C9 Old File (Puzzle/Stealth), C10 Resignation (Walking/Choice).

---

# PART 9: THE BARRAGE ARC (12-mission thread)

Woven through Acts 2-4 for all faction paths. The player discovers Nigel Barrage is controlled opposition funded by Civic Futures Foundation.

| # | Mission | Key Evidence |
|---|---------|-------------|
| 1 | The Pint | Suspicious phone call overheard |
| 2 | The Rally | Passionate, produces zero action |
| 3 | The Donor | Zia's cash delivered, Barrage denies it |
| 4 | The Leaflet | Tommy's evidence of financial links |
| 5 | The Podcast | Max Contrarian has bank statement, won't air it |
| 6 | The Accounts | Civic Futures Foundation ledger photographed |
| 7 | The Mole | Barrage's phone synced to government server |
| 8 | The Hearing | Barrage and committee chair share a car |
| 9 | The Debate | Barrage can't answer the Civic Futures question |
| 10 | The Broadcast | Evidence goes public, government calls it disinformation |
| 11 | The Fallout | Zia confronts the truth (or doesn't) |
| 12 | Controlled Demolition | Sir Keith reveals the player was useful all along |

By Mission 7, most players suspect. The game doesn't confirm until Mission 12. The discomfort of unconfirmed suspicion is deliberate.

---

# PART 10: THE HIDDEN LAYER

## The Virtue System (invisible)

Throughout the game, 8-10 moments where the right thing and the tribe's thing aren't the same. No prompt, no "MORAL CHOICE" UI, no visible tracking.

**The comedians' consensus:**
- No visible morality system (the moment they know, they optimise)
- No reward for being good
- The world changes slightly (NPCs you helped are fine later; NPCs you didn't aren't)
- Some moments cost the player mechanically with zero compensation

**The novelists' additions:**
- **Dostoevsky:** Virtue has complicated consequences. Good acts cast shadows.
- **Shakespeare:** The moments should be FELT. The world goes quiet for 3 seconds. No prompt. Just stillness.
- **O'Connor:** The deepest moment is violent: ideology meets a human face and cracks.
- **Greene:** The most meaningful virtue comes from compromised people. The player should arrive with dirty hands.

**The endgame mirror:** Near the end, white text on black screen. Every quiet choice listed. Not scored. Not judged. Just shown. Then the faction ending plays as normal.

**Jimmy's number:** After the credits, one number out of ten. No explanation. No formula revealed. Players will argue about it for years.

## The Deepest Layer

The chapel. Father Brennan. The suggestion, never stated, that the Civility Index measures everything about this life and nothing about what comes after.

Details scattered throughout the game, all optional, all unflagged:
- A church bell in the distance at irregular times. Not on the map.
- Graffiti that belongs to no faction: "IS THIS ALL THERE IS?" scratched into stone.
- A copy of The Brothers Karamazov on a shelf in a safehouse.
- Stars visible from rooftops, the only time the camera tilts up.
- The old priest in the hard-to-find church.

**The final sound:** After every ending, after the mirror, after Jimmy's number: one ring of the church bell. Then silence. Then the title screen.

For the atheist player: a nice sound. For the religious player: an answer. For the player in between: a question the game never resolves.

## The Death Ending (optional)

After the faction epilogue, a message from someone the player helped during a quiet choice. They need help again. The player can ignore it (faction ending plays normally) or go back.

Going back means death. The player gets them out. Getting yourself out is not possible. The death is not a cutscene. The player plays until they can't.

**After the death:** The world continues. Pressmore does a thread. The government calls it "neutralisation during a routine compliance operation." Tommy tries to leave flowers and gets chased because he doesn't have a memorial permit. Mum texts the family chat: "Has anyone heard from them? The lamb's getting cold."

The person you saved is buying milk on a Tuesday.

---

# PART 11: PRODUCTION APPROACH

## 2026 AI Pipeline

| Task | Tool |
|------|------|
| City generation | Claude Code + .city description file + City Builder: London prefabs |
| Building landmarks | AI generation (Meshy/Tripo) + hand polish |
| Vehicle models | Meshy/Tripo text-to-3D (12 types in an afternoon) |
| Character models | Tripo text-to-rigged-humanoid + Mixamo animation |
| Code / systems | Claude Code |
| Phone UI | React-based, AI-assisted |
| Writing | AI-assisted drafting, human editing |
| Voice acting | AI voice generation (ElevenLabs) for key characters |
| Sound / music | AI generation + licensed library |

## Realistic 2026 Estimates (1 faction arc)

| Category | Hours |
|----------|-------|
| World / Map | 80-120 |
| Vehicles | 30-50 |
| Characters | 40-70 |
| Combat / Stealth | 60-100 |
| Phone System | 115-165 |
| Civility Index | 54-81 |
| Missions (15 total) | 120-180 |
| Audio | 55-87 |
| Writing | 68-97 |
| Art / Polish | 20-30 |
| Technical Infrastructure | 60-90 |
| **TOTAL** | **702-1,070 hrs** |

## Build Phases

**Phase 1 (Month 1): Vertical Slice**
One district. The Ambulance mission. The chapel. The phone with 20 Virtue posts. The meter at GREEN/AMBER. 3 vehicles. The pronoun memory system. If this is fun, the game works.

**Phase 2 (Months 2-3): Tier 1**
Complete the map. Build shared missions S1-S5. Build first faction arc (Restorationist R1-R10). Fill the phone. Add remaining vehicles, interiors, NPCs.

**Phase 3 (Months 4-5): Polish and Ship**
Deep layer (Margaret's photo, Yusuf's appearances, chapel evolution). Sound design. Ending sequence. Testing and balancing.

**Phase 4 (Post-launch): Additional Arcs**
Each additional faction arc: 4-6 weeks. Same city, same mechanics, new missions and story. Centrist arc second (cheapest, reuses almost everything). Network arc last (true ending).

---

# PART 12: THE 20-HOUR PROTOTYPE

A playable 3D prototype proving the core experience.

| Component | Time |
|-----------|------|
| One driveable city block with placeholder buildings | 4 hrs |
| Phone UI (Virtue feed, WhatsThat, Civility Index) | 5 hrs |
| Civility Index meter (GREEN/AMBER/RED transitions) | 2 hrs |
| Mission 1: Pronoun Test (dialogue + memory system) | 3 hrs |
| Mission 2: The Ambulance (driving + timed passenger) | 3 hrs |
| Mission 3: The Occupation (stealth + choice) | 3 hrs |
| Chapel (interior, Father Brennan, healing) | 1 hr |

Total: ~21 hours. Proves: the phone is funny, the meter creates comedy, the pronoun test works, the Ambulance is tense, and the Occupation choice lands. If those five things work, the game works.

---

# APPENDICES

## A: Environmental Detail Bank

COVID origin: faded "STAY HOME" posters, "TWO METRES" marks on pavements, boarded-up pubs. Motability: dealership with red carpet next to a bus stop with a broken bench. Asylum hotels: "COMMUNITY WELCOME CENTRE" banner, homeless man in the doorway opposite. Brain drain: "TO LET" signs on City glass towers, St Clement's school motto changed to "For Excellence Without Borders." Housing: estate agent windows in different districts showing the price gap. NHS: hospital digital sign showing "A&E WAIT: 14 HOURS" next to "CIVILITY INDEX PROCESSING: 4 MINUTES."

## B: Loading Screen Lines (Jimmy)

- "Remember: in Landanstan, forgetting someone's pronouns is a choice. A wrong choice. Your choice has been recorded."
- "Churchill has been reclassified as a Category 4 Hate Figure. His statue now faces the wall."
- "The NHS wheelchair waiting list is 18 months. The Motability car waiting list is 6 weeks. Both are free. One has heated seats."
- "Community Welcome Centre: where 'welcome' means 'you can't leave' and 'centre' means 'a Holiday Inn with the minibar removed.'"
- "Your Motability vehicle has been used in a manner inconsistent with the Inclusive Transport Initiative."
- "In Landanstan, the most common disability is being too honest about what you see in the car park."
- "The UK's new export: people who can do maths."
- "Private schools are now charging VAT. For that price, the least they could include the plane ticket."
- "In Landanstan, the revolution will not be televised. It also will not be catered."
- "Day 847 of the Civility Index being 'temporary.'"

## C: Compliance Statement Checkboxes

- "I confirm that I have read, understood, and internalised the Community Values Charter (846 pages)."
- "I confirm that I have not, at any point, questioned, implied questioning of, or expressed facial doubt regarding another citizen's Motability eligibility."
- "I confirm that I have not harboured subversive thoughts during the hours of 10pm and 6am."
- "I acknowledge that my feelings may constitute a public order offence."
- "I confirm that my compliance is voluntary and that the consequences of non-compliance are also voluntary."
- "I confirm I have not expressed dissatisfaction with the Community Welcome Centre programme, its costs, its duration, its beneficiaries, or its proximity to my place of residence."

## D: Key Quotes from the Design Process

**On the meter:** "The meter isn't the game. The missions are the game. The humour is the reward. The meter is the volume knob on both."

**On virtue:** "The reward for doing the right thing is that you did the right thing. The moment you gamify virtue, you've turned it into another form of signalling." (Armando)

**On the chapel:** "They spent twenty years building a system to control what people say. Turns out they forgot to build a system to control where people go. Words can't leave Landanstan. Money can. People can. Just not the ones sleeping in doorways." (Frankie)

**On the ending:** "We don't explain the bell."

**On the asylum hotels:** "They think I chose to take their house. I didn't take their house. There is no house. Not for me. Not for them. We are standing in the same empty room arguing about who should be in it." (Yusuf)

**On the Centrists:** "The people who believe all of it are fanatics. The people who believe none of it are revolutionaries. The people who believe parts of it are the ones who keep the system running. You're exactly where I need you." (Harmer)

**On Margaret:** Both things are Margaret.

**On Father Brennan:** He opens the door in the morning. He closes it at night. That's his job.
