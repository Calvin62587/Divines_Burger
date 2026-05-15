# Divine Burger Personaje Visual Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a complete creative production package for the Divine Burger brand character: visual system, variants, prompt pack, evaluation rubric, and presentation-ready creative direction.

**Architecture:** This is a document-first creative system. The source of truth remains the approved brand criteria spec, and each new document adds one production layer: character bible, prompt pack, review rubric, and final client-facing presentation.

**Tech Stack:** Markdown documentation, local Git, optional AI image generation for visual exploration, and optional DOCX/PDF presentation export after approval.

---

## File Structure

- Modify: `docs/superpowers/specs/2026-05-15-divine-burger-personaje-criterios-marca.md`
  - Keep as the approved brand criteria source. Only change it if new criteria are approved.
- Create: `docs/brand/divine-burger-character-bible.md`
  - Defines the character system: identity, visual anatomy, variants, usage rules, and rejection rules.
- Create: `docs/brand/divine-burger-prompt-pack.md`
  - Contains production-ready prompts for realistic/cinematic image generation.
- Create: `docs/brand/divine-burger-evaluation-rubric.md`
  - Provides a scoring checklist for generated concepts and designer proposals.
- Create: `docs/brand/divine-burger-creative-presentation.md`
  - Client-facing summary for presenting the character direction clearly.
- Modify: `README.md`
  - Add links to the new brand documents and explain the project structure.

---

### Task 1: Character Bible

**Files:**
- Create: `docs/brand/divine-burger-character-bible.md`
- Read: `docs/superpowers/specs/2026-05-15-divine-burger-personaje-criterios-marca.md`

- [ ] **Step 1: Create the brand folder**

Run:

```powershell
New-Item -ItemType Directory -Force -Path docs/brand
```

Expected: `docs/brand` exists.

- [ ] **Step 2: Draft the character bible**

Create `docs/brand/divine-burger-character-bible.md` with this structure and content:

```markdown
# Divine Burger Character Bible

## Core Idea

**Divine Burger** is the visual character of Divine Burgers Colombia: a realistic gourmet hamburger elevated into a cinematic brand icon.

It is not an angel, not a cartoon mascot, and not a generic fast-food burger. It is a premium burger with presence, appetite, aura, and brand memory.

## Creative Rule

First it must make people hungry. Then it must build brand recognition.

## Visual Anatomy

### Burger Body

- Glossy brioche bun, tall and warm.
- Thick handmade beef patty with grilled edges.
- Premium cheese or sauce with controlled drip.
- Visible craft ingredients from the menu universe: bacon jam, pineapple, plantain, blueberry reduction, pesto, uchuva, chorizo, or roasted cheese.
- Real food texture, never plastic or toy-like.

### Aura Divine

- Minimal halo or aura inspired by the uppercase D from the existing logo.
- Warm light, subtle glow, and premium restraint.
- The aura must frame the burger without replacing it.

### Sello D

- The D can appear as a subtle brand mark on the bun, wrapper, box, background, or light pattern.
- It must read as a premium signature, not as a loud sticker.

## Personality

- Gourmet.
- Provocative.
- Cinematic.
- Celestial without being literal religion.
- Handcrafted.
- Confident.
- Foodie.
- Rooted in Bogota Sur pride.

## Official Variants

### Institutional

Clean, iconic, low-fire version for profile image, brand decks, menu cover, and packaging marks.

### Hero Shot

Premium campaign version with smoke, side light, dark background, high appetite, and cinematic depth.

### Modo Pecadora

More intense campaign version with stronger fire, cheese pull, sauce shine, and provocative energy for reels and promotional pieces.

### Sticker/Sello

Simplified version for stickers, highlights, packaging seals, delivery bags, and merchandise.

## Never Do

- Do not add cartoon eyes, arms, or a smiling face.
- Do not make the halo look like an angel costume.
- Do not make the burger look cheap, plastic, or generic.
- Do not let the D overpower the product.
- Do not use religious symbols beyond the restrained aura language.
- Do not reduce appetite for the sake of decoration.

## Success Test

A concept works when a customer can understand three things in under two seconds:

1. This is a gourmet burger.
2. This belongs to Divine Burgers.
3. I want to eat it.
```

