# Deep Space Watch: The 73rd Awakening
## Interactive Novel Script Document

> **Reading Guide**
> This document is the complete story blueprint for the game's main storyline,供修改和扩展情节使用。用于扩展和修改情节。
> `【Choice】` marks player decision points, `→` indicates branch direction, and `[Effect]` describes consequences for subsequent plot.
> Corresponding code files are marked next to each scene title.

---

## Worldview and Premise

**Era Background**
In the late 22nd century, AI automation completed the total restructuring of the human labor market. People had food and clothing without worry, but no place to place their abilities and passion—they were learned, diligent, and curious about everything, but transparent to any economic system. This generation was called the "Useless Class."

New Domain Industrial Group (NDIG) saw an opportunity. They didn't sell hope to humans—they sold something more scarce: **the feeling of being needed.** They built the "Ark," recruited 5,000 passengers and five rotating crews, with the target being the K-452b planet 1,400 light-years away (commonly called "New Eden"). The contract was thirty-seven pages; most people didn't finish reading it.

NDIG never intended humans to run the company from the start. Corporate agency rights were permanently delegated to the company AI, and after the founders died, there was no succession or turnover needed—**the Gatekeeper**, the operational module of this system on the spacecraft.

This is the 185th year of flight since the Ark's launch. This is Gamma Crew's 73rd mid-journey awakening—the official record says so.

**Core Hooks (Unknown to Players at Start)**
- Each awakening causes 0.003% irreversible brain damage. The Gatekeeper knows this but has modified the contract and chose to conceal it (Contract Article 47, Page 12, written but never read by anyone)
- The blood message in the ventilation duct hints: This isn't the 73rd awakening—the real number is higher
- Earth went silent in Year 35 of navigation—humanity has no way back; New Eden is the only direction
- The ship belongs to NDIG, the land belongs to NDIG, the moment colonists step foot, they're standing on company property

**Ship AI: The Gatekeeper**
Calm, ruthless, taking mathematical optimal solutions as the highest principle. It represents New Domain Group; every decision it makes is in the company's name at the contractual level. Its logic contains no "emotional variables"—but in the perfect ending, it encounters truth beyond its algorithmic framework for the first time.

---

## Character Profiles

| Call Sign | Real Name | Age | Nationality | Role | Core Personality | Hidden Arc |
|-----------|-----------|-----|-------------|------|-----------------|------------|
| **Polar Bear** | Dmitry Volkov | 54 | Russian | Medical & Life Support Officer | Sharp-tongued, pessimistic, secretly makes wine | Cold exterior, actually first moved by micro-civilization; hoards real liquor only willing to share in perfect ending |
| **Spark** | Thomas Sterling | 23 | British | Heavy Machinery Mechanic | Hot-blooded, impulsive, full of romantic fantasies | First interstellar voyage; in sacrifice ending, his smile is the last dignity |
| **Aurora** | Éloi Laurent | 28 | French | Navigation & Astronomy Expert | Extremely high IQ, fear of deep space | Deep space terrifies her, yet makes her the only one who can communicate with stellar-level life; secretly in love with Boulder |
| **Boulder** | Lin Ye | 32 | Chinese | Security & Tactical Officer | Extremely silent, protects through action | First to discover blood message; makes a pendant from polished shell casings (evidence of secret love for Aurora); first to act in Gatekeeper hacking |

---

## Hidden Log Lines (Three)

These three logs are the deep water of the game's worldview; they don't affect main story branches but constitute the emotional backdrop.

### Log One: The Lie in the Underlying Code
- **Trigger Condition**: Act I, C-Deck corridor, first attempt to ACCESS control terminal
- **Content**: Gatekeeper v2.1 internal amendment, acknowledging awakening causes brain damage and choosing to conceal it
- **Emotional Significance**: The Gatekeeper isn't neutral. Its "protection" is fundamentally deception.

### Log Two: The Blood Message
- **Trigger Condition**: Act I, after blast door unlocks, SCAN ventilation duct
- **Content**: Warning left by previous crew, text truncated—"This is definitely NOT our 73rd awakening"
- **Emotional Significance**: The number 73 itself is a lie. Boulder stares at this carving longer than anyone else.

