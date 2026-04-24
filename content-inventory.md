# The Dark Side of Charismatic Leadership — Complete Content Inventory

A linear, top-to-bottom inventory of every element on the page: text, images, quotes, data visualizations, interactive modules, and all their possible states.

Page metadata — Title: `The Dark Side of Charismatic Leadership`. Meta description: `How charismatic leaders dismantle institutions, how movements outlive their founders, and how followers seal themselves inside belief.` Font: Inter (Google Fonts). Theme: dark (#0A0A0A background, #A0A0A0 body text, #F5F5F5 headings, #C0392B accent red). The Takeaway section inverts to a white background with black text.

---

## Global / persistent elements

| # | Element | Type | Content / behavior |
|---|---------|------|--------------------|
| G1 | Progress navigation | Fixed sticky dots, right edge | Five vertical dots labeled `Introduction`, `When Charisma Meets Power`, `The Movement Outlives the Leader`, `Followers Are Self-Sealing`, `Takeaway`. The dot for the current section is highlighted red. Clicking any dot smooth-scrolls to that section. |
| G2 | No-JS fallback | Safety | If JavaScript is disabled, all scroll-triggered fade-ins become immediately visible so the page remains readable as static prose. |

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

Background image with overlaid text. JFK/Nixon debate image fills the background at 15% opacity, grayscale.

| # | Element | Type | Content |
|---|---------|------|---------|
| B1 | Background image | `opening-JFK-Nixon-debate.jpg` | Alt: "John F. Kennedy and Richard Nixon at their first televised presidential debate, Chicago, 1960." |
| B2 | Herbert portrait | `opening-frankherbert.jpg` | Small grayscale portrait pinned top-right at 60% opacity. Alt: "Portrait of Frank Herbert." Hidden on mobile. |
| B3 | Hero quote | Italic pull-quote | `"I wrote the Dune series because I had this idea that charismatic leaders ought to come with a warning label on their forehead: 'May be dangerous to your health.'"` — cite: `— Frank Herbert, UCLA, 1985`. |
| B4 | Title | `<h1>` | `The Dark Side of Charismatic Leadership` (two lines). |
| B5 | Body paragraph 1 | Prose | `Seventy million Americans watched that debate. The ones who listened on radio thought Richard Nixon won. The ones who watched on television were certain it was John F. Kennedy. Same debate, same words. The only difference was the screen.` |
| B6 | Body paragraph 2 | Prose | `Frank Herbert watched a science fiction audience fall in love with Paul Atreides — the hero of `Dune` — and it horrified him. He had written Paul as a warning. Readers took him as a savior. So Herbert wrote sequel after sequel to make the point as brutal as possible: the hero will destroy you. Not because he wants to. Because you will let him.` |
| B7 | Body paragraph 3 | Prose | `This website is about what happens when people stop questioning. How institutions collapse. How movements outlive the people who started them. How followers seal themselves inside a belief until nothing can reach them.` |

---

## SECTION 1 — When Charisma Meets Power

### Part I — The Theory

| # | Element | Type | Content |
|---|---------|------|---------|
| 1.1 | Section label | Red small-caps | `Section 1` |
| 1.2 | Section title | `<h2>` | `When Charisma Meets Power` |
| 1.3 | Part label | `<h3>` | `Part I — The Theory` |
| 1.4 | Weber intro paragraph | Prose | `In 1922, Max Weber identified three sources of political authority: tradition, law, and charisma. The first two are stable — they survive the death of any individual. Charisma does not. It lives in one person, and it demands total faith in that person.` |
| 1.5 | **Weber three-authority animated bars** | Interactive visualization | Three equal-height vertical bars labeled **Tradition**, **Law**, **Charisma**. On load, all three are dark gray except Charisma, which is red and pulses with a glowing halo. When the bars scroll into view: Charisma expands to ~2× height and Tradition + Law collapse to stubs with a diagonal striped "broken" texture overlaid — visually Charisma crushes the other two. |
| 1.6 | Weber pull-quote | Blockquote | `"A certain quality of an individual personality by virtue of which he is set apart from ordinary men and treated as endowed with supernatural, superhuman, or at least specifically exceptional powers."` — cite: `— Max Weber, Economy and Society, 1922` |
| 1.7 | Madison paragraph | Prose | `Institutions — legislatures, courts, free presses — exist because the system expects leaders to be flawed. Madison put it plainly in Federalist No. 51: "If men were angels, no government would be necessary." Every check, every balance, every procedural delay is built on that assumption.` |
| 1.8 | Charisma-breaks-assumption paragraph | Prose | `Charisma breaks the assumption. When followers believe a leader is exceptional, the checks start looking like obstacles. The followers want them gone. And the leader, surrounded by devotion, starts to agree.` |

### Part II — The Enabling (sticky scrollytelling — Reichstag vote)

Part label: `Part II — The Enabling`.

Left half of viewport: **hemicycle parliament visualization**. A dot-graphic of ~535 seats arranged in a half-circle (the Reichstag). All seats start dark gray.

Right half: four narrative "steps" that the user scrolls through. As the user scrolls, seats fill continuously with red from the right side inward.

| Step | Narrative content | Hemicycle state |
|------|-------------------|-----------------|
| Step 0 | Image `s1-hitler-reichstag.jpg` (alt: "Hitler at the Kroll Opera House, March 1933"; caption: "The Kroll Opera House, Berlin, March 1933"). Then paragraphs: `Berlin, March 23, 1933. The Kroll Opera House, draped in swastika banners. Hitler stands before the Reichstag and asks for the legal authority to rule by decree.` and `The Enabling Act would let him bypass parliament, bypass the constitution, bypass every safeguard the Weimar Republic had built. A democracy would become a dictatorship — through a vote.` | All seats dark gray. |
| Step 1 | `**The Nazi Party holds 288 seats.** They don't have a two-thirds majority alone. But the SA stormtroopers stand outside the building. The Communist Party's 81 deputies have already been arrested or barred from attending.` | Seats fill red progressively from the right, reaching 288 red Nazi seats. |
| Step 2 | `**The Centre Party caves.** Hitler promises to respect the Church. The promise is worthless, but the Centre's leader, Ludwig Kaas, tells his caucus to vote yes. One by one, the smaller parties fall in line. The pressure of the crowd, the SA outside, the momentum — resistance feels pointless.` | Red continues extending leftward, reaching 441 red seats. |
| Step 3 | `**Only the Social Democrats hold.** 94 votes against, in a room full of men who have already surrendered. Otto Wels, the SPD leader, stands to speak: "You can take our liberty and our lives, but you cannot take our honor."` followed by `No tanks. No gunfire. The institutions of German democracy were not destroyed by force. Elected officials handed them over, to a man whose crowds made resistance feel pointless.` | 441 seats locked red (Nazis + allies), the remaining 94 SPD seats switch to dim gray. Count display fades in showing `441 IN FAVOR` / `94 AGAINST`. |

### Part III — The Fire (sticky scrollytelling — Cultural Revolution)

Part label: `Part III — The Fire`.

Left half: **Cultural Revolution timeline visualization**. A giant year number (120px), an event description below, a horizontal red intensity bar that grows 0→100%, and a death-toll line that appears at the end.

| Step | Narrative content | Visualization state |
|------|-------------------|---------------------|
| Step 0 | Image `s1-cultural-revolution.jpg` (alt: "Red Guards rally in Beijing, 1966"; caption: "Red Guards rally, Beijing, 1966"). Paragraphs: `Beijing, May 1966. Mao Zedong is 72. He has led the People's Republic for seventeen years, but his grip on the Party is slipping. Rivals in the Politburo are quietly sidelining him.` and `So Mao goes around them. He bypasses his own party, his own government, his own chain of command. He writes a big-character poster — "Bombard the Headquarters" — and calls on China's students to attack the system he built.` | Year `1966`, intensity bar empty. |
| Step 1 | `Mao mobilizes millions of Red Guards. They flood the streets, drag professors from classrooms, beat officials in public, destroy temples, burn books. The chaos is total. The loyalty is absolute.` | Year `1966`, event `Mao mobilizes Red Guards`, intensity 25%. |
| Step 2 | `Red Guard factions turn on each other. Provincial governments collapse. Liu Shaoqi — the second most powerful man in China — is dragged from his home and left to die in detention. The revolution is eating its own.` | Year `1967`, event `Factions turn on each other. Governments collapse.`, intensity 55%. |
| Step 3 | `Even Mao cannot stop it. He sends the army to suppress the Red Guards — the very forces he summoned two years earlier. The weapon he built no longer answers to him.` | Year `1968`, event `Army deployed to suppress Red Guards`, intensity 80%. (Then `1969` / `Violence continues in provinces` / 65% as a decay state.) |
| Step 4 | `The Cultural Revolution officially ends. The toll: an estimated 500,000 to 2 million dead, up to 36 million persecuted.` then blockquote `"To rebel is justified — bombard the headquarters!"` cite `— Mao Zedong, 1966`. Then paragraph: `Hitler got the institutions out of his way. Mao went further — he unleashed a force that got out of *his* way. The pattern keeps repeating. A leader rises above the system. The system yields. Then the leader discovers that the thing he unleashed does not answer to him either.` | Year `1976`, event `Cultural Revolution ends`, intensity 100%, death toll `500,000 – 2,000,000 dead` appears. |

---

## SECTION 2 — The Movement Outlives the Leader

### Case A — Lenin → Stalin

| # | Element | Content |
|---|---------|---------|
| 2A.1 | Section label | `Section 2` |
| 2A.2 | Section title | `The Movement Outlives the Leader` |
| 2A.3 | Case label | `Case A — Lenin → Stalin` |
| 2A.4 | Image | `s2-lenin-stalin.jpg` — alt: "Lenin and Stalin at Gorki, 1922" — caption: "Lenin and Stalin, Gorki, 1922". |
| 2A.5 | Testament paragraphs | `Vladimir Lenin died on January 21, 1924. He had spent his final months writing a document that the Party would later call his "Testament." In it, he warned that Stalin was "too rude" and should be removed from the position of General Secretary. He proposed replacing him with someone "more patient, more loyal, more polite."` / `The Testament was read aloud at the 13th Party Congress. The delegates listened, discussed it briefly, and did nothing.` |
| 2A.6 | Image | `s2-stalin-propaganda-1.jpg` — alt: "Soviet propaganda poster, 1933" — caption: `"With the banner of Lenin..." — Soviet propaganda, 1933`. |
| 2A.7 | Stalin consolidation paragraphs | `Stalin kept his position. Within five years, he had outmaneuvered every rival. He renamed Petrograd — the city where the revolution began — to Leningrad. He turned Lenin's body into a public relic, preserved in a glass case on Red Square for pilgrims to visit. He wrapped every policy in Lenin's language, every purge in Lenin's authority. The dead man could not object.` / `By the mid-1930s, Stalin had built something Lenin never intended: a totalitarian state where disagreement was a death sentence. The Great Purge of 1936–1938 executed or imprisoned hundreds of thousands — party members, military officers, intellectuals, anyone who might one day challenge Stalin's reading of what Lenin "really meant."` |
| 2A.8 | Erasure intro | Italic line: `Execution was not enough. The Party rewrote the visual record, erasing rivals from official photographs. Drag the slider to see what was removed.` |
| 2A.9 | **Before/after slider #1 — Lenin / Trotsky** | Interactive drag-slider. Original photograph (`s2-lenin-origianl.jpg`, alt: "Lenin speaking at Sverdlov Square, 1920, with Trotsky and Kamenev beside the podium") on the left; retouched photograph (`s2-lenin_removed.jpg`, alt: "The same photograph after Stalin-era retouching, with Trotsky and Kamenev erased") on the right. A red vertical divider with a white-bordered circular red handle marked `⇆` can be dragged left and right. Labels below: `Original (1920)` / `Retouched`. Caption: `Lenin at Sverdlov Square, 1920. Trotsky and Kamenev stood beside the podium — until they didn't.` |
| 2A.10 | **Before/after slider #2 — Stalin / Yezhov** | Same component. Original (`s2_stalin_original.jpg`, alt: "Stalin walking with Nikolai Yezhov along the Moscow-Volga Canal") / retouched (`s2_stalin_removed.jpg`, alt: "The same photograph after Yezhov's execution, with Yezhov erased"). Labels: `Original` / `After Yezhov's execution`. Caption: `Stalin and secret police chief Nikolai Yezhov at the Moscow Canal. After Yezhov was shot in 1940, he vanished from the photograph too.` |
| 2A.11 | **Purge statistics counter** | Two large red numbers animating from 0 on entry: `Executed` (final value from JS: purgeExec target), `Sent to Gulag` (final value from JS: purgeGulag target). |
| 2A.12 | **Purge grid** | A dense grid of hundreds of tiny tombstone-shaped dots. On entry, dots progressively turn red (`executed`) and dark red (`gulag`) to visualize the scale of the purge victims. |
| 2A.13 | Image | `s2-gulag-workers.jpg` — alt: "Gulag prisoners building the White Sea-Baltic Canal" — caption: "Prisoners at Belbaltlag, building the White Sea–Baltic Canal". |
| 2A.14 | Closing paragraph | `Lenin's revolution was supposed to liberate the working class. Under Stalin, it became the justification for a system of forced labor camps stretching across Siberia. The ideology did not change. The words stayed the same. Only the meaning shifted — and there was no one left alive who was allowed to say so.` |
| 2A.15 | Lenin's Testament blockquote | `"Stalin is too rude... I propose to find a way to remove Stalin from that position and appoint to it another man who is more patient, more loyal, more polite."` — cite: `— Lenin's Testament, January 4, 1923` |

### Case B — Muhammad → The Fracture

| # | Element | Content |
|---|---------|---------|
| 2B.1 | Case label | `Case B — Muhammad → The Fracture` |
| 2B.2 | Image | `s2-muhammud.jpg` — alt: "The early Islamic world" — caption: "The early Islamic world". |
| 2B.3 | Succession paragraphs | `Muhammad died in Medina on June 8, 632 CE. He left behind a community of believers, a rapidly expanding territory, and no clear successor.` / `Within hours, the crisis began. One faction backed Abu Bakr, Muhammad's closest companion. Another insisted on Ali, his cousin and son-in-law — the man they believed Muhammad had designated at Ghadir Khumm. Both sides were certain. Neither side could ask the only person whose answer would have settled it.` |
| 2B.4 | Full-bleed image | `s2-karbala.webp` — alt: "The Battle of Karbala, 680 CE". Stretches edge-to-edge. |
| 2B.5 | Image caption line | Italic `The Battle of Karbala, 680 CE` |
| 2B.6 | Karbala paragraph | `Abu Bakr became the first caliph. Over the next three decades, three of the first four caliphs were assassinated. In 680 CE, Ali's son Husayn marched to Karbala to challenge the Umayyad caliph Yazid. His forces were massacred. That death became the founding trauma of Shia Islam — a grief re-enacted every year during Ashura, fourteen centuries later.` |
| 2B.7 | Image | `s2-abura.jpeg` — alt: "Ashura commemoration" — caption: "Ashura commemoration — mourning Husayn, 1400 years later". |
| 2B.8 | **Islamic schism branch tree (interactive SVG)** | A top-down family tree showing the fracture of Islam into branches. Hovering any node surfaces a tooltip with a title and explanation. Full node list below. |

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

Tree footer line: `1,850,000+ lives — from one succession crisis in 632 CE` (red).

### 2C — 632 → 2026 sticky death-toll counter

A full-viewport sticky scroll sequence (220vh tall) pinned while the user scrolls.

| # | Element | Behavior |
|---|---------|----------|
| 2C.1 | Year label (small) | `Year 632` at the top, counts upward in real time from 632 to 2026 as the user scrolls. |
| 2C.2 | **Huge red death toll** | Enormous red number at center, counting from `0` upward. Historical interpolation: roughly 10,000 by 680 (Karbala era), 80,000 by 750 (Umayyad civil wars), 120,000 by 1500, 150,000 by 1900/1980, jumps sharply to ~1,150,000 after the Iran-Iraq War (1988), 1,400,000 after the Iraq civil war (2011), 1,700,000 after the Syrian war (2014), and finishes at **1,850,000** at 2026. |
| 2C.3 | Sub-label | Italic `dead in Sunni–Shia sectarian conflict`. |

---

## SECTION 3 — Followers Are Self-Sealing

### Part 1 — The inflating number (sticky scrollytelling — Great Leap Forward)

| # | Element | Content |
|---|---------|---------|
| 3.1 | Section label | `Section 3` |
| 3.2 | Section title | `Followers Are Self-Sealing` |
| 3.3 | Image | `Great-Leap-Forward-China-Yingshuichiao-Iron-Smelting-works-1950s_副本.jpg` — alt: "Backyard steel furnaces during China's Great Leap Forward" — caption: "Backyard steel furnaces, China, late 1950s". |
| 3.4 | Henan paragraphs | `Somewhere in rural Henan province, 1959. A local Party secretary stands in a field. The wheat is thin. He knows the harvest will fall short — maybe thirty percent of last year. He also knows what happened to the last official who reported low numbers. The man was denounced as a rightist, stripped of his position, and sent to a labor camp. His family was not told where.` / `The secretary writes his report. Record yield. Twice the actual harvest. He sends it up the chain.` |

**Inflate scrolly** — sticky center panel shows a single huge number with a role label (who is reporting) and a sublabel. As the user scrolls, the number grows (both physically larger and color-shifts from white toward red). Six steps:

| Step | Number | Role label | Overlay card text |
|------|--------|------------|--------------------|
| 0 | `100 tons` | Actual harvest | `The actual harvest: roughly **100 tons**. The Party secretary knows this. Everyone in the village knows this.` |
| 1 | `200 tons` | Village secretary | `The village secretary writes **200 tons**. Double the truth. He has seen what happens to those who report low numbers.` |
| 2 | `350 tons` | County official | `The county official receives six reports, all inflated. He adds his own margin. **350 tons.**` |
| 3 | `600 tons` | Prefecture | `The prefecture consolidates. Nobody wants to be the one with lower numbers. **600 tons.**` |
| 4 | `1,000 tons` | Provincial report → Beijing | `The provincial report reaches Beijing. **1,000 tons.** Ten times reality. Mao reads this and orders the surplus exported.` |
| 5 | Collapse into famine | — | Card with red border: `**The number collapses into reality.** There is no surplus. There is famine.` |

After the scrolly ends, a full-width black panel displays the **famine counter**: a huge number that counts up (from 0) on entry to a final estimated death toll, with the label `estimated deaths, 1959–1961`.

### Part 2 — Festinger / cognitive dissonance

| # | Element | Content |
|---|---------|---------|
| 3.5 | Information-seal paragraph | `Every local official in the chain knew the real numbers. The information that could have prevented the famine existed at every level of the system. It could not travel upward, because traveling upward meant telling Mao he was wrong, and telling Mao he was wrong meant you were the enemy. The system did not lack information. It was sealed against it.` |
| 3.6 | Festinger blockquote | `"A man with a conviction is a hard man to change. Tell him you disagree and he turns away. Show him facts or figures and he questions your sources. Appeal to logic and he fails to see your point."` — cite: `— Leon Festinger, 1957` |
| 3.7 | **Cognitive-dissonance interactive demo** | A dark card containing three lines that fade in sequentially on scroll: (1) `The harvest was 100 tons.` (2) In red: `The Party says the harvest was 1,000 tons.` (3) Prompt: `What do you report?`. Two buttons appear: `Accept the fact` / `Reject the fact`. Clicking either button shows the same result: `In 1959, every official chose "Reject."` with subline `Belief in the Party outranked the evidence of their own fields.` The chosen button stays red-highlighted; the other fades to 30% opacity; both are locked. |

### Part 3 — The Confession (Moscow Show Trials)

| # | Element | Content |
|---|---------|---------|
| 3.8 | Subheading | `The Confession` |
| 3.9 | Image | `s3-moscow-trial.jpg` — alt: "Moscow Show Trials courtroom, 1936-1938" — caption: "Moscow Show Trials, 1936–1938". |
| 3.10 | Moscow trial paragraphs | `Moscow, 1936. Stalin's prosecutors put a group of Old Bolsheviks on trial. These men — Kamenev, Zinoviev, Bukharin — had fought alongside Lenin. They had built the Soviet state. The charge was treason.` / `They confessed. In open court, in front of foreign journalists, they declared themselves enemies of the people. Some had been tortured. But Bukharin's confession was different. He spoke at length, with apparent conviction. Arthur Koestler tried to explain it in `Darkness at Noon`: if you have spent your entire life believing that the Party is the instrument of history, then admitting the Party is wrong means your life was pointless. Confession — even false confession — is the last way to remain loyal.` |
| 3.11 | **Trial list table** | Five rows, each with name / role / verdict: `Lev Kamenev` · `Politburo member, revolutionary` · `Confessed → Executed`; `Grigory Zinoviev` · `Comintern chairman` · `Confessed → Executed`; `Nikolai Bukharin` · `Party theoretician, Pravda editor` · `Confessed → Executed`; `Alexei Rykov` · `Chairman of the Council` · `Confessed → Executed`; `Karl Radek` · `Revolutionary journalist` · `Confessed → Imprisoned → Died`. |
| 3.12 | Synthesis paragraph | `The Party secretary who lied about the harvest and the Old Bolshevik who confessed to a crime he did not commit are doing the same thing. They are protecting the belief at the cost of everything else. The system is sealed. Information that contradicts the belief cannot enter.` |
| 3.13 | Filter-bubble paragraph | `Today this runs on infrastructure Festinger could not have imagined. Social media algorithms optimize for engagement. Devotion engages. Doubt does not. Eli Pariser called this the filter bubble — an environment where the information you see is pre-selected to confirm what you already believe. The technology is new. The psychology is Festinger's. The scale is what changed.` |
| 3.14 | Hoffer blockquote | `"Mass movements can rise and spread without belief in a God, but never without belief in a devil."` — cite: `— Eric Hoffer, The True Believer, 1951` |

---

## SECTION 4 — Transition to Takeaway

A dedicated scrollytelling zone where the entire viewport background scroll-scrubs from black (#0A0A0A) to white (#FFFFFF). Text color cross-fades simultaneously. No prose — pure visual transition into the Takeaway section.

---

## SECTION 5 — Takeaway

Section inverts to a bright white background (#FFFFFF) with pure black text. All typography stays sans-serif Inter. The accent color becomes #111 for blockquote border instead of red.

| # | Element | Content |
|---|---------|---------|
| 5.1 | Section label | `Takeaway` |
| 5.2 | Opening paragraphs | `If you have read this far, you might be thinking: we need better leaders. Wiser ones. More careful ones.` / `That thought is the trap. It is the same logic that dismantled the Weimar Republic, that fueled the Cultural Revolution, that turned Lenin's revolution into Stalin's prison state. Every one of those catastrophes began with a population convinced they had found the right person.` |
| 5.3 | Founders blockquote | `The founders of the American republic read their history. They did not design for angels. They designed for men who would inevitably become corrupt, cowardly, or deluded — and they tried to build a system that could survive them anyway.` |
| 5.4 | Auxiliary precautions intro | `Madison and his contemporaries built what they called "auxiliary precautions" — structures that keep functioning even when the people inside them fail:` |
| 5.5 | Principle 1 | `1. **Separation of powers.** No single person holds enough authority to act alone. This is slow by design.` |
| 5.6 | Principle 2 | `2. **Term limits and succession rules.** Written in advance, enforced without exception. The leader leaves. The system stays.` |
| 5.7 | Principle 3 | `3. **Independent press and judiciary.** Their job is to say no — to the leader, to the crowd, to the mood of the moment.` |
| 5.8 | "Boring is why it works" paragraphs | `Nobody chants for judicial independence. There are no rallies for procedural checks. You cannot build a mass movement around the separation of powers. These things are boring. That is why they work.` / `The founders spent a summer in Philadelphia designing these cages. They read Thucydides, studied Rome, argued for months over how to constrain ambition. They were meticulous.` / `It took 240 years to find someone willing to take them apart.` |

### Trump stat cards (distributed alongside their source paragraphs)

Each of the four following rows is a two-column grid: a paragraph on the left, a small white-on-light-gray stat card with a red left border on the right. When the row scrolls into view, the card fades up and the number animates from 0 to its target.

| # | Paragraph | Stat card (number counts up to) |
|---|-----------|----------------------------------|
| 5.9 | `In his first year back in office, Donald Trump signed hundreds of executive orders — governing by decree in a system designed to prevent exactly that. He created DOGE, an unelected body with no congressional authorization, and gave it access to Treasury payment systems, Medicare records, and Social Security data.` | `250+` — label: `Executive orders in year one` |
| 5.10 | `When a federal judge ordered his administration to stop deporting Venezuelan immigrants mid-flight, the planes kept flying. When the Supreme Court ruled that a man mistakenly deported to El Salvador must be brought back, the administration said it was El Salvador's problem.` | `33%` — label: `Court rulings defied (1 in 3)` |
| 5.11 | `ICE agents began arresting people at immigration courthouses — the very hearings the government required them to attend. Arrests of people with no criminal record rose sharply in a single year.` | `2,450%` — label: `Increase in no-record arrests` |
| 5.12 | `By December 2025, ICE was holding people in detention at the highest number ever recorded.` | `66,000` — label: `People in ICE detention, Dec 2025` |

| # | Element | Content |
|---|---------|---------|
| 5.13 | Closing paragraphs | `The cages are still standing — most of them. But they are being opened from the inside, with keys the founders themselves provided. Norms turned out not to be laws. Institutions turned out not to enforce themselves. And a country that was designed to distrust its leaders turned out to be perfectly capable of worshipping one.` / `The founders designed for corruption, for ambition, even for delusion. They did not design for an audience that would watch the dismantling and call it entertainment.` |

---

## SECTION 6 — Closing

A short all-white section containing a single line of text revealed **word-by-word** as the user scrolls past it (each word fades in independently, left to right):

> `The next charismatic leader will come. They always do. Whether anyone still cares about the cages — that we do not know yet.`

---

## SECTION 7 — References

Heading: `References`. Unordered list:

1. Frank Herbert, UCLA Speech, April 17, 1985 (transcript: theaugustry.com)
2. Max Weber, *Economy and Society* (1922)
3. James Madison, *Federalist No. 51* (1788)
4. Eric Hoffer, *The True Believer* (1951)
5. Leon Festinger, *When Prophecy Fails* (1956)
6. Arthur Koestler, *Darkness at Noon* (1940)
7. Roderick MacFarquhar & Michael Schoenhals, *Mao's Last Revolution* (2006)
8. Richard J. Evans, *The Coming of the Third Reich* (2005)
9. Eli Pariser, *The Filter Bubble* (2011)
10. Jonathan Haidt, *The Righteous Mind* (2012)
11. Fred M. Donner, *Muhammad and the Believers* (2010)

---

## Appendix — Complete asset list

All images are in `/assets/`. Grayscale filter applied globally (~80%) unless noted.

| Filename | Used in | Alt text / description |
|----------|---------|------------------------|
| `opening-JFK-Nixon-debate.jpg` | Hero background | John F. Kennedy and Richard Nixon at their first televised presidential debate, Chicago, 1960. |
| `opening-frankherbert.jpg` | Hero, top-right portrait | Portrait of Frank Herbert. |
| `s1-hitler-reichstag.jpg` | S1 Part II, step 0 | Hitler at the Kroll Opera House, March 1933. |
| `s1-cultural-revolution.jpg` | S1 Part III, step 0 | Red Guards rally in Beijing, 1966. |
| `s1-mao-tiananmen.jpg` | (unused in final layout) | Mao at Tiananmen. |
| `s1-weber-oratory.png` | (unused in final layout) | Weber-era oratory illustration. |
| `s1-charismatic-leadership.jpg` | (unused in final layout) | — |
| `s2-lenin-stalin.jpg` | S2 Case A | Lenin and Stalin at Gorki, 1922. |
| `s2-stalin-propaganda-1.jpg` | S2 Case A | Soviet propaganda poster, 1933 ("With the banner of Lenin..."). |
| `s2-stalin-propaganda-2.jpg` | (available, not placed in final layout) | — |
| `s2-lenin-origianl.jpg` | S2 before/after slider #1 — ORIGINAL | Lenin speaking at Sverdlov Square, 1920, with Trotsky and Kamenev beside the podium. |
| `s2-lenin_removed.jpg` | S2 before/after slider #1 — RETOUCHED | Same photograph, Trotsky and Kamenev erased. |
| `s2_stalin_original.jpg` | S2 before/after slider #2 — ORIGINAL | Stalin walking with Nikolai Yezhov along the Moscow-Volga Canal. |
| `s2_stalin_removed.jpg` | S2 before/after slider #2 — RETOUCHED | Same photograph, Yezhov erased. |
| `s2-gulag-workers.jpg` | S2 Case A | Gulag prisoners building the White Sea–Baltic Canal. |
| `s2-muhammud.jpg` | S2 Case B | The early Islamic world. |
| `s2-karbala.webp` | S2 Case B, full-bleed | The Battle of Karbala, 680 CE. |
| `s2-abura.jpeg` | S2 Case B | Ashura commemoration. |
| `s3-moscow-trial.jpg` | S3 Confession | Moscow Show Trials courtroom, 1936–1938. |
| `Great-Leap-Forward-China-Yingshuichiao-Iron-Smelting-works-1950s_副本.jpg` | S3 opening | Backyard steel furnaces during China's Great Leap Forward. |

---

## Appendix — Interaction summary for non-visual users

The page is fully readable as linear prose even if every interactive element is skipped. All visualizations are supplemental illustrations of points made in the surrounding text. A non-visual summary of what each "black box" would be doing to a sighted user:

1. **Hero intro** — three lines of text revealed one by one as the user scrolls; "58,000 / Americans killed in Vietnam. / Because no one questioned a charismatic president."
2. **Weber bars (S1 Theory)** — visually asserts that "charisma dominates and crushes tradition and law."
3. **Reichstag hemicycle (S1 Enabling)** — visually reconstructs the 441-to-94 vote: the chamber fills red as institutional resistance collapses.
4. **Cultural Revolution timeline (S1 Fire)** — year-by-year escalation from 1966 to 1976, with intensity building to 100% and a final death-toll line.
5. **Before/after photo sliders (S2 Case A)** — interactive proof that the Soviet state edited Trotsky and Yezhov out of existence in its own photographic record.
6. **Purge stat counters + victim grid (S2 Case A)** — quantifies the Great Purge in executed / gulag numbers and a dot grid.
7. **Islamic branch tree (S2 Case B)** — static SVG tree listing every major Sunni/Shia branch with hover tooltips; culminates in a death toll of 1,850,000+ across four modern sectarian wars.
8. **632 → 2026 sticky counter (S2 end)** — visually equates the passage of 1,394 years with a cumulative death toll climbing from 0 to 1,850,000.
9. **Inflate scrolly (S3 Great Leap Forward)** — visually dramatizes the harvest number growing 100 → 200 → 350 → 600 → 1,000 tons as each layer of the bureaucracy lies upward, then collapsing into famine.
10. **Famine counter (S3)** — counts up to an estimate of the Great Famine death toll (1959–61).
11. **Dissonance demo (S3 Festinger)** — a two-button choice that delivers the same answer regardless: "In 1959, every official chose 'Reject.'"
12. **Trial list (S3 Confession)** — five-row table of Old Bolsheviks and their verdicts.
13. **Transition zone** — pure visual scrub from dark mode to light mode.
14. **Trump stat cards (Takeaway)** — four numbers beside their source paragraphs: 250+ executive orders, 33% of court rulings defied, 2,450% rise in no-record arrests, 66,000 in ICE detention.
15. **Closing** — word-by-word reveal of a single line.