- [ ] **Step 3: Review the character bible against the source criteria**

Run:

```powershell
Select-String -Path docs/brand/divine-burger-character-bible.md -Pattern "cartoon|angel|gourmet|D|aura|hungry|Divine"
```

Expected: The output confirms the bible includes the approved anti-cartoon, anti-angel, gourmet, D, aura, appetite, and Divine Burger criteria.

- [ ] **Step 4: Commit Task 1**

Run:

```powershell
git add docs/brand/divine-burger-character-bible.md
git commit -m "Add Divine Burger character bible"
```

Expected: Commit succeeds.

---

### Task 2: Prompt Pack

**Files:**
- Create: `docs/brand/divine-burger-prompt-pack.md`
- Read: `docs/brand/divine-burger-character-bible.md`

- [ ] **Step 1: Create the prompt pack**

Create `docs/brand/divine-burger-prompt-pack.md` with this content:

```markdown
# Divine Burger Prompt Pack

## Global Prompt Rules

Use these rules in every visual prompt:

- Realistic gourmet burger.
- Cinematic food photography.
- Dark premium studio background.
- Warm side light.
- Subtle smoke or flame.
- Glossy brioche bun.
- Thick handmade beef patty.
- Premium cheese or sauce texture.
- Minimal aura inspired by the uppercase D logo.
- Subtle D brand mark on bun, wrapper, box, or background.
- No cartoon face, no arms, no childish mascot, no angel character.

## Master Prompt: Divine Burger Hero

Realistic cinematic gourmet hamburger as the main brand icon for Divine Burgers Colombia, glossy brioche bun, thick handmade beef patty with grilled edges, premium melted cheese and sauce with controlled drip, subtle smoke, warm side lighting, dark charcoal studio background, minimal celestial aura inspired by an uppercase D logo behind the burger, discreet D brand mark on the wrapper, premium handcrafted food photography, dramatic depth of field, appetizing texture, elegant provocative mood, no cartoon, no face, no arms, no angel, no cheap fast food look.

## Variant Prompt: Institutional

Realistic premium gourmet hamburger centered like a brand emblem, clean glossy brioche bun, thick artisan beef patty, subtle cheese shine, dark charcoal background, restrained warm halo shaped by light inspired by an uppercase D logo, discreet D mark on the bun, elegant minimal composition, high-end restaurant branding, no cartoon features, no human expression, no angel figure.

## Variant Prompt: Hero Shot

Close-up cinematic food photography of a gourmet artisan hamburger, glossy brioche bun, juicy thick beef patty, melted cheese, sauce texture, light smoke rising, controlled low flame in the background, warm side light, dark premium studio setting, subtle celestial aura inspired by the Divine Burgers uppercase D logo, branded wrapper with small D mark, dramatic and appetizing, premium campaign image, no cartoon, no mascot, no religious character.

## Variant Prompt: Modo Pecadora

Intense realistic cinematic gourmet burger, glossy brioche, thick grilled beef patty, bacon jam, melted cheddar, sauce dripping with premium texture, stronger fire glow, smoke, dark background, provocative high-contrast lighting, subtle D-shaped aura behind the burger, small D brand stamp on wrapper, indulgent and dramatic, made for viral social media, no eyes, no mouth, no arms, no angel, not childish.

## Variant Prompt: Sticker/Sello

Realistic simplified premium burger icon for packaging sticker, glossy brioche bun, thick artisan patty, cheese accent, subtle warm aura inspired by uppercase D logo, compact centered composition, transparent or dark background option, premium brand seal, no cartoon face, no childish mascot, no angel figure.

## Negative Prompt

cartoon, cute mascot, smiling face, eyes, arms, legs, angel, wings, religious statue, plastic food, cheap fast food, messy background, flat lighting, low resolution, unreadable logo, giant letter D covering the burger, childish illustration, fake burger, toy burger.
```

- [ ] **Step 2: Verify every prompt preserves the approved constraints**

Run:

```powershell
Select-String -Path docs/brand/divine-burger-prompt-pack.md -Pattern "realistic|gourmet|cinematic|D|aura|no cartoon|no angel"
```

Expected: Every variant references realism/gourmet/cinema and rejects cartoon/angel direction.

- [ ] **Step 3: Commit Task 2**

Run:

```powershell
git add docs/brand/divine-burger-prompt-pack.md
git commit -m "Add Divine Burger visual prompt pack"
```

Expected: Commit succeeds.

---

### Task 3: Evaluation Rubric

**Files:**
- Create: `docs/brand/divine-burger-evaluation-rubric.md`
- Read: `docs/brand/divine-burger-character-bible.md`
- Read: `docs/brand/divine-burger-prompt-pack.md`

- [ ] **Step 1: Create the rubric**

Create `docs/brand/divine-burger-evaluation-rubric.md` with this content:

```markdown
# Divine Burger Evaluation Rubric

Use this rubric to score generated images, designer sketches, agency proposals, or campaign visuals.

Score each category from 1 to 5.

## 1. Appetite

5: The burger immediately creates hunger and looks premium, juicy, warm, and real.

3: The burger is recognizable and decent but lacks strong craving.

1: The burger looks fake, cold, plastic, cheap, or unappetizing.

## 2. Gourmet Quality

5: The image clearly communicates brioche, artisan meat, premium ingredients, and craft.

3: The burger looks acceptable but could belong to any casual restaurant.

1: The image reads as generic fast food.

## 3. Cinematic Impact

5: Lighting, smoke, depth, contrast, and composition feel like a premium campaign.

3: The image has some mood but lacks memorable presence.

1: The image is flat, ordinary, or poorly lit.

## 4. Divine Brand Recognition

5: The D/aura system is clear, subtle, and strongly connected to Divine Burgers.

3: The D or aura exists but feels decorative or underdeveloped.

1: The concept could belong to any burger brand.

## 5. Avoids Wrong Territory

5: No cartoon, no angel mascot, no childish tone, no religious literalism.

3: Mostly avoids the wrong territory but has small visual risks.

1: Feels like a mascot, angel, toy, or religious illustration.

## 6. Versatility

5: Can work in profile image, reels, menu, packaging, stickers, and campaign visuals.

3: Works in one or two formats but does not scale well.

1: Only works as a single isolated image.

## Decision Guide

- 26-30: Strong candidate. Refine details and test in formats.
- 21-25: Good direction. Needs targeted improvement.
- 16-20: Weak. Rework before presenting.
- 15 or less: Reject.

## Mandatory Rejection Triggers

Reject immediately if:

- The burger is not the main object.
- The image looks like a cartoon mascot.
- The concept depends on an angel character.
- The D is larger or more important than the burger.
- The food does not look appetizing.
- The style feels cheap or generic.
```

- [ ] **Step 2: Verify the rubric has numeric scoring and rejection triggers**

Run:

```powershell
Select-String -Path docs/brand/divine-burger-evaluation-rubric.md -Pattern "Score each category|26-30|Reject immediately|cartoon|angel|D"
```

Expected: Output confirms scoring, thresholds, and mandatory rejection triggers are present.

- [ ] **Step 3: Commit Task 3**

Run:

```powershell
git add docs/brand/divine-burger-evaluation-rubric.md
git commit -m "Add Divine Burger evaluation rubric"
```

Expected: Commit succeeds.

---

### Task 4: Creative Presentation

**Files:**
- Create: `docs/brand/divine-burger-creative-presentation.md`
- Read: `docs/brand/divine-burger-character-bible.md`
- Read: `docs/brand/divine-burger-prompt-pack.md`
- Read: `docs/brand/divine-burger-evaluation-rubric.md`

- [ ] **Step 1: Create the presentation narrative**

Create `docs/brand/divine-burger-creative-presentation.md` with this content:

```markdown
# Divine Burger Creative Presentation

## 1. The Shift

The brand should not be represented by an angelito. The object that must become the ID of the brand is the burger itself.

The solution is **Divine Burger**: a realistic gourmet hamburger transformed into a cinematic brand icon.

## 2. Why This Works

Divine Burgers already owns a powerful territory: gastronomia celestial, artesanal real, provocative food content, and cinematic appetite.

A burger icon makes the category instantly clear. The aura and D system make it ownable for Divine Burgers.

## 3. The Character

Divine Burger is not a cartoon mascot. It is a premium hero object with presence.

It uses:

- A gourmet burger as the protagonist.
- A subtle aura inspired by the uppercase D in the logo.
- A discreet D stamp as a signature.
- Smoke, warm light, and dark cinematic atmosphere.

## 4. Visual System

The system has three layers:

1. Burger gourmet protagonista.
2. Aura Divine.
3. Sello D.

Together, these elements create a brand asset that can live without always showing the full logo.

## 5. Official Variants

### Institutional

For profile, packaging marks, and brand identity.

### Hero Shot

For menu, launch campaign, paid ads, and pinned posts.

### Modo Pecadora

For reels, promotions, and high-craving content.

### Sticker/Sello

For delivery packaging, stories, highlights, and merchandise.

## 6. Creative Standard

Every execution must pass this test:

1. Does it make the viewer hungry?
2. Does it look gourmet?
3. Does it feel cinematic?
4. Does the aura/D system make it Divine?
5. Does it avoid cartoon, angel, and cheap fast-food territory?

## 7. Recommended Next Move

Generate or design 6 to 10 visual explorations using the approved prompts. Score them with the rubric. Select the strongest 2 directions, then refine into a final master character.
```

- [ ] **Step 2: Verify the presentation is client-readable**

Run:

```powershell
Select-String -Path docs/brand/divine-burger-creative-presentation.md -Pattern "The Shift|Why This Works|The Character|Visual System|Recommended Next Move"
```

Expected: Output confirms the presentation has a clear narrative arc.

- [ ] **Step 3: Commit Task 4**

Run:

```powershell
git add docs/brand/divine-burger-creative-presentation.md
git commit -m "Add Divine Burger creative presentation"
```

Expected: Commit succeeds.

---

### Task 5: README Index and Push

**Files:**
- Modify: `README.md`

- [ ] **Step 1: Update README with document index**

Replace `README.md` content with:

```markdown
# Divine Burger Brand Character

Repositorio de trabajo para definir el personaje visual de marca de Divine Burgers Colombia.

## Concepto Base

El personaje principal es **Divine Burger**: una hamburguesa gourmet realista, cinematografica y provocadora, elevada a icono de marca.

La hamburguesa debe ser el objeto protagonista. El aura y la D del logo funcionan como firma visual, sin reemplazar el apetito ni convertir el concepto en un angelito.

## Documentos

- `docs/superpowers/specs/2026-05-15-divine-burger-personaje-criterios-marca.md` - criterios de marca aprobados.
- `docs/brand/divine-burger-character-bible.md` - sistema del personaje y variantes.
- `docs/brand/divine-burger-prompt-pack.md` - prompts para exploracion visual realista/cinematografica.
- `docs/brand/divine-burger-evaluation-rubric.md` - rubrica para evaluar conceptos.
- `docs/brand/divine-burger-creative-presentation.md` - narrativa para presentar la direccion creativa.

## Regla Central

Primero debe dar hambre. Despues debe construir marca.
```

- [ ] **Step 2: Confirm all files are tracked**

Run:

```powershell
git status --short
```

Expected: Only `README.md` is modified before staging, unless previous task commits were skipped.

- [ ] **Step 3: Commit README update**

Run:

```powershell
git add README.md
git commit -m "Document Divine Burger brand package"
```

Expected: Commit succeeds.

- [ ] **Step 4: Push all commits**

Run:

```powershell
git push
```

Expected: Remote `origin/main` updates successfully.

---

## Self-Review

- Spec coverage: The plan covers the approved character criteria, the D/aura system, gourmet/cinematic style, variants, rejection criteria, prompt production, and scoring.
- Placeholder scan: No open placeholders are present.
- Consistency check: The character is named **Divine Burger** throughout. The direction remains realistic/cinematic and avoids angelito/cartoon territory.