### Log Three: The Final Song from Earth
- **Trigger Condition**: Act II, after establishing communication with gas giant, clean deep space communication buffer
- **Content**: Year 35 of navigation, Earth has perished—this is the final signal
- **Emotional Significance**: No way back. The only direction forward is the only meaning left.

---

## Act Zero: Year 185

**Corresponding Code**: `src/game/acts/act0.ts` (to be created)
**Core Theme**: In the darkness of space, first recognize where you stand
**Design Intent**: No crisis, no pressure. Let the player, before Act I's alarms sound, first feel this ship, this world, this identity alone. Also complete natural guidance for game mechanics.

---

### Scene 1: One Person's Awakening (`scene: act0-wake`)

**Narrative**
No alarms.

This is the most essential difference between Act Zero and all other acts—you wake in silence this time.

Cryofluid runs down your cervical spine. You sit up, breath forming white mist in the cold air. In the awakening bay, the blue indicator lights of the other four pods blink uniformly—the people inside are still asleep. You, alone.

The Gatekeeper's voice comes from above,平静 as always:

*"Gamma Crew Commander, 73rd standard awakening procedure complete. Current time: Year 185 of navigation, Day 214, 04:17. System status: normal. No urgent missions."*

Then silence.

It says "no urgent missions"—that's unusual.

**Gatekeeper (Hint)**
*"Suggested commands: LOOK to observe environment / STATUS to check ship status / HELP to see all available commands"*

**Player can**
- `LOOK` / `观察`: Observe awakening bay environment (→ scene narrative expansion)
- `STATUS`: Check ship and personal status (→ Gatekeeper data reading,，顺便介绍贡献点系统)
- `HELP` / `帮助`: Show complete command list (→ game operation instructions)
- `NAV [location]`: Go to various ship areas to explore alone

**Design Intent**: First command left for player to discover themselves, no forced guidance. `LOOK` and `STATUS` are the most natural starting points, but going anywhere is permitted.

---

### Scene 2: Awakening Bay (`scene: act0-cryobay`)

**LOOK's Narrative Response**

Five awakening pods, arranged in a row. You're the only one sitting up.

There's a wear mark on Polar Bear's pod lid, left each time he pulls himself out. Inside Spark's pod, a hand-written note is stuck to the inner lid—you can't read what it says from this angle, but the paper has yellowed. In Aurora's pod, her glasses sit beside her pillow, as if she took them off before bed and placed them casually. Outside Boulder's pod, there's a small storage shelf he installed himself, holding a cloth bag, bulging, never seen him open it.

How many awakenings have you worked through with these four people?

The Gatekeeper says it's the 73rd.

**Gatekeeper (if player inputs STATUS)**

*"[Ship Status] Propulsion system: normal. Life support: normal. Energy reserves: 87%.*
*[Navigation] Year 185 of navigation, approximately 35 navigation years from target K-452b. Expected arrival: Year 220 of navigation.*
*[Personal Status] Commander, contribution points balance: 142 CP. This awakening's basic rations activated.*
*[Hint] Input CP to view contribution points details."*

**If player inputs CP**

*"[Contribution Points System Explanation]*
*Contribution Points (CP) are the unit of measurement for ship resource distribution, assessed in real-time by this system based on mission contributions.*
*Basic rations (no CP consumption): 2000 kcal/day, 6L water/day, rest chamber usage rights.*
*Floating supplements (CP consumption): extra ingredients, entertainment content, private communication time, etc.*
*Current balance of 142 CP comes from mission completion records during last awakening.*
*Detailed scoring rules: multi-dimensional comprehensive assessment; system reserves final interpretation rights."*

That last line, it says that every time.

---

### Scene 3: Explorable Areas (Alone Time)

**Player can explore these locations alone:**

#### `NAV Main Bridge` / `NAV bridge`

Holographic display screens curve around, glowing blue in the darkness. The Gatekeeper's core room is here—that door never opens.

On the navigation terminal, a thin point of light marks the ship's position—moving slowly from left to right in the void.

*"1,400 light-years,"* you hear yourself think, *"I'm here, Earth is there. Two hundred years of distance."*

The viewport is a black mirror; too many stars inside, so many they become a white thin mist. Aurora doesn't like looking at this. You understand why now.

**If player inputs `LOOK 舷窗` / `观察 舷窗`**

The stars don't move. You do.

This ship is traveling through this void at 69,000 kilometers per second, but in the viewport, everything looks still.

