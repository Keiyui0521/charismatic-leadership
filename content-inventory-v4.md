# The Dark Side of Charismatic Leadership — Complete Content Inventory (v4)

A linear, top-to-bottom inventory of every element on the page: text, images, quotes, data visualizations, interactive modules, and all their possible states.

Page metadata — Title: `The Dark Side of Charismatic Leadership`. Meta description: `How charismatic leaders dismantle institutions, how movements outlive their founders, and how followers seal themselves inside belief.` Font: Inter (Google Fonts). Theme: dark (#0A0A0A background, #A0A0A0 body text, #F5F5F5 headings, #C0392B accent red). The Takeaway section inverts to a white background with black text.

---

## v4 changelog (from v3)

Changes driven by full-page review feedback:

1. **Hero restructured** — Herbert portrait centered and enlarged; Herbert quote is now a standalone opening element revealed first; title appears on scroll; Paul Atreides photo added after B6.
2. **S1 header image replaced** — `s1-charismatic-leadership.jpg` (comic-style superhero) cut. Replaced with `s1-nuremberg-rally-1934.jpg` (Bundesarchiv, Nuremberg SA/SS rally).
3. **Weber portrait enlarged** — now displayed as a left-right layout (portrait right, text left) or enlarged and centered. No longer small/inline.
4. **Weber → bar graph transition** — added bridging sentence (1.5a) explaining what the bars will show.
5. **Mao "bombard the headquarters" quote moved** — now appears in Step 0 (where the poster is described), not Step 4. It is the catalyst, not the epilogue.
6. **Two Cultural Revolution images added** — `s1-cr-rebellion-poster-1967.jpg` after Step 1, `s1-cr-pla-revolutionary-committee.jpg` after Step 3. Additional CR images available: `s1-cr-struggle-session.jpg`, `s1-cr-execution.jpg`, `s1-cr-beijing-university-rally-1966.jpg`.
7. **Global scrolling principle added** — G3: every scroll-step reveals ONE element. The reader must never see content from the next section while reading the current one. This applies to all prose, images, interactive modules, and transitions throughout the entire page.
8. **All interactive modules enlarged** — G4: interactive visualizations (hemicycle, CR timeline, Weber bars, routinization diagram, Islamic tree, inflate number, polarization dots, dissonance demo, referendum bar, SCOTUS bench, purge grid) must each fill at least 60–80% of the viewport. No module should feel like a thumbnail embedded in an article.
9. **AI writing purge** — G5: all prose must be rewritten to remove AI-flavored sentence patterns. See appendix for the de-AI rewrite rules. This is a global pass applied to every paragraph in the document.
10. **Photo slider alignment** — 2A.11 updated: both image pairs must be cropped/masked to identical aspect ratios. Added contextual paragraph explaining Soviet-era photo retouching techniques (airbrush, darkroom compositing).
11. **Purge counter now scroll-driven** — 2A.14 changed from static snap-count to scroll-driven incremental animation.
12. **Lenin's Testament quote (2A.18) deleted** — redundant; the testament is already quoted in 2A.7 and shown in 2A.8.
13. **Muhammad image caption fixed** — 2B.4 alt/caption changed from "early Islamic world" to conceptual portrait of Muhammad.
14. **Karbala image replaced** — 2B.6: old `s2-karbala.webp` replaced with `s2-karbala-battle.jpg` — visceral oil painting of the Battle of Karbala with close-combat detail.
15. **Islamic tree enlarged** — 2B.10 sizing instruction: tree must fill the full viewport width, not sit inside a 680px content column.
16. **Death counter (632→2026) enhanced** — 2C now shows event labels alongside the cumulative number: as each major conflict is reached (Karbala, Umayyad wars, Iran-Iraq, Iraq, Syria, Yemen), a label fades in identifying the event and its individual toll.
17. **Peng Dehuai section restructured** — 3.4a broken into five granular scroll steps with new image `s3-mao-lushan-conference-1959.jpeg`.
18. **Famine causal explanation added** — Step 5 of inflate scrolly now explains the mechanism: inflated numbers made Beijing believe a surplus existed, so grain was exported and not redistributed; the famine was caused by policy decisions based on false data, not by crop failure alone.
19. **Cognitive dissonance demo expanded** — 3.7 now includes a multi-step reveal with more context on what the buttons represent and what the outcome means historically.
20. **Polarization module clarified** — 3.9 now has inline labels at each phase explaining the real-world analogy, plus a brief intro paragraph before the visualization.
21. **Takeaway shortened and made interactive** — paragraphs cut to 2–3 sentences max. Removed redundant rhetorical build-up. Added scroll-triggered reveals for each principle. The section should feel like an interactive conclusion, not an essay.

---

## Global / persistent elements

| # | Element | Type | Content / behavior |
|---|---------|------|--------------------|
| G1 | Progress navigation | Fixed sticky dots, right edge | Five vertical dots labeled `Introduction`, `When Charisma Meets Power`, `The Movement Outlives the Leader`, `Followers Are Self-Sealing`, `Takeaway`. The dot for the current section is highlighted red. Clicking any dot smooth-scrolls to that section. |
| G2 | No-JS fallback | Safety | If JavaScript is disabled, all scroll-triggered fade-ins become immediately visible so the page remains readable as static prose. |
| G3 | **One-element-per-scroll principle** | Global layout rule | At any scroll position, the reader should see ONLY the current element. No content from the next section, next paragraph, or next module should be visible until the user scrolls to it. This applies to all prose blocks, images, interactive modules, and transitions. Every element occupies its own full viewport or near-full viewport space. Violation of this rule makes the page feel like an article instead of a scrollytelling experience. |
| G4 | **Interactive module sizing** | Global layout rule | All interactive visualizations must fill at least 60–80% of the viewport in both width and height. No module should look like a small widget embedded in text. The visualization IS the content — text supports it, not the other way around. |
| G5 | **AI writing purge** | Global content rule | All prose must pass through a de-AI rewrite. See Appendix B for the full rewrite rules. In brief: eliminate hollow rhetorical structures ("Not X, but Y"), inflated adjectives (comprehensive, robust, seamless, nuanced, transformative), fake-depth sentence patterns, and filler transitions. Replace with short declarative sentences, specific claims, and abrupt endings. If a sentence is hollow after stripping the structure, delete it. |

---

## SECTION A — Hero Intro (scroll-driven opening)

A tall (300vh) section with a sticky inner panel pinned to the viewport. The user must scroll through it to reveal each line.

| # | Element | Type | Content / behavior |
|---|---------|------|--------------------|
| A1 | `58,000` | Huge red number (dominant, full viewport height) | Visible on load, centered. |
| A2 | `scroll ↓` | Small gray hint text, bottom center | Gently bobs up/down. Fades out after the user begins scrolling. |
| A3 | `Americans killed in Vietnam.` | Medium white line | Fades in at ~18% scroll progress through the intro. |
| A4 | `Because no one questioned a charismatic president.` | Italic muted line, smaller | Fades in at ~42% scroll progress. |
| A5 | Whole intro panel | Fade-out | At ~78% progress the entire panel fades to 0 opacity, revealing the Hero section beneath. |

---

## SECTION B — Hero

**Restructured layout (v4):** The Hero is no longer a single static screen. It is a scroll-driven sequence:

**Phase 1 — The Warning (full viewport, centered)**

| # | Element | Type | Content |
|---|---------|------|---------|
| B1 | Herbert portrait | `opening-frankherbert.jpg` | **Centered, large** (not small top-right). Grayscale, ~40% viewport width. Alt: "Portrait of Frank Herbert." |
| B2 | Hero quote | Italic pull-quote, centered below portrait | `"I wrote the Dune series because I had this idea that charismatic leaders ought to come with a warning label on their forehead: 'May be dangerous to your health.'"` — cite: `— Frank Herbert, UCLA, 1985`. |

This phase occupies a full viewport. The reader sees Herbert's face and his warning. Nothing else.

**Phase 2 — The Title (scroll to reveal)**

| # | Element | Type | Content |
|---|---------|------|---------|
| B3 | Title | `<h1>`, scroll-triggered fade-in | `The Dark Side of Charismatic Leadership` (two lines). Centered or left-aligned, large. |

**Phase 3 — The Context (scroll to reveal, one element at a time)**

| # | Element | Type | Content |
|---|---------|------|---------|
| B4 | Background image | `opening-JFK-Nixon-debate.jpg` | Fades in as subtle background at 15% opacity, grayscale. Alt: "John F. Kennedy and Richard Nixon at their first televised presidential debate, Chicago, 1960." |
| B5 | Body paragraph 1 | Prose | `Seventy million Americans watched that debate. The ones who listened on radio thought Richard Nixon won. The ones who watched on television were certain it was John F. Kennedy. Same words. The only difference was the screen.` |
| B6 | Body paragraph 2 | Prose | `Frank Herbert watched a science fiction audience fall in love with Paul Atreides — the hero of Dune — and it horrified him. He had written Paul as a warning. Readers took him as a savior. So Herbert wrote sequel after sequel to make the point as brutal as possible: the hero will destroy you. Not because he wants to. Because you will let him.` |
| B6a | Paul Atreides image | `opening-paul-atreides.png` | Film still of Timothée Chalamet as Paul Atreides in Dune (2021). Alt: "Paul Atreides." Caption: `The hero Herbert tried to warn you about.` |
| B7 | Body paragraph 3 | Prose | `What happens when people stop questioning. How institutions collapse. How movements outlive the people who started them. How followers seal themselves inside a belief until nothing can reach them.` |

---

## SECTION 1 — When Charisma Meets Power

### Part I — The Theory

| # | Element | Type | Content |
|---|---------|------|---------|
| 1.1 | Section label | Red small-caps | `Section 1` |
| 1.2 | Section title | `<h2>` | `When Charisma Meets Power` |
| 1.2a | Full-bleed header image | `s1-nuremberg-rally-1934.jpg` | Bundesarchiv photograph of the 1934 Nuremberg Rally — massed SA and SS troops in formation. Alt: "SA and SS formations at the Nuremberg Rally, 1934." Replaces the comic-style superhero image. |
| 1.3 | Part label | `<h3>` | `Part I — The Theory` |
| 1.4 | Weber intro paragraph | Prose | `In 1922, Max Weber identified three sources of political authority: tradition, law, and charisma. The first two are stable — they survive the death of any individual. Charisma does not. It lives in one person, and it demands total faith in that person.` |
| 1.5 | Weber portrait | Image — **ENLARGED** | `s1-weber-portrait-1918.jpg` — **Layout: either (a) enlarged and centered as a standalone image block, or (b) placed on the right side with the Weber text (1.4, 1.7) flowing on the left.** No longer a small inline thumbnail. Alt: "Max Weber, 1918." |
| 1.5a | **Weber → bars transition** (NEW) | Prose | A bridging sentence before the bars that explains what they will show: `Weber's three types of authority are not equal in practice. When charisma enters the room, the other two buckle.` |
| 1.6 | **Weber three-authority animated bars** | Interactive visualization | Three equal-height vertical bars labeled **Tradition**, **Law**, **Charisma**. On load, all three are dark gray except Charisma, which is red and pulses with a glowing halo. When the bars scroll into view: Charisma expands to ~2× height and Tradition + Law collapse to stubs with a diagonal striped "broken" texture overlaid — visually Charisma crushes the other two. **Must fill at least 60% of viewport height per G4.** |
| 1.7 | Weber pull-quote | Blockquote | `"A certain quality of an individual personality by virtue of which he is set apart from ordinary men and treated as endowed with supernatural, superhuman, or at least specifically exceptional powers."` — cite: `— Max Weber, Economy and Society, 1922` |
| 1.7a | Weber-era oratory image | `s1-weber-oratory.png` | Alt: "Illustration of an early-20th-century crowd listening to a charismatic orator." Caption: `The kind of scene Weber had in mind: a crowd listening, all at once, to one man.` |
| 1.8 | Madison paragraph | Prose | `Institutions — legislatures, courts, free presses — exist because the system expects leaders to be flawed. Madison put it plainly in Federalist No. 51: "If men were angels, no government would be necessary." Every check, every balance, every procedural delay is built on that assumption.` |
| 1.9 | Charisma-breaks-assumption paragraph | Prose | `Charisma breaks the assumption. When followers believe a leader is exceptional, the checks start looking like obstacles. The followers want them gone. And the leader, surrounded by devotion, starts to agree.` |
| 1.10 | Routinization paragraph | Prose | `Weber saw further than the moment of seizure. Charismatic authority is unstable — it cannot outlast the leader. It must undergo what he called routinization: it hardens into bureaucratic rule, fractures into competing traditions, or the institutions hold and charisma fades. The next sections are three variations of that process — and the question of whether there is a fourth.` |
| 1.11 | **Routinization pathway diagram** | Animated SVG | A single node labeled **Charisma** at top, with three branching paths downward. Path A: `Routinized into Bureaucracy` (labeled `Lenin → Stalin`). Path B: `Fractured into Competing Traditions` (labeled `Muhammad → The Schism`). Path C: `Constrained by Institutions` (labeled `?`, dimmed, with a subtle lock icon). On scroll, paths A and B illuminate sequentially; path C stays dim with a pulsing `?` — it is answered in the Takeaway. **Must fill full viewport per G4.** |

### Part II — The Enabling (sticky scrollytelling — Reichstag vote)

Part label: `Part II — The Enabling`.

Left half of viewport: **hemicycle parliament visualization**. A dot-graphic of ~535 seats arranged in a half-circle (the Reichstag). All seats start dark gray. **Hemicycle must fill at least 50% of viewport width and be vertically centered per G4.**

Right half: four narrative "steps" that the user scrolls through. As the user scrolls, seats fill continuously with red from the right side inward.

| Step | Narrative content | Hemicycle state |
|------|-------------------|-----------------|
| Step 0 | Image `s1-hitler-reichstag.jpg` (alt: "Hitler at the Kroll Opera House, March 1933"; caption: "The Kroll Opera House, Berlin, March 1933"). Then paragraphs: `Berlin, March 23, 1933. The Kroll Opera House, draped in swastika banners. Hitler stands before the Reichstag and asks for the legal authority to rule by decree.` and `The Enabling Act would let him bypass parliament, bypass the constitution, bypass every safeguard the Weimar Republic had built. A democracy would become a dictatorship — through a vote.` | All seats dark gray. |
| Step 1 | `**The Nazi Party holds 288 seats.** They don't have a two-thirds majority alone. But the SA stormtroopers stand outside the building. The Communist Party's 81 deputies have already been arrested or barred from attending.` | Seats fill red progressively from the right, reaching 288 red Nazi seats. |
| Step 2 | `**The Centre Party caves.** Hitler promises to respect the Church. The promise is worthless, but the Centre's leader, Ludwig Kaas, tells his caucus to vote yes. One by one, the smaller parties fall in line. The pressure of the crowd, the SA outside, the momentum — resistance feels pointless.` | Red continues extending leftward, reaching 441 red seats. |
| Step 3 | Image: `s1-otto-wels-portrait.jpg` (alt: "Otto Wels, SPD chairman"; caption: "Otto Wels, 1933"). Then: `**Only the Social Democrats hold.** 94 votes against, in a room full of men who have already surrendered. Otto Wels, the SPD leader, stands to speak: "You can take our liberty and our lives, but you cannot take our honor."` followed by `No tanks. No gunfire. The institutions of German democracy were not destroyed by force. Elected officials handed them over, to a man whose crowds made resistance feel pointless.` | 441 seats locked red (Nazis + allies), the remaining 94 SPD seats switch to dim gray. Count display fades in showing `441 IN FAVOR` / `94 AGAINST`. |

### Part III — The Fire (sticky scrollytelling — Cultural Revolution)

Part label: `Part III — The Fire`.

Left half: **Cultural Revolution timeline visualization**. A giant year number (120px), an event description below, a horizontal red intensity bar that grows 0→100%, and a death-toll line that appears at the end. **Timeline viz must fill at least 50% of viewport width per G4.**

| Step | Narrative content | Visualization state |
|------|-------------------|---------------------|
| Step 0 | Image `s1-cultural-revolution.jpg` (alt: "Red Guards rally in Beijing, 1966"; caption: "Red Guards rally, Beijing, 1966"). Second image `s1-mao-tiananmen.jpg` (alt: "Mao Zedong reviewing Red Guards from atop the Tiananmen Gate"; caption: "Mao reviews the Red Guards from Tiananmen Gate, August 1966."). Then blockquote **(MOVED from Step 4)**: `"To rebel is justified — bombard the headquarters!"` cite `— Mao Zedong, 1966`. Then paragraphs: `Beijing, May 1966. Mao Zedong is 72. He has led the People's Republic for seventeen years, but his grip on the Party is slipping. Rivals in the Politburo are quietly sidelining him.` and `So Mao goes around them. He bypasses his own party, his own government, his own chain of command. He writes a big-character poster — "Bombard the Headquarters" — and calls on China's students to attack the system he built.` | Year `1966`, intensity bar empty. |
| Step 1 | `Mao mobilizes millions of Red Guards. They flood the streets, drag professors from classrooms, beat officials in public, destroy temples, burn books. The chaos is total. The loyalty is absolute.` Image: `s1-cr-rebellion-poster-1967.jpg` (alt: "Cultural Revolution woodcut propaganda poster, 1967 — 'Revolution is innocent, rebellion is justified'"; caption: "1967. 'Revolution is innocent, rebellion is justified.'"). | Year `1966`, event `Mao mobilizes Red Guards`, intensity 25%. |
| Step 2 | `Red Guard factions turn on each other. Provincial governments collapse. Liu Shaoqi — the second most powerful man in China — is dragged from his home and left to die in detention. The revolution is eating its own.` Image: `s1-anti-liu-shaoqi-poster.jpg` (alt: "Anti-Liu Shaoqi propaganda poster during the Cultural Revolution"; caption: "Liu Shaoqi, denounced as 'China's Khrushchev.' Died in detention, 1969."). | Year `1967`, event `Factions turn on each other. Governments collapse.`, intensity 55%. |
| Step 3 | `Even Mao cannot stop it. He sends the army to suppress the Red Guards — the very forces he summoned two years earlier. The weapon he built no longer answers to him.` Image: `s1-cr-pla-revolutionary-committee.jpg` (alt: "People's Liberation Army troops massed with rifles and red flags at a rally celebrating the Beijing Revolutionary Committee"; caption: "The PLA takes control. The revolution Mao started now requires an army to contain."). | Year `1968`, event `Army deployed to suppress Red Guards`, intensity 80%. (Then `1969` / `Violence continues in provinces` / 65% as a decay state.) |
| Step 4 | `The Cultural Revolution officially ends. The toll: an estimated 500,000 to 2 million dead, up to 36 million persecuted.` Causal annotation (smaller muted text below death toll): `Courts suspended. Local governments collapsed. The military was politicized. No institution remained that could stop the violence — because the one man who stood above all institutions had told the people to destroy them.` Then paragraph: `Hitler got the institutions out of his way. Mao went further — he unleashed a force that got out of *his* way.` | Year `1976`, event `Cultural Revolution ends`, intensity 100%, death toll `500,000 – 2,000,000 dead` appears with causal annotation fading in below. |

---

## SECTION 2 — The Movement Outlives the Leader

### Case A — Lenin → Stalin

| # | Element | Content |
|---|---------|---------|
| 2A.1 | Section label | `Section 2` |
| 2A.2 | Section title | `The Movement Outlives the Leader` |
| 2A.3 | Case label | `Case A — Lenin → Stalin` |
| 2A.4 | Routinization framing | Prose (italic, muted) | `Weber called this routinization — the moment when a movement built on one man's charisma must find a way to survive without him. Lenin's revolution would become Stalin's bureaucracy: the personal cult frozen into institutional terror.` |
| 2A.5 | Image | `s2-lenin-stalin.jpg` — alt: "Lenin and Stalin at Gorki, 1922" — caption: "Lenin and Stalin, Gorki, 1922". |
| 2A.6 | Image | `s2-lenin-last-photo-1923.jpg` — alt: "Vladimir Lenin in a wheelchair at Gorki, 1923, after his third stroke, with his sister Anna Yelizarova" — caption: "Lenin at Gorki, summer 1923. After three strokes, he could no longer speak. This is his last known photograph." |
| 2A.7 | Testament paragraphs | `Vladimir Lenin died on January 21, 1924. He had spent his final months writing a document that the Party would later call his "Testament." In it, he warned that Stalin was "too rude" and should be removed from the position of General Secretary. He proposed replacing him with someone "more patient, more loyal, more polite."` / `The Testament was read aloud at the 13th Party Congress. The delegates listened, discussed it briefly, and did nothing.` |
| 2A.8 | **Testament manuscript interactive** | Image: `s2-lenin-testament-manuscript.jpg` (alt: "Typewritten page of Lenin's Testament addition, January 4, 1923, in Russian"). On click or hover, a translucent dark overlay appears with an English translation typeset line-by-line over the Russian text (Resident Evil 2 remake inspection style). The final line — `"I propose to find a way to remove Stalin from that position"` — is highlighted in red. A small label reads `Click to translate`. |
| 2A.9 | Image | `s2-stalin-propaganda-1.jpg` — alt: "Soviet propaganda poster, 1933" — caption: `"With the banner of Lenin..." — Soviet propaganda, 1933`. |
| 2A.10 | Stalin consolidation paragraphs | `Stalin kept his position. Within five years, he had outmaneuvered every rival. He renamed Petrograd — the city where the revolution began — to Leningrad. He turned Lenin's body into a public relic, preserved in a glass case on Red Square. He wrapped every policy in Lenin's language, every purge in Lenin's authority. The dead man could not object.` / `By the mid-1930s, Stalin had built something Lenin never intended: a totalitarian state where disagreement was a death sentence. The Great Purge of 1936–1938 executed or imprisoned hundreds of thousands — party members, military officers, intellectuals, anyone who might challenge Stalin's reading of what Lenin "really meant."` |
| 2A.11 | Erasure intro | Italic line: `Execution was not enough. The Party rewrote the visual record, erasing rivals from official photographs. Drag the slider to see what was removed.` **NEW contextual paragraph (v4):** `These alterations were not digital. Soviet retouchers used airbrushes, ink, and darkroom compositing to paint people out of negatives and prints by hand. The process could take days. The results were distributed as official history — the doctored versions replaced the originals in archives, newspapers, and textbooks. What you see below is not a Photoshop exercise. It is what the state actually did.` |
| 2A.12 | **Before/after slider #1 — Lenin / Trotsky** | Interactive drag-slider. Original photograph (`s2-lenin-original.jpg`, alt: "Lenin speaking at Sverdlov Square, 1920, with Trotsky and Kamenev beside the podium") on the left; retouched photograph (`s2-lenin-removed.jpg`, alt: "The same photograph after Stalin-era retouching, with Trotsky and Kamenev erased") on the right. A red vertical divider with a white-bordered circular red handle marked `⇆` can be dragged left and right. Labels below: `Original (1920)` / `Retouched`. Caption: `Lenin at Sverdlov Square, 1920. Trotsky and Kamenev stood beside the podium — until they didn't.` **v4 note: both images must be cropped/masked to identical aspect ratios to prevent misalignment.** |
| 2A.13 | **Before/after slider #2 — Stalin / Yezhov** | Same component. Original (`s2-stalin-original.jpg`, alt: "Stalin walking with Nikolai Yezhov along the Moscow-Volga Canal") / retouched (`s2-stalin-removed.jpg`, alt: "The same photograph after Yezhov's execution, with Yezhov erased"). Labels: `Original` / `After Yezhov's execution`. Caption: `Stalin and secret police chief Nikolai Yezhov at the Moscow Canal. After Yezhov was shot in 1940, he vanished from the photograph too.` **v4 note: same aspect-ratio alignment rule as 2A.12.** |
| 2A.14 | **Purge statistics counter** — **NOW SCROLL-DRIVEN (v4)** | Two large red numbers that **increment as the user scrolls** (not a static snap-count). The numbers climb from 0 to their final values (`Executed` / `Sent to Gulag`) across a dedicated scroll zone (~150vh). The effect should feel like watching the toll accumulate in real time. |
| 2A.15 | **Purge grid** | A dense grid of hundreds of tiny tombstone-shaped dots. On entry, dots progressively turn red (`executed`) and dark red (`gulag`) to visualize the scale of the purge victims. |
| 2A.15a | Image | `s2-stalin-propaganda-2.jpg` — alt: "Soviet poster glorifying Stalin alongside Lenin's image" — caption: `As the purges intensified, Stalin's image multiplied — always beside Lenin's, always borrowing his authority.` |
| 2A.16 | Image | `s2-gulag-workers.jpg` — alt: "Gulag prisoners building the White Sea-Baltic Canal" — caption: "Prisoners at Belbaltlag, building the White Sea–Baltic Canal". |
| 2A.17 | Closing paragraph | `Lenin's revolution was supposed to liberate the working class. Under Stalin, it became the justification for a system of forced labor camps stretching across Siberia. The ideology did not change. The words stayed the same. Only the meaning shifted — and there was no one left alive who was allowed to say so.` |

**2A.18 — DELETED (v4).** The Lenin's Testament blockquote that was here is redundant — the testament is already quoted in 2A.7 and displayed interactively in 2A.8.

### Case B — Muhammad → The Fracture

| # | Element | Content |
|---|---------|---------|
| 2B.1 | Case label | `Case B — Muhammad → The Fracture` |
| 2B.2 | Framing disclaimer | Prose (italic, muted, smaller font) | `A note on framing: for nearly two billion Muslims, Muhammad is not a case study in political leadership — he is the Prophet. This section uses Weber's secular academic framework to analyze the political consequences of a succession crisis, not to pass judgment on faith or religious authority. The analysis that follows concerns institutions, not theology.` |
| 2B.3 | Routinization framing | Prose (italic, muted) | `Where Lenin's charisma was routinized into a single bureaucratic tyranny, Muhammad's faced a different fate. Without a clear succession mechanism, charismatic authority did not harden into one structure — it fractured into competing claims of legitimate inheritance. Weber's routinization, split in two.` |
| 2B.4 | Image | `s2-muhammad.jpg` — **CORRECTED (v4):** alt: "Conceptual artistic portrait of the Prophet Muhammad" — caption: "A conceptual portrait. In Islamic tradition, figurative depictions of the Prophet vary by era and region." |
| 2B.5 | Succession paragraphs | `Muhammad died in Medina on June 8, 632 CE. He left behind a community of believers, a rapidly expanding territory, and no clear successor.` / `Within hours, the crisis began. One faction backed Abu Bakr, Muhammad's closest companion. Another insisted on Ali, his cousin and son-in-law — the man they believed Muhammad had designated at Ghadir Khumm. Both sides were certain. Neither side could ask the only person whose answer would have settled it.` |
| 2B.6 | Full-bleed image | `s2-karbala-battle.jpg` — alt: "The Battle of Karbala, 680 CE — oil painting depicting the close-combat massacre of Husayn's forces". Stretches edge-to-edge. Replaces the old blurry `s2-karbala.webp`. |
| 2B.7 | Image caption line | Italic `The Battle of Karbala, 680 CE` |
| 2B.8 | Karbala paragraph | `Abu Bakr became the first caliph. Over the next three decades, three of the first four caliphs were assassinated. In 680 CE, Ali's son Husayn marched to Karbala to challenge the Umayyad caliph Yazid. His forces were massacred. That death became the founding trauma of Shia Islam — a grief re-enacted every year during Ashura, fourteen centuries later.` |
| 2B.9 | Image | `s2-ashura.jpeg` — alt: "Ashura commemoration" — caption: "Ashura commemoration — mourning Husayn, 1400 years later". |
| 2B.10 | **Islamic schism branch tree (interactive SVG)** — **ENLARGED (v4)** | A top-down family tree showing the fracture of Islam into branches. **Must fill full viewport width (not constrained to 680px content column). Minimum height: 70vh.** Hovering any node surfaces a tooltip with a title and explanation. Full node list below. |

**Islamic branch tree — all nodes and tooltips:**

Root: **Muhammad** (red, with label `d. 632 CE`). Tooltip: `Prophet of Islam, d. 632 CE in Medina. His death without a clear successor triggered the central schism of Islamic history.`

Level 1 — the primary split:
- **Sunni** — Tooltip: `~85% of Muslims worldwide. Recognize Abu Bakr as rightful first caliph. Authority from community consensus.`
- **Shia** — Tooltip: `~15% of Muslims worldwide. Believe Ali was Muhammad's designated successor. Authority through the Prophet's bloodline.`

Level 2 — four Sunni jurisprudence schools:
- **Hanafi** — `Largest Sunni school. Dominant in Turkey, Central/South Asia. Emphasizes reason and analogy.`
- **Maliki** — `Dominant in North/West Africa. Emphasizes the practice of Medina as legal source.`
- **Shafi'i** — `Dominant in Southeast Asia, East Africa. Systematized Islamic legal sources.`
- **Hanbali** — `Most conservative school. Dominant in Saudi Arabia. Source of Wahhabism and Salafism.`

Level 3 — three Shia branches:
- **Twelvers** — `Largest Shia branch (~85% of Shia). Believe in 12 divinely appointed Imams. Dominant in Iran, Iraq, Lebanon.`
- **Ismailis** — `Split over the 7th Imam. Led by the Aga Khan. Prominent in South/Central Asia, East Africa.`
- **Zaidis** — `Closest to Sunni theology. Concentrated in Yemen.`

Level 4 — derivative movements:
- **Wahhabism** — `18th-century revivalist movement. Allied with House of Saud. State ideology of Saudi Arabia.`
- **Salafism** — `Modern fundamentalist movement. Includes quietist, activist, and jihadist strands.`
- **Usuli / Akhbari** — `Competing Twelver schools on clerical authority. Usuli dominates modern Iran.`
- **Iranian Theocracy** — `Est. 1979. Velayat-e faqih: rule by Islamic jurist. Fusion of Twelver theology and state power.`

Level 5 — section header `MODERN FRAGMENTATION`. Nodes (no tooltips): `Fundamentalists`, `Extremists` (red), `Secularists`, `Reformists`, `Nationalists`, `Modernists`.

Level 6 — section header `SECTARIAN CONFLICTS — DEATH TOLL`. Four boxed conflicts with red-tinted borders:
- **Iran-Iraq War** `~1,000,000 dead` — tooltip: `Iran-Iraq War (1980–1988) — Shia Iran vs Sunni-led Iraq. One of the deadliest wars of the 20th century.`
- **Iraq Civil War** `~200,000 dead` — tooltip: `Iraq Civil War (2003–2011) — Sunni-Shia sectarian violence after the US invasion.`
- **Syrian War** `~500,000 dead` — tooltip: `Syrian Civil War (2011–present) — Multi-faction war with strong sectarian dimensions.`
- **Yemen War** `~150,000+ dead` — tooltip: `Yemen Civil War (2014–present) — Zaidi Shia Houthis vs Saudi-backed Sunni government.`

Tree footer line: `1,850,000+ lives — in conflicts shaped by a fracture that began in 632 CE` (red).

Image: `s2-syria-aleppo-destruction.jpg` — full-bleed, similar treatment to Karbala image. Alt: "Destroyed buildings in Aleppo, Syria, during the civil war." Caption: "Aleppo, Syria. One of the oldest continuously inhabited cities in the world, reduced to rubble in a war with deep sectarian dimensions."

### 2B.11 — Causal complexity bridge

| # | Element | Content |
|---|---------|---------|
| 2B.11 | Bridge paragraph | `No war on that list was caused by theology alone. The Iran-Iraq War was triggered by border disputes, revolutionary export, and Cold War maneuvering. The Iraq Civil War followed a foreign invasion. The Syrian War began as a political uprising. The Yemen War is tangled in Saudi-Iranian rivalry and resource competition. Each conflict had its own proximate causes, its own geopolitics, its own cynical actors. But each one also cracked along the same fault line — the question of who inherited Muhammad's authority. Fourteen centuries later, that fracture has not healed. It does not cause the wars. It shapes where they break.` |

### 2C — 632 → 2026 sticky death-toll counter — **ENHANCED (v4)**

A full-viewport sticky scroll sequence (220vh tall) pinned while the user scrolls.

| # | Element | Behavior |
|---|---------|----------|
| 2C.1 | Year label (small) | `Year 632` at the top, counts upward in real time from 632 to 2026 as the user scrolls. |
| 2C.2 | **Huge red death toll** | Enormous red number at center, counting from `0` upward. Historical interpolation: roughly 10,000 by 680 (Karbala era), 80,000 by 750 (Umayyad civil wars), 120,000 by 1500, 150,000 by 1900/1980, jumps sharply to ~1,150,000 after the Iran-Iraq War (1988), 1,400,000 after the Iraq civil war (2011), 1,700,000 after the Syrian war (2014), and finishes at **1,850,000** at 2026. |
| 2C.2a | **Event labels (NEW v4)** | As the counter reaches each major conflict threshold, an event label fades in below or beside the number identifying the conflict and its individual toll: `Karbala & early succession wars — ~10,000`, `Umayyad civil wars — ~70,000`, `Iran-Iraq War (1980–88) — ~1,000,000`, `Iraq Civil War (2003–11) — ~200,000`, `Syrian Civil War (2011–) — ~500,000`, `Yemen Civil War (2014–) — ~150,000+`. Each label fades in as its conflict is reached, then fades to muted text as the counter continues. This grounds the cumulative number in specific, identifiable events so the total does not feel invented. |
| 2C.3 | Sub-label | Italic `killed in conflicts with sectarian dimensions — each triggered by its own political crisis, none reducible to religion alone`. |

---

## SECTION 3 — Followers Are Self-Sealing

### Part 1 — The inflating number (sticky scrollytelling — Great Leap Forward)

| # | Element | Content |
|---|---------|---------|
| 3.1 | Section label | `Section 3` |
| 3.2 | Section title | `Followers Are Self-Sealing` |
| 3.3 | Image | `s3-great-leap-forward-furnaces.jpg` — alt: "Backyard steel furnaces during China's Great Leap Forward" — caption: "Backyard steel furnaces, China, late 1950s". |
| 3.4 | Henan paragraphs | `Somewhere in rural Henan province, 1959. A local Party secretary stands in a field. The wheat is thin. He knows the harvest will fall short — maybe thirty percent of last year. He also knows what happened to the last official who reported low numbers. The man was denounced as a rightist, stripped of his position, and sent to a labor camp. His family was not told where.` / `The secretary writes his report. Record yield. Twice the actual harvest. He sends it up the chain.` |

### 3.4a — Peng Dehuai: the cost of telling the truth — **RESTRUCTURED (v4)**

This sub-section is now a **dedicated scroll sequence** with five discrete steps. Each step occupies its own viewport. The reader scrolls through them one at a time.

| Step | Element | Content |
|------|---------|---------|
| Step 1 | Image — Peng Dehuai military portrait | `s1-peng-dehuai-military-portrait.jpg` (alt: "Marshal Peng Dehuai in military uniform before persecution"; caption: "Peng Dehuai — defense minister, war hero, veteran of Korea."). Full viewport, centered. |
| Step 2 | Paragraph | `Not everyone lied. In July 1959, Marshal Peng Dehuai — China's defense minister and one of the most decorated commanders of the Korean War — wrote a private letter to Mao at the Lushan Conference. He called the backyard steel campaign "a waste of resources and manpower." He said the harvest numbers were inflated. He was right about everything.` |
| Step 3 | Paragraph + image | `Mao read the letter aloud to the Politburo — not to act on it, but to force everyone in the room to choose a side.` Image: `s3-mao-lushan-conference-1959.jpeg` (alt: "Mao Zedong at the Lushan Conference, 1959"; caption: "Lushan, July 1959. Mao turns Peng's letter into a loyalty test."). |
| Step 4 | Image + paragraph | `s1-peng-dehuai-struggle-session.jpg` (alt: "Marshal Peng Dehuai subjected to a struggle session by Red Guards"; caption: "The same man, after. Beaten until his back was broken. Died in prison, 1974."). Then: `Peng was stripped of all positions, placed under house arrest, and eventually handed to the Red Guards.` |
| Step 5 | Paragraph | `The message was clear: the system does not lack information. It punishes the people who carry it. Every official in the chain below Peng understood what his fate meant for theirs.` |

**Inflate scrolly** — sticky center panel shows a single huge number with a role label (who is reporting) and a sublabel. As the user scrolls, the number grows (both physically larger and color-shifts from white toward red). **Number must fill at least 40% of viewport width per G4.** Six steps:

| Step | Number | Role label | Overlay card text |
|------|--------|------------|--------------------|
| 0 | `100 tons` | Actual harvest | `The actual harvest: roughly **100 tons**. The Party secretary knows this. Everyone in the village knows this.` |
| 1 | `200 tons` | Village secretary | `The village secretary writes **200 tons**. Double the truth. He has seen what happens to those who report low numbers.` |
| 2 | `350 tons` | County official | `The county official receives six reports, all inflated. He adds his own margin. **350 tons.**` |
| 3 | `600 tons` | Prefecture | `The prefecture consolidates. Nobody wants to be the one with lower numbers. **600 tons.**` |
| 4 | `1,000 tons` | Provincial report → Beijing | `The provincial report reaches Beijing. **1,000 tons.** Ten times reality. Mao reads this and orders the surplus exported.` |
| 5 | Collapse into famine | — | Card with red border: `**The number collapses into reality.** Beijing believed the inflated harvest reports. Grain was exported to repay Soviet debts and fund industrialization. Local food reserves were seized for redistribution to cities. No one sent food back — because the numbers said there was more than enough. There was famine not because the crops failed, but because the system acted on lies as if they were true.` |

After the scrolly ends, a full-width black panel displays:

Image: `s3-great-famine-victims.jpg` — alt: "A family during the Great Chinese Famine, 1959–1961" — caption: "Rural China, 1959–1961. The surplus did not exist. The famine did." Displayed above the counter, muted grayscale, giving the number a human face.

The **famine counter**: a huge number that counts up (from 0) on entry to a final estimated death toll. Causal annotation below the number (smaller muted text): `The information that could have prevented this existed at every level of the system. It could not travel upward — because the system was sealed against it.` Label: `estimated deaths, 1959–1961`.

### Part 2 — Festinger / cognitive dissonance

| # | Element | Content |
|---|---------|---------|
| 3.5 | Information-seal paragraph | `Every local official in the chain knew the real numbers. The information that could have prevented the famine existed at every level. It could not travel upward, because traveling upward meant telling Mao he was wrong, and telling Mao he was wrong meant destruction. The system did not lack information. It was sealed against it.` |
| 3.6 | Festinger blockquote | `"A man with a conviction is a hard man to change. Tell him you disagree and he turns away. Show him facts or figures and he questions your sources. Appeal to logic and he fails to see your point."` — cite: `— Leon Festinger, 1957` |
| 3.7 | **Cognitive-dissonance interactive demo** — **EXPANDED (v4)** | A dark card with a multi-step scroll-driven reveal. **Step 1:** A scene-setting line fades in: `You are a county official in Henan province, 1959. You have just inspected the fields yourself.` **Step 2:** The fact: `The harvest was **100 tons.**` **Step 3:** In red: `The Party says the harvest was **1,000 tons.**` **Step 4:** A line of context: `The last official who reported real numbers was sent to a labor camp. His family does not know where he is.` **Step 5:** Prompt: `WHAT DO YOU REPORT?` Two buttons appear: `Report 100 tons (the truth)` / `Report 1,000 tons (the Party line)`. Clicking either button: the unchosen button fades to 30% opacity. If "truth": result text `You have chosen what Peng Dehuai chose. He was stripped of his rank, beaten, and died in prison.` If "Party line": result text `You have chosen what every official in the chain chose. The grain was exported. Your village starved.` Final line (shown for both): `In 1959, every official chose the Party line. Not because they believed it — but because the cost of honesty was higher than the cost of famine.` Both buttons lock after clicking. **Must fill at least 60% of viewport per G4.** |

### Part 2b — From Individual to Crowd (the bridge)

| # | Element | Content |
|---|---------|---------|
| 3.8 | Bridge paragraph 1 | `Festinger described a defense mechanism inside one person's head. Cass Sunstein studied what happens when people who share a belief are placed together: the group does not settle at the average. It moves toward the extreme. He called this group polarization. In a room where everyone agrees, the most forceful voice sets the new anchor. Moderate positions feel like betrayal.` |
| 3.8a | **Polarization intro (NEW v4)** | A brief setup line before the visualization: `The simulation below shows how this works. Each dot is a person. Watch what happens when they find others who agree with them — and what happens when the algorithm decides what they see.` |
| 3.9 | **Polarization drift simulation** — **CLARIFIED (v4)** | Interactive scroll-driven visualization. **Must fill at least 70% of viewport per G4.** A field of ~60 small dots, initially scattered randomly across a horizontal spectrum (left to right = opinion range). As the user scrolls: **Phase 1** (Festinger — individual): dots are randomly placed, each a slightly different shade. Label: `Individual beliefs — scattered. Each person holds their own position.` **Phase 2** (Sunstein — group): dots drift toward 3–4 clusters, leaving empty space in the center. Clusters tighten. Label: `Group polarization — people find others who agree. The center empties. Moderates are pulled to the nearest cluster or go silent.` **Phase 3** (Pariser — algorithm): each cluster drifts further toward the edges. A semi-transparent bubble border appears around each cluster. Label: `Filter bubbles — the algorithm shows you what keeps you engaged. You stop seeing the other side. Not because it disappeared, but because the feed decided it wasn't relevant.` Final state: two dense clusters at far left and far right, wide empty center, each enclosed in a bubble. |
| 3.10 | Bridge paragraph 2 | `Eli Pariser identified the infrastructure that automates Sunstein's process. Social media algorithms optimize for engagement. Devotion engages. Doubt does not. The filter bubble is an environment where the information you see is pre-selected to confirm what you already believe. The technology is new. The psychology is Festinger's. The group dynamics are Sunstein's. The scale is what changed.` |

### Part 3 — The Confession (Moscow Show Trials)

| # | Element | Content |
|---|---------|---------|
| 3.11 | Subheading | `The Confession` |
| 3.12 | Image | `s3-moscow-trial.jpg` — alt: "Moscow Show Trials courtroom, 1936-1938" — caption: "Moscow Show Trials, 1936–1938". |
| 3.13 | Image | `s3-bukharin-portrait.jpg` — alt: "Nikolai Bukharin, Party theoretician and editor of Pravda, before his arrest" — caption: "Nikolai Bukharin — revolutionary, theoretician, editor of Pravda. Confessed to treason he did not commit. Executed, 1938." Small portrait placed alongside trial paragraphs. |
| 3.14 | Moscow trial paragraphs | `Moscow, 1936. Stalin's prosecutors put a group of Old Bolsheviks on trial. These men — Kamenev, Zinoviev, Bukharin — had fought alongside Lenin. They had built the Soviet state. The charge was treason.` / `They confessed. In open court, in front of foreign journalists, they declared themselves enemies of the people. Some had been tortured. But Bukharin's confession was different. He spoke at length, with apparent conviction. Arthur Koestler tried to explain it in Darkness at Noon: if you have spent your entire life believing that the Party is the instrument of history, then admitting the Party is wrong means your life was pointless. Confession — even false confession — is the last way to remain loyal.` |
| 3.15 | **Trial list table** | Five rows, each with name / role / verdict: `Lev Kamenev` · `Politburo member, revolutionary` · `Confessed → Executed`; `Grigory Zinoviev` · `Comintern chairman` · `Confessed → Executed`; `Nikolai Bukharin` · `Party theoretician, Pravda editor` · `Confessed → Executed`; `Alexei Rykov` · `Chairman of the Council` · `Confessed → Executed`; `Karl Radek` · `Revolutionary journalist` · `Confessed → Imprisoned → Died`. |
| 3.16 | Synthesis paragraph | `The Party secretary who lied about the harvest and the Old Bolshevik who confessed to a crime he did not commit are doing the same thing. They are protecting the belief at the cost of everything else. The system is sealed. Information that contradicts the belief cannot enter.` |
| 3.17 | Hoffer blockquote | `"Mass movements can rise and spread without belief in a God, but never without belief in a devil."` — cite: `— Eric Hoffer, The True Believer, 1951` |

---

## SECTION 4 — Transition to Takeaway

A dedicated scrollytelling zone where the entire viewport background scroll-scrubs from black (#0A0A0A) to white (#FFFFFF). Text color cross-fades simultaneously. No prose — pure visual transition into the Takeaway section.

---

## SECTION 5 — Takeaway: When the Cages Held — **SHORTENED & MADE INTERACTIVE (v4)**

Section inverts to a bright white background (#FFFFFF) with pure black text. All typography stays sans-serif Inter. The accent color becomes #111 for blockquote border instead of red.

**v4 design principle:** This section must NOT feel like an article. Paragraphs are cut to 2–3 sentences max. Each element gets its own scroll step. The three counter-examples are the interactive content; the framing text is minimal connective tissue.

| # | Element | Content |
|---|---------|---------|
| 5.1 | Section label | `Takeaway` |
| 5.2 | Opening paragraphs | `If you have read this far, you might be thinking: we need better leaders.` / `That thought is the trap.` |
| 5.3 | Founders blockquote | `The founders of the American republic did not design for angels. They designed for men who would inevitably become corrupt, cowardly, or deluded — and they tried to build a system that could survive them anyway.` |
| 5.4 | Auxiliary precautions intro | `Madison called them "auxiliary precautions":` |
| 5.5 | Principle 1 | Scroll-triggered reveal: `**Separation of powers.** No single person holds enough authority to act alone.` |
| 5.6 | Principle 2 | Scroll-triggered reveal: `**Term limits and succession rules.** Written in advance, enforced without exception. The leader leaves. The system stays.` |
| 5.7 | Principle 3 | Scroll-triggered reveal: `**Independent press and judiciary.** Their job is to say no.` |
| 5.8 | "Boring is why it works" | `Nobody rallies for judicial independence. You cannot build a mass movement around the separation of powers. These things are boring. That is why they work.` / `But do they? Everything above is a story of cages that failed. Three times in the twentieth century, the cages held.` |

### Counter-example 1 — De Gaulle, 1969

| # | Element | Content |
|---|---------|---------|
| 5.9 | Image | `takeaway-degaulle-portrait.jpeg` — alt: "Charles de Gaulle" — caption: "Charles de Gaulle, founder of the Fifth Republic." |
| 5.10 | De Gaulle paragraphs | `Charles de Gaulle liberated France, founded the Fifth Republic, and wrote a constitution that concentrated executive power in the presidency — around himself. By any definition, a charismatic leader who had reshaped his country's institutions in his own image.` Between the two paragraphs, image `takeaway-degaulle-speech.jpg` (alt: "Charles de Gaulle addressing journalists at a press conference"; caption: "De Gaulle in office."). / `In April 1969, de Gaulle put a package of constitutional reforms to a national referendum. He announced that if the vote failed, he would resign. The same kind of gamble Hitler had made in 1933, staking everything on a single vote.` After the second paragraph, image `takeaway-degaulle-voting.jpg` (alt: "Charles de Gaulle casting his vote in the 1969 referendum"; caption: "De Gaulle casts his own vote, April 27, 1969."). |
| 5.11 | **Referendum result bar** | Interactive horizontal bar chart, scroll-triggered. A single bar expands from center: left side blue `52.41% Non`, right side red `47.59% Oui`. Numbers count up as bar fills. Visual mirror of the hemicycle 441/94 — but this time, the vote constrains the leader instead of enabling him. |
| 5.11a | Image | `takeaway-degaulle-referendum.jpeg` — alt: "Newspaper headlines reporting the results of the 1969 French referendum" — caption: `The morning after: a 'Non' the founder of the Republic chose to honor.` |
| 5.12 | De Gaulle resolution | `The French voted Non. De Gaulle resigned the next day. No tanks, no emergency powers, no attempt to circumvent the result. The man who had built the cage walked into it and closed the door behind him.` |
| 5.13 | Image | `takeaway-degaulle-retirement.jpg` — alt: "Charles de Gaulle walking on a beach after his resignation" — caption: "Colombey-les-Deux-Églises, 1969. The day after." |

### Counter-example 2 — FDR, 1937

| # | Element | Content |
|---|---------|---------|
| 5.14 | Image | `takeaway-fdr-portrait.jpg` — alt: "Franklin D. Roosevelt" — caption: "Franklin D. Roosevelt, 32nd President of the United States." |
| 5.15 | FDR paragraph | `Roosevelt won the 1936 election with 61% of the vote — the largest mandate since Monroe ran unopposed — and carried 46 of 48 states. When the Supreme Court kept striking down his New Deal legislation, he proposed packing the bench: adding up to six new justices. His own party killed the bill. The Senate voted 70 to 22 against their own president — because the institutional principle mattered more than the political alliance. Roosevelt remained president. The Court stayed at nine.` |
| 5.16 | Image | `takeaway-fdr-supreme-court-1937.png` — alt: "The nine justices of the U.S. Supreme Court, 1937" — caption: "The Hughes Court, 1937. Nine seats. Roosevelt wanted fifteen. The Senate said no." |

### Counter-example 3 — Mandela, 1999

| # | Element | Content |
|---|---------|---------|
| 5.17 | Image | `takeaway-mandela-salute.jpg` — alt: "Nelson Mandela saluting a crowd" — caption: "Nelson Mandela, Galeshewe, South Africa." |
| 5.18 | Mandela paragraph | `Mandela spent twenty-seven years in prison. He won South Africa's first democratic election in 1994 with 62% of the vote. His moral authority was absolute. He served one term and stepped down. De Gaulle was constrained by a vote. Roosevelt was constrained by the Senate. Mandela was constrained by nothing except his own judgment.` |
| 5.19 | Image | `takeaway-mandela-portrait.jpg` — alt: "Portrait of Nelson Mandela" — caption: "The institution did not constrain him. He constrained himself. That is the exception, not the rule." |

### Synthesis

| # | Element | Content |
|---|---------|---------|
| 5.20 | **Three-column comparison table** | Scroll-triggered fade-in. Three cards side by side, each with identical structure. Header row: `Leader` / `Pressure Moment` / `What Held` / `Outcome`. Card 1: `De Gaulle` / `1969 referendum` / `The vote` / `Resigned. Republic continued.` Card 2: `Roosevelt` / `Court-packing, 1937` / `The Senate (his own party)` / `Bill killed 70–22. Court stayed at nine.` Card 3: `Mandela` / `Presidency, 1999` / `His own restraint` / `Stepped down. But — would the next leader?` The third card's "What Held" cell has a subtle question-mark pulse, visually distinct from the first two. |
| 5.21 | Synthesis paragraphs | `Weber's third path — charisma constrained by institutions — held three times. But Mandela's case is the fragile one. His restraint came from character, not from design.` / `The cages do not hold by themselves. They hold because someone decides they matter more than the leader standing in front of them.` |

Visual instruction for engineering: at this point in the Takeaway, the **routinization pathway diagram** from Section 1.11 should be recalled or echoed — Path C (`Constrained by Institutions`) illuminates fully, its `?` replaced by three labels: `De Gaulle / FDR / Mandela`. Mandela's label retains the subtle pulse, acknowledging the ambiguity.

---

## SECTION 6 — Closing

A short all-white section. Two elements revealed **word-by-word** as the user scrolls past them (each word fades in independently, left to right):

First, the Herbert quote:

> `"The bottom line of the Dune trilogy is: beware of heroes. Much better rely on your own judgment, and your own mistakes."`
>
> — cite: `— Frank Herbert, 1979`

Then, after a pause of whitespace, the final line:

> `The cages will not remind you they matter. That is something you have to remember on your own.`

---

## SECTION 7 — References

Heading: `References`.

**Primary sources and speeches:**

1. Frank Herbert, Speech at UCLA, April 17, 1985. Transcript: The Augustry (theaugustry.com). Audio: UCLA Campus Events Commission archives.
2. Frank Herbert, "Dune Genesis," *Omni*, July 1980. Source of "beware of heroes" and "the bottom line of the Dune trilogy" statement.
3. James Madison, *Federalist No. 51* (1788). "If men were angels, no government would be necessary."
4. Max Weber, *Economy and Society* (Wirtschaft und Gesellschaft), ed. Guenther Roth and Claus Wittich, University of California Press, 1978 (original German publication 1922). Definition of charismatic authority: Part I, Chapter III, §10.
5. Leon Festinger, Henry Riecken, and Stanley Schachter, *When Prophecy Fails*, University of Minnesota Press, 1956. Festinger quote ("A man with a conviction…") from Leon Festinger, *A Theory of Cognitive Dissonance*, Stanford University Press, 1957, p. 3.
6. Eric Hoffer, *The True Believer: Thoughts on the Nature of Mass Movements*, Harper & Brothers, 1951. "Mass movements can rise and spread without belief in a God…": Part III, §65.
7. Arthur Koestler, *Darkness at Noon*, Macmillan, 1940.
8. Eli Pariser, *The Filter Bubble: What the Internet Is Hiding from You*, Penguin Press, 2011.
9. Cass Sunstein, *Going to Extremes: How Like Minds Unite and Divide*, Oxford University Press, 2009.

**Historical sources — Section 1 (Reichstag / Cultural Revolution):**

10. Richard J. Evans, *The Coming of the Third Reich*, Penguin, 2005. Enabling Act vote count (441 to 94): Chapter 8, pp. 351–374.
11. Ian Kershaw, *Hitler: 1889–1936 — Hubris*, W.W. Norton, 1998. Reichstag context: Chapter 10.
12. Otto Wels, Speech to the Reichstag, March 23, 1933. "You can take our liberty and our lives…": reprinted in Evans (2005) and in the Reichstag Protocols (Verhandlungen des Reichstags), Vol. 457, p. 34.
13. Roderick MacFarquhar and Michael Schoenhals, *Mao's Last Revolution*, Harvard University Press, 2006. Cultural Revolution death toll estimate (500,000–2,000,000): Chapter 14 and Epilogue. "36 million persecuted" figure: pp. 262–263.
14. Frank Dikötter, *The Cultural Revolution: A People's History, 1962–1976*, Bloomsbury, 2016. Corroborating death toll estimates and provincial violence.
15. Mao Zedong, "Bombard the Headquarters — My First Big-Character Poster," August 5, 1966. Reprinted in Stuart Schram, ed., *Mao Tse-Tung Unrehearsed*, Penguin, 1974.

**Historical sources — Section 2 (Lenin/Stalin, Islamic schism):**

16. Robert Service, *Lenin: A Biography*, Macmillan, 2000. Lenin's Testament: Chapter 33, pp. 466–475.
17. Lenin's Testament (Letter to the Congress), January 4, 1923. Published in *Kommunist* No. 9, 1956, following Khrushchev's Secret Speech. English translation in Robert C. Tucker, ed., *The Lenin Anthology*, W.W. Norton, 1975, pp. 725–728.
18. Stephen Kotkin, *Stalin: Paradoxes of Power, 1878–1928*, Penguin, 2014. Stalin's outmaneuvering of rivals: Chapters 11–14.
19. David King, *The Commissar Vanishes: The Falsification of Photographs and Art in Stalin's Russia*, Metropolitan Books, 1997. Source for both before/after photograph pairs (Lenin at Sverdlov Square; Stalin with Yezhov at the Moscow Canal).
20. Robert Conquest, *The Great Terror: A Reassessment*, Oxford University Press, 2008 (orig. 1968). Great Purge execution and gulag statistics: Chapters 8–13 and statistical appendix.
21. Oleg Khlevniuk, *The History of the Gulag*, Yale University Press, 2004. Corroborating gulag population numbers.
22. Fred M. Donner, *Muhammad and the Believers: At the Origins of Islam*, Harvard University Press, 2010. Succession crisis and early caliphate: Chapters 4–6.
23. Wilferd Madelung, *The Succession to Muhammad: A Study of the Early Caliphate*, Cambridge University Press, 1997. Ghadir Khumm and the Abu Bakr/Ali dispute.
24. Hugh Kennedy, *The Prophet and the Age of the Caliphates*, Longman, 2004. Assassination of early caliphs and Karbala.
25. Heinz Halm, *Shi'ism*, Edinburgh University Press, 2004. Ashura, Twelver/Ismaili/Zaidi branches.

**Historical sources — Section 2 (Sectarian conflict death tolls):**

26. Iran-Iraq War (~1,000,000 dead): Pierre Razoux, *The Iran-Iraq War*, Harvard University Press, 2015. Also: Lawrence G. Potter and Gary G. Sick, eds., *Iran, Iraq, and the Legacies of War*, Palgrave, 2004.
27. Iraq Civil War (~200,000 dead): Iraq Body Count project (iraqbodycount.org); also *The Lancet* survey estimates (Gilbert Burnham et al., "Mortality after the 2003 invasion of Iraq," *The Lancet* 368, no. 9545, 2006).
28. Syrian Civil War (~500,000 dead): United Nations Office of the High Commissioner for Human Rights estimates, 2021; Syrian Observatory for Human Rights data through 2024.
29. Yemen Civil War (~150,000+ dead): Armed Conflict Location and Event Data Project (ACLED), 2019 report; United Nations Office for the Coordination of Humanitarian Affairs (OCHA).

**Historical sources — Section 3 (Great Leap Forward, Moscow Trials):**

30. Frank Dikötter, *Mao's Great Famine: The History of China's Most Devastating Catastrophe, 1958–1962*, Bloomsbury, 2010. Death toll estimates (15–55 million, scholarly range): Chapter 37 and statistical appendix. Harvest inflation and Henan case studies: Chapters 5–8.
31. Yang Jisheng, *Tombstone: The Great Chinese Famine, 1958–1962*, Farrar, Straus and Giroux, 2012. Corroborating famine death toll and bureaucratic falsification of harvest numbers.
32. Peng Dehuai, "Letter of Opinion" (万言书), Lushan Conference, July 14, 1959. Discussed in Roderick MacFarquhar, *The Origins of the Cultural Revolution, Vol. 2: The Great Leap Forward, 1958–1960*, Columbia University Press, 1983, pp. 203–222.
33. Robert Conquest, *The Great Terror* (2008). Moscow Show Trials — Kamenev, Zinoviev (Trial of the Sixteen, 1936), Bukharin, Rykov, Radek (Trial of the Twenty-One, 1938): Part Two.
34. Stephen F. Cohen, *Bukharin and the Bolshevik Revolution*, Oxford University Press, 1980. Bukharin's confession: Chapter 12.

**Historical sources — Takeaway (De Gaulle, FDR, Mandela):**

35. Julian Jackson, *De Gaulle*, Harvard University Press, 2018. 1969 referendum result (52.41% Non, 47.59% Oui): Chapter 27, pp. 735–741. Also: Serge Berstein, *The Republic of de Gaulle, 1958–1969*, Cambridge University Press, 1993.
36. Official results: French Constitutional Council, Proclamation of Referendum Results, April 28, 1969.
37. Jeff Shesol, *Supreme Power: Franklin Roosevelt vs. the Supreme Court*, W.W. Norton, 2010. Court-packing bill defeated 70–22 in the Senate Judiciary Committee: Chapters 20–22.
38. William E. Leuchtenburg, *The Supreme Court Reborn: The Constitutional Revolution in the Age of Roosevelt*, Oxford University Press, 1995. 1936 election (61%, 46 of 48 states): Chapter 4.
39. Nelson Mandela, *Long Walk to Freedom*, Little, Brown, 1994.
40. Tom Lodge, *Mandela: A Critical Life*, Oxford University Press, 2006. 1994 election (62.65% of the vote): Chapter 14. Decision not to seek second term.

**Additional references:**

41. Jonathan Haidt, *The Righteous Mind: Why Good People Are Divided by Politics and Religion*, Vintage Books, 2012.
42. Vietnam War U.S. military deaths (58,220): National Archives, Department of Defense records. Also: *Statistical Information about Fatal Casualties of the Vietnam War*, National Archives (archives.gov).
43. Frank Herbert, Introduction to *Eye* (short story collection), Berkley Books, 1985. "The mistakes made by a leader (or made in a leader's name) are amplified by the numbers who follow without question."

---

## Appendix A — Complete asset list

All images are in `/assets/`. Grayscale filter applied globally (~80%) unless noted.

| Filename | Used in | Alt text / description |
|----------|---------|------------------------|
| `opening-JFK-Nixon-debate.jpg` | Hero Phase 3 background | John F. Kennedy and Richard Nixon at their first televised presidential debate, Chicago, 1960. |
| `opening-frankherbert.jpg` | Hero Phase 1, centered large portrait | Portrait of Frank Herbert. |
| `s1-weber-portrait-1918.jpg` | S1 Theory — enlarged | Max Weber, 1918. |
| `s1-hitler-reichstag.jpg` | S1 Part II, step 0 | Hitler at the Kroll Opera House, March 1933. |
| `s1-otto-wels-portrait.jpg` | S1 Part II, step 3 | Otto Wels, SPD chairman, 1933. |
| `s1-cultural-revolution.jpg` | S1 Part III, step 0 | Red Guards rally in Beijing, 1966. |
| `s1-mao-tiananmen.jpg` | S1 Part III, step 0 (second image) | Mao reviews the Red Guards from Tiananmen Gate, August 1966. |
| `s1-anti-liu-shaoqi-poster.jpg` | S1 Part III, step 2 | Anti-Liu Shaoqi propaganda during the Cultural Revolution. |
| `s1-peng-dehuai-military-portrait.jpg` | S3 Part 1, Peng Dehuai scroll step 1 | Peng Dehuai in military uniform before persecution. |
| `s1-peng-dehuai-struggle-session.jpg` | S3 Part 1, Peng Dehuai scroll step 4 | Marshal Peng Dehuai subjected to a struggle session by Red Guards. |
| `s1-weber-oratory.png` | S1 Part I, after the Weber blockquote | Weber-era oratory illustration: a crowd listening to a charismatic orator. |
| `s2-lenin-last-photo-1923.jpg` | S2 Case A | Vladimir Lenin in wheelchair at Gorki, 1923, last known photograph. |
| `s2-lenin-testament-manuscript.jpg` | S2 Case A, interactive | Typewritten page of Lenin's Testament addition, January 4, 1923. |
| `s2-lenin-stalin.jpg` | S2 Case A | Lenin and Stalin at Gorki, 1922. |
| `s2-stalin-propaganda-1.jpg` | S2 Case A | Soviet propaganda poster, 1933 ("With the banner of Lenin..."). |
| `s2-stalin-propaganda-2.jpg` | S2 Case A, between purge grid and gulag | Soviet poster pairing Stalin with Lenin's image. |
| `s2-lenin-original.jpg` | S2 before/after slider #1 — ORIGINAL | Lenin speaking at Sverdlov Square, 1920, with Trotsky and Kamenev beside the podium. |
| `s2-lenin-removed.jpg` | S2 before/after slider #1 — RETOUCHED | Same photograph, Trotsky and Kamenev erased. |
| `s2-stalin-original.jpg` | S2 before/after slider #2 — ORIGINAL | Stalin walking with Nikolai Yezhov along the Moscow-Volga Canal. |
| `s2-stalin-removed.jpg` | S2 before/after slider #2 — RETOUCHED | Same photograph, Yezhov erased. |
| `s2-gulag-workers.jpg` | S2 Case A | Gulag prisoners building the White Sea–Baltic Canal. |
| `s2-muhammad.jpg` | S2 Case B | Conceptual artistic portrait of the Prophet Muhammad. |
| `s2-karbala-battle.jpg` | S2 Case B, full-bleed | The Battle of Karbala, 680 CE — visceral oil painting (replaces old `s2-karbala.webp`). |
| `s2-ashura.jpeg` | S2 Case B | Ashura commemoration. |
| `s2-syria-aleppo-destruction.jpg` | S2 Case B, between tree and counter | Destroyed buildings in Aleppo, Syria. |
| `s3-great-leap-forward-furnaces.jpg` | S3 opening | Backyard steel furnaces during China's Great Leap Forward. |
| `s3-great-famine-victims.jpg` | S3, after inflate scrolly | Family during the Great Chinese Famine, 1959–1961. |
| `s3-bukharin-portrait.jpg` | S3 Confession | Nikolai Bukharin, Party theoretician, before arrest. |
| `s3-moscow-trial.jpg` | S3 Confession | Moscow Show Trials courtroom, 1936–1938. |
| `takeaway-degaulle-portrait.jpeg` | Takeaway, counter-example 1 | Charles de Gaulle. |
| `takeaway-degaulle-speech.jpg` | Takeaway, counter-example 1 | De Gaulle at a press conference. |
| `takeaway-degaulle-referendum.jpeg` | Takeaway, counter-example 1 | Newspaper headlines reporting the 1969 referendum result. |
| `takeaway-degaulle-voting.jpg` | Takeaway, counter-example 1 | De Gaulle voting. |
| `takeaway-degaulle-retirement.jpg` | Takeaway, counter-example 1 | De Gaulle walking on a beach after resignation. |
| `takeaway-fdr-portrait.jpg` | Takeaway, counter-example 2 | Franklin D. Roosevelt. |
| `takeaway-fdr-supreme-court-1937.png` | Takeaway, counter-example 2 | The nine justices of the U.S. Supreme Court, 1937. |
| `takeaway-mandela-salute.jpg` | Takeaway, counter-example 3 | Nelson Mandela saluting a crowd in Galeshewe. |
| `takeaway-mandela-portrait.jpg` | Takeaway, counter-example 3 | Portrait of Nelson Mandela. |

**NEW assets added in v4:**

| Filename | Used in | Description |
|----------|---------|-------------|
| `opening-paul-atreides.png` | Hero B6a | Film still of Timothée Chalamet as Paul Atreides in Dune (2021). |
| `s1-nuremberg-rally-1934.jpg` | S1 1.2a | Bundesarchiv — SA/SS formations at the 1934 Nuremberg Rally. Replaces `s1-charismatic-leadership.jpg`. |
| `s1-cr-rebellion-poster-1967.jpg` | S1 Part III, Step 1 | Cultural Revolution woodcut poster, 1967 — "Revolution is innocent, rebellion is justified." |
| `s1-cr-beijing-university-rally-1966.jpg` | S1 Part III (spare) | Red Guard rally at Beijing University, September 1966. |
| `s1-cr-struggle-session.jpg` | S1 Part III (spare) | Public struggle session during the Cultural Revolution. |
| `s1-cr-execution.jpg` | S1 Part III (spare) | Execution during the revolutionary period. |
| `s1-cr-pla-revolutionary-committee.jpg` | S1 Part III, Step 3 | PLA troops massed with rifles and red flags at Beijing Revolutionary Committee rally. |
| `s3-mao-lushan-conference-1959.jpeg` | S3 Peng Dehuai Step 3 | Mao Zedong at the Lushan Conference, 1959. |
| `s2-karbala-battle.jpg` | S2 Case B, 2B.6 | Visceral oil painting of the Battle of Karbala. Replaces `s2-karbala.webp`. |

**Deprecated assets (kept in /assets/ but no longer referenced):**

| Filename | Reason |
|----------|--------|
| `s1-charismatic-leadership.jpg` | Replaced by `s1-nuremberg-rally-1934.jpg` — wrong tone (comic-style). |
| `s2-karbala.webp` | Replaced by `s2-karbala-battle.jpg` — too blurry, no visual impact. |

---

## Appendix B — De-AI rewrite rules

All prose in this document must pass through a de-AI rewrite before being considered final. The following rules apply:

**What to eliminate:**

- Empty openers and closers ("Certainly!", "I'd be happy to help", "Hope this helps!")
- Hollow rhetorical structures: "Not X, but Y" / "Both X and Y" balance sentences / "Precisely because X, therefore Y" — say the causal relationship directly
- Inflated adjectives: comprehensive, robust, seamless, powerful, nuanced, multifaceted, transformative, dynamic, holistic, innovative — replace with specific description or delete
- Fake empathy phrases ("I understand this may be frustrating...")
- Filler transitions: "It's worth noting that..." / "Importantly..." / "In conclusion" — cut or integrate naturally
- The fake-depth sentence pattern: "A is not B, but A is a C that does D" / "While A lacks X, it represents Y" — flatten into a direct claim

**What to keep and aim for:**

- Specific over general
- Short declarative sentences: say the thing, then stop
- Asymmetry is fine: not every point needs a counterpoint
- Opinions are fine: don't hedge everything into mush
- Abrupt endings are fine: don't wrap up with a bow

**Rewrite rules:**

1. Preserve all factual content and meaning
2. Match the original language (Chinese stays Chinese, English stays English)
3. Do not add new content or commentary
4. If a sentence is hollow after stripping the structure, delete it
5. Do not explain what you changed — just output the rewritten text
