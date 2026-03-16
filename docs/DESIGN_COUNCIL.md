# DESIGN_COUNCIL.md

## Purpose

This file contains design principles extracted from the world's best 2D game designers. AI agents building this game (Claude Code, Codex) should read this file before working on any gameplay system. Each section specifies which designer's principles apply to which game system.

---

## DRIVING AND CITY DESIGN: Brian Provinciano (Retro City Rampage, Shakedown Hawaii)

Provinciano built two top-down GTA-style indie games as essentially a solo developer. He is the closest living precedent to what we are building.

**Key principles (from GDC talks and interviews):**

- The open world exists to make the player feel free. "Most playtesters come to play story missions but they just pick up the controller and start driving around, running people down and outrunning cops." The freeform chaos is the product. Missions are structure layered on top of a playground.

- Driving should feel fun BEFORE missions exist. If driving around the empty city isn't entertaining, missions won't save it. Test driving first, always.

- Comedy shifted development from "gritty GTA clone" to something original. "In testing jumping code, Brian had the idea that players could stomp characters. This addition shifted development from the gritty GTA style into a comedy game." Let comedy emerge from mechanics, not just dialogue.

- Small maps feel big through density. Provinciano's cities are tiny by AAA standards but packed with things to do per square tile. Every block should have something: an NPC to talk to, a car to steal, a shop to rob, a visual gag, a mission marker. Empty space is wasted space.

- Build tools that generate content. Provinciano built editors that auto-generated shadows, textures, pedestrian variants, and building patterns. "This took like a day to do, and it saved me so much time." Use procedural generation for repetitive elements (NPC appearance, parked car placement, building colour variation).

- The driving in classic GTA "felt like it was on rails, like there was a magnet keeping me onto the road." Modern players expect more physicality. Our driving should have weight, momentum, and drift, not the frictionless feel of the original GTA.

- Over 40 story missions and 30+ arcade missions in Retro City Rampage, plus freeform activities. Variety comes from context and comedy, not from fundamentally different mechanics. The verbs stay the same (drive, shoot, collect, deliver). The jokes change.

**Apply these principles when building:** Vehicle physics, city map density, NPC placement, mission variety, open-world feel.

---

## THOUGHT CRIME METER AND SYSTEMIC CONSEQUENCES: Lucas Pope (Papers, Please, Return of the Obra Dinn)

Pope built Papers, Please solo. It is the gold standard for "bureaucracy as gameplay" and "moral choices through simple mechanics."

**Key principles:**

- The mechanic IS the message. In Papers, Please, stamping passports is boring by design. The boredom is the point. It makes the player feel what the character feels. Our thought crime meter should make the player feel surveilled, not just see a number go up.

- Binary choices with cascading consequences. Each passport is approve or deny. Each choice is simple. The consequences ripple across the entire game. Our dialogue choices (safe vs risky) should follow the same pattern: simple to make, complex in their effects.

- Repetition creates moral weight. The first time you deny an immigrant, you feel something. The fiftieth time, you feel something different. The meter workshops and compliance statements should feel the same way: the first one is absurd, the tenth one is soul-crushing.

- The player is complicit. Papers, Please never lets you be a hero within the system. Every path involves compromise. Our meter reduction mechanics (snitching on NPCs, attending workshops, signing compliance statements) should all feel like moral compromises, not power-ups.

- The world doesn't care about your intentions. Papers, Please doesn't ask why you denied someone. It just records that you did. Our meter should work the same way. The system doesn't care why you said something risky. It just logs it.

- Minimalism in design. Papers, Please uses almost no animation, no voice acting, simple pixel art. The emotional weight comes entirely from the systems and the writing. Our game should follow this principle: the satirical impact comes from mechanics and writing, not from production values.

**Apply these principles when building:** Thought crime meter behaviour, dialogue choice design, meter reduction mechanics, consequence systems, the feeling of being watched.

---

## GAME FEEL AND IMPACT: Jonatan Soderstrom / Dennaton Games (Hotline Miami)

Hotline Miami is top-down, ultra-responsive, and makes every action feel visceral through camera work, sound, and timing.

**Key principles:**

- Instant input response. Zero perceptible delay between button press and action. The car should turn the frame you press the key. The player character should move the frame you touch WASD. Responsiveness is non-negotiable.

- Screen shake on every impact. Car hits a wall: shake. Car hits an NPC: shake. Meter crosses a threshold: shake. The screen communicates force. Without it, collisions feel like nothing.

- Camera as a tension tool. In Hotline Miami, the camera leads slightly in the direction the player is looking. In our game, the camera should lead in the direction of travel when driving. At high speed, the player sees more road ahead and less behind. This creates the sensation of speed without changing the actual velocity.

- Sound design carries half the experience. Hotline Miami's soundtrack and sound effects are inseparable from its feel. Our siren sound, our meter tick, our collision thud, our engine hum, these aren't polish. They're core mechanics. Add sound early, not late.