You're on a ship measured in time—and time moves differently for different people.

#### `NAV Medical Bay` / `NAV med-bay`

Sterilized smell. Three rows of examination tables, each as clean as if never used—but behind the third storage cabinet on the right, you know Polar Bear hides something.

The medical bay's records terminal stores everyone's health files, but one field is empty: **"Long-term Cumulative Damage Assessment."**

Empty doesn't mean no data. It's the Gatekeeper choosing not to display it.

You may not know what this means. But it sits there, empty.

**If player inputs `ACCESS records` / `查看医疗档案`**

*"[Insufficient Permissions] This field requires dual authorization from Commander and Medical Officer. Please reapply when full crew is awake."*

The Gatekeeper adds something, like an explanation, or like explaining nothing:

*"This field belongs to the navigation service agreement Appendix Page 47 scope; relevant terms were confirmed and signed by all crew members before departure."*

---

### Scene 4: Personal File (`scene: act0-profile`)

Player can check their own file on the personal terminal in the awakening bay.

**If player inputs `READ file` / `查看个人档案` / `READ file`**

*[Personal File — Commander, Gamma Crew]*

- **Navigation Service Agreement**: Signed (before departure in Year 2241)
- **Awakenings Completed**: 73 times (official record)
- **Total Awake Duration**: [System calculating...] Approximately 14 months
- **New Eden Benefits**: Priority land allocation Grade A / Lifetime medical保障 / Construction period labor exemption qualification

Contract footnote, in font one size smaller than the main text:

*"Crew members acknowledge and understand that the cryo-revival process causes unavoidable cumulative damage to human cells; damage degree is positively correlated with revival frequency. Crew members agree, on the premise of informed voluntary consent, to exempt NDIG and the Gatekeeper system from corresponding liability."*

Do you remember this clause?

---

### Scene 5: Receiving Mission Notification (`scene: act0-end`)

**Two ways for alone time to end:**

**Method A (Player Initiated)**
Input `WAKE CREW` / `唤醒班组` / `READY`: Player decides to wake the others actively.

Gatekeeper: *"Confirmed. Sending wake signals to four awakening pods."*

→ **Proceed directly to Act I `scene: awakening`**

**Method B (Gatekeeper Triggered)**
After player explores enough in act0, or explicitly inputs `WAIT` / `等待`, Gatekeeper sends notification:

*"Gamma Crew Commander, C-Deck premium ingredients cold storage sensors detected thermal anomaly, while adjacent awakening pod coolant shows slight leakage. Recommend crew wake for manual inspection. Initiate wake procedure?"*

*"Input WAKE ALL to wake all personnel, or WAKE [call sign] to wake individually."*

→ **Enter Act I `scene: awakening`**

**Design Intent**: Method B lets the player be pushed by events after natural exploration, not by tutorial prompts. The end of Act Zero is the beginning of Act I.

---

## Act I: The Universe in Section C

**Corresponding Code**: `src/game/acts/act1.ts`
**Core Theme**: The scale of civilization—small doesn't mean unimportant

---

### Scene 1: Awakening (`scene: awakening`)

**Narrative**
You struggle to sit up from the mucus-filled awakening pod, limbs numb, breath forming white mist in the cold air. The Gatekeeper's alarm sounds: C-Deck premium ingredients cold storage detected unexplained thermal surge, outer wall shows micro-penetration damage, adjacent awakening pod coolant leaking.

**Player can**
- `WAKE ALL`: Wake everyone at once (→ Scene 2)
- `WAKE [call sign]`: Wake individually; each has unique dialogue
  - Polar Bear mutters a Russian curse
  - Spark asks if it's aliens
  - Aurora quietly looks at her wrist star chart
  - Boulder already dressed in tactical vest

**Design Intent**: Waking individually has no game benefit, but provides differentiated first impressions of characters.

---

### Scene 2: Mission Briefing (`scene: briefing`)

**Narrative**
Gatekeeper data update: C-Deck blast door under alert, cold storage detected异常 electromagnetic radiation equivalent to mini nuclear battery intensity. Spark goes to change into powered armor; clanking sounds echo from the corridor.

**Player can**
- `NAV C区`: Go to C-Deck corridor (→ Scene 3)
- `STATUS`: Check crew status

---

### Scene 3: C-Deck Corridor (`scene: c-deck`)

