# Engineering Implementation Brief — index.html v5 Rewrite

**Target file:** `index.html` (GitHub commit `d6f8acd`, 1621 lines, single-file HTML/CSS/JS)
**Authoritative spec:** `content-inventory-v5.md`
**Base version:** GitHub `origin/main` — the local copy may have stale edits; use `git show origin/main:index.html` as the source of truth.

This brief covers **8 changes** from 修改意见 ver2. All line numbers reference the GitHub version.

---

## CHANGE 1 — Flash-card scroll architecture (G3 rewrite)

**Problem:** The current G3 implementation relies on `margin-bottom: max(18vh, 140px)` between `.fade-in` elements (lines 48–52). This does not reliably prevent multiple elements from being visible simultaneously — on large screens or with short content, 2–4 elements stack into view at once.

**Solution:** Replace the margin-based approach with **GSAP ScrollTrigger pin-based flash cards**. Every standalone `.fade-in` element in `.prose-section` containers gets individually pinned to the viewport.

### CSS changes (lines 47–53)

Keep the existing margin rules as a **no-JS fallback only**. Add new CSS:

```css
/* === G3: FLASH-CARD SCROLL (v5) === */
.flashcard-pin{min-height:100vh;display:flex;flex-direction:column;justify-content:center;padding:80px 40px}
```

Do NOT apply `min-height:100vh` via CSS alone — the JS will handle pinning. The CSS class is just for no-JS fallback styling.

### JS changes (lines 1211–1214)

**Replace the current generic fade-in handler:**

```js
// OLD (delete):
gsap.utils.toArray('.fade-in').forEach(el=>{
  gsap.to(el,{opacity:1,y:0,duration:0.8,scrollTrigger:{trigger:el,start:'top 85%'}});
});
```

**With a pin-based flash-card system:**

```js
// NEW: Flash-card scroll (G3 v5)
gsap.utils.toArray('.prose-section .fade-in').forEach(el=>{
  // Pin each element to viewport center while active
  ScrollTrigger.create({
    trigger:el,
    start:'top 80%',
    end:'bottom 20%',
    onEnter:()=>gsap.to(el,{opacity:1,y:0,duration:0.6}),
    onLeave:()=>gsap.to(el,{opacity:0,y:-30,duration:0.4}),
    onEnterBack:()=>gsap.to(el,{opacity:1,y:0,duration:0.6}),
    onLeaveBack:()=>gsap.to(el,{opacity:0,y:30,duration:0.4})
  });
});
// Non-prose fade-ins (inside scrolly modules, takeaway, etc.) keep simple reveal
gsap.utils.toArray('.fade-in:not(.prose-section .fade-in)').forEach(el=>{
  gsap.to(el,{opacity:1,y:0,duration:0.8,scrollTrigger:{trigger:el,start:'top 85%'}});
});
```

**Also increase the spacing between `.fade-in` elements** to guarantee separation even on tall screens:

```css
/* Line 48 — increase from max(18vh,140px) to max(40vh,300px) */
.prose-section .fade-in{margin-bottom:max(40vh,300px)}
.prose-section .fade-in:last-child{margin-bottom:0}
.prose-section blockquote.fade-in{margin-top:max(30vh,240px);margin-bottom:max(40vh,300px)}
.prose-section .section-image.fade-in{margin-top:max(40vh,300px)}
```

### Scrolly module boundaries

At the END of each scrolly module (hemicycle, CR timeline, inflate, polarization), add a spacer div:

```html
<div style="height:40vh" aria-hidden="true"></div>
```

This prevents the next section's content from leaking into view when the scrolly unpins.

### Hero body (lines 414–419)

The hero-body paragraphs use their own spacing (`margin-bottom: max(18vh, 140px)` on line 70). **Increase to `max(40vh, 300px)`** to match the new flash-card spacing:

```css
/* Line 70 */
.hero-body p{opacity:0;margin-bottom:max(40vh,300px)}
```

---

## CHANGE 2 — Global font size increase

**Problem:** Body text at 18px is too small on a fullscreen laptop browser. The Cultural Revolution timeline sub-text is especially hard to read.

### CSS changes — find and replace these exact values:

| Line | Old | New |
|------|-----|-----|
| 14 | `font-size:18px` (body) | `font-size:20px` |
| 16 | `font-size:28px` (h2) | `font-size:32px` |
| 17 | `font-size:14px` (h3) | `font-size:15px` |
| 21 | `font-size:20px` (blockquote) | `font-size:22px` |
| 22 | `font-size:14px` (blockquote cite) | `font-size:15px` |
| 24 | `font-size:12px` (.section-label) | `font-size:13px` |
| 65 | `font-size:13px` (.hero-portrait-caption) | `font-size:14px` |
| 66 | `font-size:24px` (.hero-quote) | `font-size:26px` |
| 76 | `font-size:22px` (#heroIntro .intro-sub1) | `font-size:24px` |
| 77 | `font-size:17px` (#heroIntro .intro-sub2) | `font-size:19px` |
| 111 | `font-size:14px` (.ba-erasure-intro) | `font-size:16px` |
| 119 | `font-size:13px` (.ba-caption) | `font-size:14px` |
| 135 | `font-size:14px` (.yc-year-label) | `font-size:16px` |
| 138 | `font-size:16px` (.yc-toll-label) | `font-size:18px` |
| 139 | `font-size:18px` (.yc-event-label) | `font-size:20px` |
| 144 | `font-size:18px` (.dd-step) | `font-size:20px` |
| 146 | `font-size:16px` (.dd-scene) | `font-size:18px` |
| 149 | `font-size:14px` (.dd-context) | `font-size:16px` |
| 150 | `font-size:13px` (.dd-prompt) | `font-size:14px` |
| 152 | `font-size:14px` (.dd-btn) | `font-size:16px` |
| 159 | `font-size:14px` (.dd-result-sub) | `font-size:16px` |
| 171 | `font-size:14px` (.pol-label) | `font-size:16px` |
| 177 | `font-size:13px` (.section-image .caption) | `font-size:14px` |
| 197 | `font-size:16px` (.cr-event-text) | `font-size:18px` |
| 200 | `font-size:14px` (.cr-death-toll) | `font-size:16px` |
| 201 | `font-size:12px` (.cr-causal) | `font-size:14px` |
| 232 | `font-size:19px` (.peng-text) | `font-size:21px` |
| 231 | `font-size:14px` (.peng-caption) | `font-size:15px` |

### Responsive breakpoint (line 353):

```css
/* Old: */
body{font-size:16px}
/* New: */
body{font-size:18px}
```

Also on line 354:
```css
/* Old: */
h1,.hero-title{font-size:36px}
/* New: */
h1,.hero-title{font-size:38px}
```

And line 355:
```css
/* Old: */
h2{font-size:22px}
/* New: */
h2{font-size:26px}
```

---

## CHANGE 3 — Nixon/Kennedy debate paragraph expanded

**Line 415** — replace the existing paragraph:

```html
<!-- OLD: -->
<p>Seventy million Americans watched that debate. The ones who listened on radio thought Richard Nixon won. The ones who watched on television were certain it was Kennedy. Same words. The only difference was the screen.</p>
```

```html
<!-- NEW: -->
<p>On September 26, 1960, seventy million Americans tuned in to the first televised presidential debate in the country's history. Richard Nixon had been vice president for eight years. He knew policy cold. On substance, the people who listened on radio thought he won. But Nixon had recently been hospitalized, and it showed — he looked pale, underweight, and was visibly sweating under the studio lights. Kennedy, tanned and composed, looked like he belonged on camera. The television audience was certain Kennedy won. Same words, same arguments. The only difference was the screen. Two months later, Kennedy won the presidency by less than 120,000 votes out of 69 million cast — one of the narrowest margins in American history. The election did not turn on policy. It turned on the fact that one man looked like a leader and the other did not.</p>
```

**NOTE:** This is now a long paragraph. Under the flash-card system (Change 1), it occupies one full card by itself. That is fine — long text on a single card is acceptable as long as no OTHER element is visible at the same time.

---

## CHANGE 4 — Dune/Chalamet section reordered

**Lines 416–418** — reorder the three elements in hero-body Phase 3.

**Current order (lines 416–418):**
```html
<p>Frank Herbert watched a science fiction audience fall in love with Paul Atreides — the hero of <em>Dune</em> — and it horrified him. He had written Paul as a warning. Readers took him as a savior. So Herbert wrote sequel after sequel to make the point as brutal as possible: the hero will destroy you. Not because he wants to. Because you will let him.</p>
<div class="section-image"><img src="assets/opening-paul-atreides.png" alt="Paul Atreides"><div class="caption">The hero Herbert tried to warn you about.</div></div>
<p>What happens when people stop questioning. How institutions collapse. How movements outlive the people who started them. How followers seal themselves inside a belief until nothing can reach them.</p>
```

**New order:**
```html
<div class="section-image"><img src="assets/opening-paul-atreides.png" alt="Paul Atreides in Dune (2021)"><div class="caption">Paul Atreides — the hero of Frank Herbert's <em>Dune</em>.</div></div>
<p>Frank Herbert watched a science fiction audience fall in love with Paul Atreides — the hero of <em>Dune</em> — and it horrified him. He had written Paul as a warning. Readers took him as a savior. So Herbert wrote sequel after sequel to make the point as brutal as possible: the hero will destroy you. Not because he wants to. Because you will let him.</p>
<p>What happens when people stop questioning. How institutions collapse. How movements outlive the people who started them. How followers seal themselves inside a belief until nothing can reach them.</p>
```

Key differences: (a) image moves to first position, (b) alt text updated to "Paul Atreides in Dune (2021)", (c) caption changed from "The hero Herbert tried to warn you about." to "Paul Atreides — the hero of Frank Herbert's *Dune*." — this identifies the character for readers who haven't seen the film.

---

## CHANGE 5 — Hero background image repositioned

**Line 61** — add `object-position` to prevent Nixon/Kennedy faces from being cropped:

```css
/* OLD: */
#hero .hero-bg img{width:100%;height:100%;object-fit:cover;opacity:0.15;filter:grayscale(100%)}
/* NEW: */
#hero .hero-bg img{width:100%;height:100%;object-fit:cover;object-position:center 30%;opacity:0.15;filter:grayscale(100%)}
```

---

## CHANGE 6 — Routinization pathway diagram enlarged

**Line 95** — increase max-width:

```css
/* OLD: */
.routine-diagram{margin:0 auto;max-width:min(80vw,900px);width:100%}
/* NEW: */
.routine-diagram{margin:0 auto;max-width:min(90vw,1100px);width:100%}
```

---

## CHANGE 7 — Before/after slider: initial state + aspect ratio

### 7a. CSS initial state (line 115–116)

```css
/* OLD: */
.ba-slider .ba-after{clip-path:inset(0 0 0 50%)}
.ba-divider{position:absolute;top:0;bottom:0;left:50%;width:2px;background:#c0392b;transform:translateX(-50%);pointer-events:none;box-shadow:0 0 12px rgba(192,57,43,0.5)}
/* NEW — start at 100% (full original visible): */
.ba-slider .ba-after{clip-path:inset(0 0 0 100%)}
.ba-divider{position:absolute;top:0;bottom:0;left:100%;width:2px;background:#c0392b;transform:translateX(-50%);pointer-events:none;box-shadow:0 0 12px rgba(192,57,43,0.5)}
```

### 7b. Handle initial position (line 117)

```css
/* OLD: */
.ba-handle{position:absolute;top:50%;left:50%;transform:translate(-50%,-50%);...}
/* NEW: */
.ba-handle{position:absolute;top:50%;left:100%;transform:translate(-50%,-50%);...}
```

### 7c. Aspect ratio enforcement (line 113)

Both image pairs have different source aspect ratios causing misalignment. Force a unified ratio:

```css
/* OLD: */
.ba-slider .ba-wrap{position:relative;width:100%;aspect-ratio:16/10;overflow:hidden;border-radius:4px;background:#1a1a1a;cursor:ew-resize;user-select:none}
/* NEW: */
.ba-slider .ba-wrap{position:relative;width:100%;aspect-ratio:4/3;overflow:hidden;border-radius:4px;background:#1a1a1a;cursor:ew-resize;user-select:none}
```

The `object-fit: cover` on line 114 already handles cropping — changing the container aspect-ratio to `4/3` will make both sliders consistent. If `4/3` crops too aggressively on one pair, test `3/2` as an alternative.

### 7d. Labels update (lines 588, 598)

Since the slider now starts showing the original fully, update the labels:

Line 588: `<div class="ba-labels"><span>Original (1920)</span><span>← Drag to reveal retouched</span></div>`

Line 598: `<div class="ba-labels"><span>Original</span><span>← Drag to reveal altered</span></div>`

---

## CHANGE 8 — Year counter → Horizontal timeline

**This is a full rewrite of the module.** Delete the current HTML (lines 698–707) and CSS (lines 132–140), and the JS that drives it.

### 8a. New CSS (replace lines 132–140)

```css
/* === HORIZONTAL DEATH-TOLL TIMELINE (v5) === */
.htl-wrap{position:relative;height:250vh;margin:64px 0}
.htl-sticky{position:sticky;top:0;height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:0 40px;gap:32px}
.htl-toll{font-size:clamp(64px,12vw,140px);font-weight:600;color:#c0392b;letter-spacing:-3px;line-height:1;font-variant-numeric:tabular-nums;text-shadow:0 0 60px rgba(192,57,43,0.25);min-width:600px;text-align:center}
.htl-axis-wrap{position:relative;width:min(80vw,900px);height:120px}
.htl-axis{position:absolute;top:50%;left:0;right:0;height:2px;background:#1f1f1f;transform:translateY(-50%)}
.htl-axis-labels{position:absolute;top:calc(50% + 16px);left:0;right:0;display:flex;justify-content:space-between;font-size:13px;color:#555;font-variant-numeric:tabular-nums}
.htl-progress{position:absolute;top:50%;left:0;height:2px;background:#c0392b;transform:translateY(-50%);width:0%;transition:none}
.htl-marker{position:absolute;top:0;transform:translateX(-50%);text-align:center;opacity:0;transition:opacity 0.6s}
.htl-marker.active{opacity:1}
.htl-marker.past{opacity:0.5}
.htl-marker-dot{width:10px;height:10px;background:#c0392b;border-radius:50%;margin:0 auto 8px}
.htl-marker-year{font-size:12px;color:#888;font-weight:500}
.htl-marker-event{font-size:13px;color:#d0d0d0;white-space:nowrap;max-width:140px;white-space:normal;text-align:center;line-height:1.4}
.htl-marker-toll{font-size:12px;color:#c0392b;font-weight:500;margin-top:2px}
.htl-sublabel{font-size:16px;color:#888;font-style:italic;max-width:680px;text-align:center;margin-top:8px}
```

### 8b. New HTML (replace lines 698–707)

```html
<div class="htl-wrap" id="htlWrap">
  <div class="htl-sticky">
    <div class="htl-toll" id="htlToll">0</div>
    <div class="htl-axis-wrap">
      <div class="htl-axis"></div>
      <div class="htl-progress" id="htlProgress"></div>
      <div class="htl-marker" data-year="680" style="left:3.4%"><div class="htl-marker-dot"></div><div class="htl-marker-year">680</div><div class="htl-marker-event">Karbala</div><div class="htl-marker-toll">~10,000</div></div>
      <div class="htl-marker" data-year="750" style="left:8.5%"><div class="htl-marker-dot"></div><div class="htl-marker-year">750</div><div class="htl-marker-event">Umayyad civil wars</div><div class="htl-marker-toll">~70,000</div></div>
      <div class="htl-marker" data-year="1988" style="left:97.4%"><div class="htl-marker-dot"></div><div class="htl-marker-year">1988</div><div class="htl-marker-event">Iran-Iraq War</div><div class="htl-marker-toll">~1,000,000</div></div>
      <div class="htl-marker" data-year="2011" style="left:99.1%"><div class="htl-marker-dot"></div><div class="htl-marker-year">2011</div><div class="htl-marker-event">Iraq Civil War</div><div class="htl-marker-toll">~200,000</div></div>
      <div class="htl-marker" data-year="2014" style="left:99.3%"><div class="htl-marker-dot"></div><div class="htl-marker-year">2014</div><div class="htl-marker-event">Syrian Civil War</div><div class="htl-marker-toll">~500,000</div></div>
      <div class="htl-marker" data-year="2024" style="left:100%"><div class="htl-marker-dot"></div><div class="htl-marker-year">2024</div><div class="htl-marker-event">Yemen Civil War</div><div class="htl-marker-toll">~150,000+</div></div>
      <div class="htl-axis-labels"><span>632 CE</span><span>2024</span></div>
    </div>
    <div class="htl-sublabel">killed in conflicts with sectarian dimensions — each triggered by its own political crisis, none reducible to religion alone</div>
  </div>
</div>
```

**NOTE on marker positions:** The events cluster heavily toward the right end of the timeline (all modern wars are in the last 3% of the 632–2024 range). This is intentional — it visually communicates that most of the death toll accumulated in the modern era. However, if the markers overlap too much, use a **non-linear scale** for the last 100 years: compress 632–1900 into 60% of the axis, expand 1900–2024 into 40%. Adjust the `left:%` values accordingly. Test and tweak.

### 8c. New JS (replace the old year-counter ScrollTrigger)

Find and delete the old year-counter JS block (search for `yearCounter` or `ycNum` in the JS section). Replace with:

```js
// === HORIZONTAL TIMELINE (v5) ===
(function(){
  const data=[
    {year:680,toll:10000},{year:750,toll:80000},
    {year:1500,toll:120000},{year:1980,toll:150000},
    {year:1988,toll:1150000},{year:2011,toll:1400000},
    {year:2014,toll:1700000},{year:2024,toll:1850000}
  ];
  const tollEl=document.getElementById('htlToll');
  const progressEl=document.getElementById('htlProgress');
  const markers=document.querySelectorAll('.htl-marker');
  if(!tollEl)return;
  ScrollTrigger.create({
    trigger:'#htlWrap',start:'top top',end:'bottom bottom',scrub:0.5,
    onUpdate:function(self){
      const p=self.progress;
      const minY=632,maxY=2024;
      const yr=Math.round(minY+p*(maxY-minY));
      // Interpolate death toll
      let toll=0;
      for(let i=0;i<data.length;i++){
        if(yr<data[i].year){
          if(i===0){toll=0;break}
          const prev=data[i-1],cur=data[i];
          const t=(yr-prev.year)/(cur.year-prev.year);
          toll=Math.round(prev.toll+t*(cur.toll-prev.toll));
          break;
        }
        toll=data[i].toll;
      }
      tollEl.textContent=toll.toLocaleString();
      progressEl.style.width=(p*100)+'%';
      markers.forEach(function(m){
        const my=parseInt(m.dataset.year);
        if(yr>=my){m.classList.add('active');if(yr>my+30)m.classList.add('past')}
        else{m.classList.remove('active');m.classList.remove('past')}
      });
    }
  });
})();
```

---

## EXECUTION ORDER

1. **Change 5** — Hero bg `object-position` (1 line CSS, zero risk)
2. **Change 6** — Routinization diagram max-width (1 line CSS)
3. **Change 2** — Global font size increase (many CSS lines, mechanical)
4. **Change 3** — Nixon/Kennedy paragraph replacement (1 HTML block)
5. **Change 4** — Dune/Chalamet reorder (3 HTML lines rearranged)
6. **Change 7** — Slider initial state + aspect ratio (CSS + label text)
7. **Change 8** — Year counter → horizontal timeline (CSS + HTML + JS rewrite)
8. **Change 1** — Flash-card scroll architecture (CSS + JS — most complex, do last)

---

## TESTING CHECKLIST

After all changes, verify in a fullscreen browser (~1440×900):

- [ ] **G3 flash-card:** Scroll through the entire page. At NO point should two independent elements be visible at the same time in any `.prose-section`. Each scroll step reveals one thing.
- [ ] **Font sizes:** Body text is visibly larger. The "1976" sub-text in the CR timeline is readable. All captions, labels, and small-caps have increased.
- [ ] **Nixon/Kennedy faces:** When the hero background image fades in, both candidates' faces are visible (not cropped above the viewport).
- [ ] **Debate context:** The paragraph mentions September 26 1960, describes Nixon's appearance, Kennedy's poise, and that Kennedy won the election by ~120,000 votes.
- [ ] **Dune order:** Scrolling through hero Phase 3 shows: debate text → Chalamet photo (captioned "Paul Atreides — the hero of Frank Herbert's Dune") → Herbert paragraph → closing paragraph.
- [ ] **Routinization diagram:** The Charisma→3-paths SVG diagram is noticeably larger, filling ~90% of viewport width.
- [ ] **Slider #1 (Lenin):** On first appearance, the full original photo is visible (divider at right edge). Dragging left reveals the retouched version.
- [ ] **Slider #2 (Stalin):** Same behavior — starts at full original.
- [ ] **Slider aspect ratios:** Both slider pairs display without misaligned/offset images.
- [ ] **Horizontal timeline:** The year counter section now shows a horizontal axis from 632→2024. Scrolling advances a red progress bar left-to-right. Markers appear at each conflict year. The cumulative number stays centered and does not shift layout as digits increase.
- [ ] **Timeline doesn't scroll away early:** The sticky behavior keeps the timeline pinned until the scroll zone is fully traversed — the user always reaches 2024.
- [ ] **Scrolly module boundaries:** After each scrolly module (hemicycle, CR timeline, inflate, polarization), there is empty space before the next content appears.
- [ ] **No-JS fallback:** Disabling JS still renders a readable page with all content visible.
- [ ] **Progress nav:** The right-side dot navigation still correctly tracks sections.
- [ ] **Responsive (768px):** Body text is 18px, nothing breaks.