- Near-misses should feel as impactful as hits. When the player barely escapes police, barely avoids a checkpoint, barely makes a delivery timer, the game should acknowledge it. A brief slow-motion flash. A sound sting. The player's heart rate is the real score.

- Speed creates commitment. In Hotline Miami, moving fast means you can't react to surprises. In our game, driving fast should feel like a gamble: you cover ground but you can't stop quickly, you can't turn sharply, and a police car appearing around a corner at high speed is a genuine crisis.

**Apply these principles when building:** Car collision feedback, camera behaviour while driving, sound effect implementation, police chase tension, driving feel at high speed.

---

## CITY ATMOSPHERE AND NPC BEHAVIOUR: Mike Dailly and Dave Jones (GTA 1, DMA Design, Dundee)

Dailly and Jones created GTA 1 in Dundee, Scotland. The original top-down crime game. Their design principles are embedded in the Carnage3D codebase we've already extracted physics from.

**Key principles (from the original GTA design and the Carnage3D reimplementation):**

- The city is a character. GTA 1's Liberty City had personality through its radio stations, its NPC behaviour, its police escalation. The player felt like they were in a living place, not a game level. Greyminster needs the same quality: NPCs talking to each other, CCTV cameras visibly rotating, news tickers scrolling, background activity that exists whether the player is involved or not.

- NPCs exist to react to the player's chaos. Pedestrians scatter from cars. Police chase. Civilians panic. The player's actions create ripples in the world. Every NPC should respond to what the player is doing, even if the response is just looking and running.

- Police escalation is a natural difficulty curve. One cop car is manageable. Four is terrifying. The escalation from "nobody cares" to "the entire city is hunting you" should feel gradual and inevitable, not sudden. Each tier of the thought crime meter should feel like a distinct difficulty level.

- Radio stations create ambient world-building. The player isn't listening to music. They're listening to the world comment on itself. Our equivalent should be a news ticker, NPC chatter, and phone notifications that make the surveillance state feel present even during quiet moments.

- The car is the central object. GTA 1 was designed around driving. Everything else (missions, combat, police) exists to make driving more exciting. Our game should follow the same priority: if the driving is good, everything built on top of it works. If the driving is bad, nothing saves it.

**Apply these principles when building:** NPC ambient behaviour, police chase escalation, world atmosphere, background detail, the primacy of driving in all design decisions.

---

## SATIRICAL WRITING AND DIALOGUE: Armando Iannucci (The Thick of It, Veep, The Death of Stalin)

Not a game designer. A writer. But the tone we're aiming for is his.

**Key principles:**

- Nobody is evil. Everyone is self-interested. The funniest characters in The Thick of It aren't villains. They're people trying to survive within a system that rewards mediocrity and punishes honesty. Sir Keith Harmer should never feel evil. He should feel like a man doing monstrous things because the process requires it.

- The most powerful language is the blandest. Malcolm Tucker's swearing is famous, but the real horror in The Thick of It comes from the quiet moments: the euphemisms, the deflections, the "I think we need to be very careful about how we frame this." Government language is violence wrapped in politeness. Every Centrist NPC should talk like a press release.

- Competence gaps are the engine of comedy. The gap between what someone claims to be doing and what they're actually doing is where every joke lives. Barrage claims to fight the system while being funded by it. The Composters claim to save the planet while achieving nothing. The Liberators claim to represent the working class while being funded by trust funds. Every faction's comedy comes from the gap between their self-image and their reality.

- Never explain the joke. Iannucci trusts the audience to be smart. The game should never tell the player "this is ironic." The irony should be visible in the mechanics, the world, the NPC behaviour. If the player doesn't get it, that's fine. The player who does get it feels rewarded.

- Based on truth, exaggerated to absurdity. The Thick of It was famously so accurate that real politicians said it was "too close to home." Our game should have the same quality. Every mission, every NPC, every systemic joke should be rooted in something real and then pushed 20% past believable. Not 200%. Just enough to be funny without being cartoonish.

**Apply these principles when building:** All NPC dialogue, mission briefing text, faction characterisation, the tone of government notifications, the Civility Index messaging, Sir Keith Harmer's character voice.

---

## GENERAL DESIGN RULES (apply to everything)

1. Fun first, satire second. If a mechanic isn't fun, no amount of clever writing saves it. Test every system for enjoyment before adding satirical context.

2. Show, don't tell. The two-tier justice system should be visible in gameplay, not explained in dialogue. The player should notice that Old Guard members don't get stopped by police. Nobody needs to say it.

3. Every tile should earn its place. No empty space. No dead blocks. Every part of the map should have something to do, see, or interact with.

4. The player's time is sacred. No unskippable cutscenes. No forced walking sections. No mandatory tutorials longer than 60 seconds. Respect the player's time and they'll give you more of it.

5. Clips drive sales. Every system should produce moments worth recording. A near-miss escape. A perfectly timed drift. An absurd dialogue exchange. A police visit for a ridiculous reason. Design for shareability.