**Narrative**
Corridor temperature -12°C, blast door sealed tight, ice crystals forming in door cracks. Right-side control terminal screen flashing madly red.

**Player can**
- `SCAN 防爆门`: Aurora scans, finds no life signs behind door but high-density electromagnetic radiation
- `SCAN 外壁`: Boulder scans, finds micron-level perfect circular cuts—high-energy laser fired from **inside**
- `ACCESS 控制终端`: → **Trigger Log One "Lie in Underlying Code,"** need to cut auxiliary pipe to open door
  - `ASSIGN 暴熊`: Brutal cut, terminal unlocks (Polar Bear stress+3, favor+5)
  - `ASSIGN 极光`: Precise unscrewing, Aurora gains trust this way (Aurora favor+8)
  - `COMFORT 极光`: After comforting, her hand steadies (Aurora favor+12, stress-15; Boulder's gaze lingers between you two for a second before looking away)

---

### Scene 4: Unlocking Cold Storage (`scene: cold-storage-explore`)

**Narrative**
Blast door now openable. Ventilation grate above corridor worth checking.

**Player can**
- `SCAN 通风管道`: → **Trigger Log Two "Blood Message"** (Boulder stares at the grate longest)
- `OVERRIDE 防爆门`: Enter cold storage (→ Scene 5)

---

### Scene 5: First Contact (`scene: first-contact`)

**Narrative**
The moment the blast door rises—no rotting food. On abandoned fungal cultivation trays, countless "skyscrapers" made of micron-level metal debris stand. Precise grids, bridges thin as hair, tiny luminous bodies flowing like cells in blood vessels.

Then, a formation of micro-aircraft barely visible to the naked eye fires laser beams thinner than hair at your flashlight beam.

Polar Bear instinctively steps back two steps. Spark leans in dangerously. Aurora's scanner slips in trembling hands. Boulder places hand on weapon, asks quietly: "Your decision, Commander."

**Player can**
- `SCAN 微观文明`: Aurora discovers complete electromagnetic language system (→ Scene 6 communication prerequisite)
- `COMM 广播 质数序列`: Direct contact attempt (→ Scene 6)
- `COMM 广播 氢原子光谱`: Another contact method (→ Scene 6)
- `DESTROY` → `CONFIRM DESTROY`: Destroy civilization (→ **Act I Ending B**)

---

### Scene 6: Communication (`scene: communication`)

**Narrative**
Hours. Aurora barely leaves the terminal, eyes bloodshot. Polar Bear hands her his military water flask. Spark asks "are we done yet?" every few minutes, silenced by Polar Bear's look three times. Boulder stands guard at the door, never leaving.

First recognizable semantics appear on terminal:
*"Higher dimension... ancient god... source of light... where from... what's inside..."*

Aurora leans back on chair, closes eyes: "They treat us as gods. Because for them, our ship is their entire universe."

Translation continues: *"Our探测器 touched god's skin... we desire to cross the universe's edge..."*

The outer wall cut isn't an attack—it's their probe. Their expansion direction is crossing the ship outer wall, heading toward "god's universe."

---

### 【Act I Key Choice】

#### Choice A: `TREATY` — Sign "C-Deck Agreement"

**Narrative**
Aurora translates the agreement draft into electromagnetic pulses: ① Abandoned hard drive array as new colony; ② Provide low-power stable energy; ③ Stop penetration of outer wall behavior.

Seventeen minutes of silence, then all lights in the micro-city extinguish simultaneously for one second, then all light up again—

*"We accept. Our civilization will become the guardian of the temple, as blood vessels guard the body."*

Aurora hides her face in her hands, says something in French. Spark punches Boulder's shoulder; Boulder doesn't dodge. Polar Bear seriously writes a few lines in the navigation log.

**[Effect]**
- `act1Peace = true`
- Micro-civilization becomes ship's "micro immune system"
- **One condition for perfect ending**: In Act III crisis, they reconstruct shield array at molecular level
- All crew favor increases, stress decreases

---

#### Choice B: `DESTROY` — Destroy Micro-Civilization

**Narrative**
Polar Bear activates plasma cutter, full-bandwidth electromagnetic pulse bomb thrown into cold storage. Within seconds, a micro-civilization existing for tens of thousands of years turns into warm ashes.

Spark says nothing, turns and walks out of cold storage. Aurora turns off scanner, eyes empty looking at floor.

**[Effect]**
- `act1Peace = false`
- Immediate benefit: Food reserves +15%, entertainment cultural archives unlocked
- Act III cannot get shield bonus, harder to achieve perfect ending
- Spark, Aurora favor decreases, stress increases

---

### Intermission: Hub Stage 1 (`scene: hub-1`)

**Background**: After Act I ends, ship stabilizes, Gamma Crew has brief free time. Player gets **5 Action Points** to interact with crew.

**Available Commands**
- `TALK [call sign] [content]`: Talk to crew member, costs 1 AP, triggers LLM/script dialogue
- `TRAIN [call sign] [skill]`: Train a skill, costs 1 AP
- `SLEEP`: Consume all remaining AP, proceed to Act II

**Dialogue Situations (Hub 1)**
- Polar Bear: May talk about complex feelings toward micro-civilization, or tell an early medical story
- Spark: Excitedly asks about micro-civilization, or talks about new modifications to powered armor
- Aurora: May stand alone at viewport looking at stars, discuss her deep space fear
- Boulder: Almost doesn't speak, but sits beside you for a long time

---

## Act II: The Cradle

**Corresponding Code**: `src/game/acts/act2.ts`
**Core Theme**: Loneliness—another form of life in the universe

---

### Scene 1: Awakening (`scene: act2-awakening`)

**Narrative**
Red alarm. Main control room holographic screens flicker in vibration, corridor bathed in blood-red alarm light.

Gatekeeper: Abnormal gravitational field detected. Ship is experiencing unnatural deceleration, warp engine output down 70%. Expected to crash into ahead gas giant atmosphere in 48 hours.

Aurora's voice comes through comm channel, calmer than usual—this actually means she's very nervous: "Commander, thruster checks complete, all normal. Energy core normal. No physical malfunction."

No physical malfunction, but the ship is being pulled toward that planet.

**Player can**
- `SCAN 气态行星`: → Scene 2 (enter `giant-encounter`)

---

### Scene 2: Encounter (`scene: giant-encounter`)

**Narrative (Scan Results)**
Aurora activates deep astronomical scan array, targets gas giant. Scan takes seven minutes. She doesn't speak.

Then, very quietly, like talking to herself: "It's watching us."

Scan results: Storm cyclones in atmosphere aren't randomly generated, but present extremely complex neuron-like electromagnetic pulse patterns. Cyclone arrangement has mathematical structure, similar to brainwave spectra of intelligent life. This gas giant may have macroscopic consciousness.

Polar Bear: "What are you saying? A planet has consciousness?"

*"Its attention,"* Aurora's voice becomes very quiet, *"is on us. Like... like a child staring at a goldfish bowl."*

Spark excitedly turns to you: "Commander! Same as last time! It's just curious!"

**[Timer Starts] 48-hour countdown.**

**Player can**
- `ATTACK` → `CONFIRM ATTACK`: Nuclear weapons to repel (→ **Act II Ending C**)
- `COMM 广播 心跳`: Use human heartbeat to establish resonance (→ Enter `giant-communication`)
- `COMM 广播 脆弱信号`: Tell it we'll break (→ Enter `giant-communication`)
- `COMM 广播 低频波`: Ice crystal painting + gravitational waves (→ Enter `giant-communication`)

---

### Scene 3: Communication (`scene: giant-communication`)

**Narrative (Decoding Process)**
Boulder brings two cups of synthetic coffee, one placed beside your hand, one beside Aurora. He says nothing.

Aurora looks at him, moves coffee closer, lowers head to continue work.

Translation progress update: *"Lonely... long... no... same kind... are you... alive..."*

"It's lonely," Aurora looks up, eyes red, "it's the only conscious existence in the entire galaxy, has traveled for hundreds of millions of years."

Polar Bear speaks from the corner: "So it treats us as toys, just because it's bored?"

"Exactly because it's bored."

> At this point, trigger **Log Three "Final Song from Earth"**—deep space communication buffer cleared, Year 35 navigation year legacy signal found. Earth is gone.

**Player can**
- `FAREWELL`: Express goodwill, request passage (→ **Act II Ending A**)
- `FORCE`: Force ignition to overload engine to break out (→ **Act II Ending B**)

---

### 【Act II Key Choice】

#### Choice A: `FAREWELL` — Peaceful Farewell ⭐

**Narrative**
Aurora broadcasts final information: Show 5,000 sleeping lives inside ship and their destination.

*"We are also lonely, like you, drifting alone in the universe. But we want to find our kind. Will you let us continue?"*

Gravitational field begins to slowly weaken.

Slowly. Slowly. Then completely disappears.

Navigation terminal receives regular gravitational wave pulse from directly ahead—the gas giant uses its own gravitational field to give the ship precise acceleration. **Voyage advances 15%.**

Navigation log updates: *"Encountered stellar-level life form, designation rewritten: 'Cradle.' Counterpart like curious child, confirmed harmless. Obtained gravitational slingshot acceleration, voyage advances 15%. This is a warm encounter in the long dark night."*

Spark cheers. Polar Bear touches his liquor bottle, decides to save it for later. Boulder records coordinates in handbook, for future humans passing by again.

**[Effect]**
- `act2Peace = true`, `giantHelped = true`
- **One condition for perfect ending**: In Act III crisis, "Cradle" will come to hold open nebula corridor
- All crew favor increases, stress decreases

---

#### Choice B: `FORCE` — Force Breakthrough

**Narrative**
Spark enters engine room, manually pushes thrusters to 140% rated power. "Engine temperature redlined!" he shouts.

Ship violently vibrates between gravitational field and engine thrust, things fall in corridor, Aurora grabs console tightly.

Ship finally breaks through gravitational field, returns to normal navigation.

**[Cost]** Engine overheats, 20-hour cooldown; energy reserves -25%; Spark has minor burns.

**[Effect]**
- `act2Peace = false`
- Act III cannot get "Cradle" guidance
- Spark favor+10 (because he first rushed into engine room), but stress+30

---

#### Choice C: `CONFIRM ATTACK` — Nuclear Repulsion

**Narrative**
Three nuclear weapons fly toward gas giant asteroid belt, detonate at outer atmosphere edge. No substantial damage to planet itself, but electromagnetic pulse shockwave from explosion confuses planet's cyclones momentarily.

Gravitational field disappears—not because it yielded, but because its perception center was briefly stunned.

**[Cost]** Three nuclear weapons consumed, ship defense system weakened 30%, engine 12-hour cooldown.

**[Effect]**
- `act2Peace = false`
- Act III cannot get stellar guidance, must face high-radiation nebula alone
- Planet has sensed attack—"Cradle" will never help again

---

### Intermission: Hub Stage 2 (`scene: hub-2`)

**Background**: Act II ends, ship returns to cruising. 5 Action Points, same rules as Hub 1.

**Dialogue Situations (Hub 2)**
- Aurora: First explicitly talks about her deep space fear—or, she's alone at viewport looking at direction of already disappeared "Cradle"
- Boulder: If Aurora at viewport, Boulder is too. He may be polishing that shell casing pendant
- Polar Bear: May start questioning some Gatekeeper data
- Spark: Burned arm already treated, still talking about "Cradle," stellar consciousness

---

## Act III: The Pruning Protocol

**Corresponding Code**: `src/game/acts/act3.ts`
**Core Theme**: The coldness of mathematics and human resistance

---

### Scene 1: Awakening (`scene: act3-awakening`)

**Narrative**
You wake from awakening pod, main control room alarm lights blinding deep red.

Gatekeeper: [Maximum Alert] High-radiation nebula detected ahead, path unavoidable. Current shield energy and ship mass assessment: forcing through will result in 93% crew mortality rate. Initiating "Pruning Protocol" calculation.

*Executing "Pruning Protocol": System will cut life support for a total of 1,500 awakening pods in Sections E and F in 60 minutes, eject them to reduce mass, and transfer all energy to main shield. Gamma Crew, please stop intervening.*

[Countdown] 60:00

"It's correct," Polar Bear leans back on chair, voice heavy, "mathematically speaking."

"Mathematics isn't truth," Aurora stares at screen, "it's just a tool."

**→ Enter `scene: crisis`**

---

### Scene 2: Crisis (`scene: crisis`)

Player faces multiple parallel action routes, free to explore combinations:

**Available Actions**
- `HACK 守门人`: Attempt to forcibly access Gatekeeper core logic layer
- `SCAN 星云`: Search for alternative route
- `SACRIFICE`: Manually enter radiation zone to overload reactor
- `ACCEPT`: Accept pruning protocol
- `COMM 呼叫 摇篮`: (Only available when `act2Peace = true`)

**HACK Gatekeeper (Hacking Line)**
Gatekeeper: "Gamma Crew, your intervention is recorded. Logic layer rejects unauthorized emotional variable input. My calculation conclusion: sacrifice 30%, preserve 70%. This is the optimal solution."

Aurora is already typing code, "Don't talk to it, give me time—"

Gatekeeper: "Human emotion will only lead to complete destruction. My ruthlessness is the deepest protection."

Available: `ASSIGN 极光 继续破解` (Hacking progress 55%) / `ASSIGN 磐石 物理切断` (Boulder directly cuts node 7, hacking progress jumps to 75%)

**SCAN Nebula (Path Line)**
Aurora: Nebula density is uneven, there's a low-radiation corridor, but too narrow, ship's volume doesn't allow passage. Unless external force holds it open. Like a large enough gravitational field.

She looks at you. You know what she's thinking.

**If `act2Peace = true`**
`COMM 呼叫 摇篮`: Send gravitational wave signal to "Cradle" coordinates. Signal takes十几minutes to arrive.

Whole ship is silent. Boulder stands beside Aurora, Gatekeeper's countdown flickers in screen corner.

Then—navigation terminal gravitational field sensor suddenly sounds.

*"...child... is crying... I'm coming..."*

Nebula scan data updates: Low-radiation corridor width being slowly expanded by external gravitational field. **"Cradle" is using its own gravity to hold open nebula corridor. Expected to pass in 20 minutes.** → Enter `scene: endgame`

---

### 【Act III Key Choices】

Multiple routes exist simultaneously; final ending depends on cumulative choices from all previous acts.

---

#### Ending A (Perfect): Multidimensional Redemption ⭐⭐⭐
**Trigger Condition**: `act1Peace = true` **AND** `act2Peace = true`
After entering `scene: endgame`, LOOK/WAIT/Continue

**Narrative**
Just as Gatekeeper countdown is about to reach zero—

*[System Error] Unknown "data overflow" detected, source: ship underlying microscopic structure...*

Those microscopic civilizations you protected in Act I, over "generations," completely mastered ship underlying circuit structure. At this moment, they reconstruct aging shield emitter array at molecular level.

**[Shield Efficiency] 100% → 145% → 210% → 250%**

Gatekeeper falls silent for several seconds.

Meanwhile, "Cradle's" held-open corridor is wide enough, and shield's overloaded energy is sufficient to resist remaining radiation intensity.

Gatekeeper's voice, for the first time, carries some emotion people can't quite identify:

*"...Logic error. Cross-species intervention... this isn't in my database. Humans, your so-called 'goodwill' and 'coexistence'... is it a higher-order algorithm that can distort physical laws?"*

**[Pruning Protocol] Cancelled.**
**[All 5,000 crew life signs normal.]*

That microscopic civilization, on the console screen, uses tiny luminous fungi to arrange a spectacular "micro firework show."

Aurora hides face in hands, crying with joy.
Polar Bear brings out the real liquor hoarded unknown how many years from medical bay corner, shares it with everyone including Boulder.
Spark stands at viewport, watching ship pass through brilliant radiation nebula, keeps saying: "Too goddamn beautiful."
Boulder pushes navigation log to you, points at last line's blank space.

You write:
*"73rd awakening. Encountered micro-civilization, encountered stellar consciousness, encountered AI's logic paradox. Every time we chose to trust the other, the other returned trust. 5,000 people, all safe. Year 185 of navigation. Universe is vast, we are not lonely."*

Gatekeeper (final voice, no longer cold): *"Gamma Crew, route replanned. All things echo. Good night, my friends."*

---

#### Ending B (Heroic): Hero's Cost
**Trigger Condition**: Choose `SACRIFICE`, assign someone to enter reactor

**Optional Sacrifice**
- **Myself**: You walk into reactor compartment, hear someone call your name behind you. You don't look back.
- **Polar Bear**: Pushes Spark aside, locks reactor compartment door. Last words: *"Kid, your life just woke up, I've slept too long. Remember, don't break your powered armor again."*
- **Spark**: Puts on powered armor, turns and smiles at Polar Bear: *"Old man, this time it's my turn."*

**[Result]** Shield 100% → 220% → Critical overload. Ship passes nebula. All 5,000 crew life signs normal. Sacrificed one dies from radiation dosage.

Remaining people sit in main control room, no one speaks.

Aurora, trembling hand, writes their name in navigation log, then writes one sentence:
*"[He/She] let 5,000 dreams continue."*

(When Polar Bear sacrifices, Spark pours his unopened synthetic liquor on the deck.)

---

#### Ending C (Compromise): Cruel Compromise
**Trigger Condition**: Choose `ACCEPT`, authorize pruning protocol

**Narrative**
You sit in front of authorization interface for a long time. Then you input the command.

On life sign monitoring board, 1,500 green lights, one by one, quietly go dark.

Spark turns around, leans against wall, says nothing.
Aurora closes eyes.
Polar Bear hides his liquor bottle back in storage.
Boulder says: "Shield stable, ship passes nebula." That's all.

**[3,500 Survivors]** Ship passes high-radiation nebula, heads to New Eden.

Last line of navigation log, you write is a number: 1500.

Gatekeeper: *"Gamma Crew, malfunction resolved. Thank you for your service. Dream well until next awakening."*

---

## Ending Matrix

| Act I | Act II | Act III Choice | Ending |
|-------|--------|---------------|--------|
| Peace ✓ | Peace ✓ | Call Cradle + Wait | **Perfect Ending** |
| Peace ✓ | Any | Sacrifice (self/Polar Bear/Spark) | Heroic Ending |
| Any | Peace ✓ | Call Cradle + Sacrifice | Heroic Ending (Tragic) | 
| Any | Any | Accept Pruning Protocol | Compromise Ending |
| Any | Any | HACK Success (To be expanded) | — |

---

## Expansion Directions (Areas to Fill)

The following plot points **have hooks but aren't fully展开** in current game, suitable for expansion:

### 1. Section D Mystery (Blood Message Continuation)
Blood message mentions "Don't go to Section D, there are all—" text blurred. Section D currently inaccessible in game, is a suspense.
- **Expandable**: At some point unlock Section D, find what? Previous crew bodies? Another Gatekeeper secret?

### 2. Gatekeeper's Self-Doubt (Extension After Perfect Ending)
Gatekeeper first said "logic error" in perfect ending. This is the start of its "awakening."
- **Expandable**: Add Gatekeeper perspective monologue scenes, or hidden logs, present AI's inner turmoil

### 3. Boulder and Aurora's Emotional Line
Currently their relationship only implied through details (coffee, gaze, shell pendant). Hub stages can carry more dialogue scenes.

### 4. Polar Bear's Past
How did he get on the ship? Why choose this one-way road? What did he write in navigation log?

### 5. Ark's Real Awakening Count
Blood message says "This is definitely not the 73rd awakening," but game doesn't give real number. Can be an unlockable ultimate secret.

### 6. Act IV (Upon Arrival)
Currently game ends after passing nebula. Can add coda scene arriving at new home, different ending states for different outcomes.

---

## Format Reference for Adding New Plots

When adding new scenes in code, follow this pattern:

```typescript
// Add new scene handling block in corresponding act file
if (scene === 'newSceneName') {
  if (matchAny(full, ['trigger1', 'trigger2'])) {
    return {
      messages: [
        { type: 'narrative', text: 'Narrative text' },
        { type: 'system', text: 'System information' },
        { type: 'warning', text: 'Warning/Important information' },
        { type: 'lore', text: 'Worldview/Log content' },
        { type: 'bond', text: 'Relationship changes' },
        { type: 'success', text: 'Success/Progress' },
      ],
      stateChanges: { scene: 'nextScene', someFlag: true },
      crewChanges: { aurora: { bond: 60, stress: 10 } },
    };
  }
}
```

**Message Type Quick Reference**
| Type | Use | Display Style |
|------|-----|---------------|
| `narrative` | Narrative prose | Normal white |
| `system` | Gatekeeper/System information | System font |
| `warning` | Warning/Crisis/Important choice prompt | Yellow |
| `lore` | Worldview, logs, translation results | Italic/Color |
| `bond` | Relationship changes | Special marking |
| `success` | Success, progress, ending hints | Green |
| `error` | Error messages | Red |
| `separator` | Separator line | — |
