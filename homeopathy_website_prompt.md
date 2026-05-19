# MASTER PROMPT: Build a Homeopathy Learning Website

## OVERVIEW

Build a complete, single-file static website (`index.html`) that teaches homeopathy from scratch to practical self-use. The website must be **visually rich, animated, fully interactive**, and structured as a modular learning journey. Use **Bootstrap 5** for layout and UI components, **Chart.js** for data visualizations, and **vanilla JavaScript** for all interactivity.

All content must be organized in the **exact sequence a beginner should learn it** — from history and philosophy through to practical home use.

---

## TECHNICAL REQUIREMENTS

- **Single file**: Everything in one `index.html` (inline CSS in `<style>`, inline JS in `<script>`)
- **Bootstrap 5**: Load via CDN (`https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css`)
- **Chart.js**: Load via CDN (`https://cdn.jsdelivr.net/npm/chart.js`)
- **Animate.css**: Load via CDN for entrance animations
- **Font Awesome 6**: Load via CDN for icons
- **Google Fonts**: Use `Inter` for body, `Playfair Display` for headings
- **No external images** — use CSS gradients, SVG icons, and Unicode symbols for all visuals
- **Fully responsive** — works on mobile and desktop
- **Dark/light mode toggle** in the navbar

---

## DESIGN SYSTEM

```
Color Palette:
  --primary:     #2E7D5B  (deep forest green — homeopathy/nature)
  --secondary:   #7B5EA7  (purple — philosophy/healing)
  --accent:      #E8A838  (amber — highlights/warnings)
  --danger:      #C0392B  (red — stop/emergency)
  --light-bg:    #F5F7F2  (off-white)
  --card-bg:     #FFFFFF
  --text:        #1A2B20
  --muted:       #6B7280

Typography:
  Headings: Playfair Display, serif
  Body: Inter, sans-serif
  Code/remedies: monospace pill badges

Spacing: Bootstrap grid, sections with py-5 padding

Cards: Soft shadow (box-shadow: 0 2px 16px rgba(0,0,0,0.07)), border-radius: 12px

Animations:
  - Section headers: fade-in-up on scroll (use IntersectionObserver)
  - Cards: staggered slide-up on scroll
  - Tabs: smooth fade transition
  - Charts: animated draw-in (Chart.js built-in animation)
  - Progress bar for learning progress (localStorage)
```

---

## SITE STRUCTURE

### NAVBAR (sticky-top)
- Logo: 🌿 **Homeopathy Academy**
- Nav links: History | Principles | Potencies | Materia Medica | Repertory | Case Taking | Miasms | Home Kit
- Right side: 🌙 Dark Mode toggle + 📊 Progress badge showing "X/7 modules complete"

### HERO SECTION
- Large headline: *"Learn Homeopathy — From First Principles to Home Practice"*
- Subtitle: *"A structured, visual, self-paced learning journey through classical homeopathy"*
- Two CTA buttons: [Start Learning →] [View Learning Path]
- Animated learning path roadmap (horizontal stepper with 7 phases, each clickable to scroll to that section)
- Source citation at bottom of hero: Based on curriculum from *Dr. Bhatia's Homeopathy Foundation Course* (academy.doctorbhatia.com), *Alison.com Understanding Homeopathy*, and *The School of Homeopathy* (homeopathyschool.com)

---

## MODULE 1: History & Origins
**ID**: `#module-1`
**Badge**: Phase 1 of 7 | Estimated read: 15 min

### Content:
1. **Timeline visualization** (horizontal scrollable timeline using CSS/JS):
   - 1755: Samuel Hahnemann born in Meissen, Germany
   - 1790: Hahnemann translates Cullen's Materia Medica; discovers cinchona bark experiment
   - 1796: First paper on the Law of Similars published in Hufeland's Journal
   - 1810: *Organon of Medicine* (1st edition) published
   - 1828: *Chronic Diseases* published — miasm theory introduced
   - 1843: Hahnemann dies in Paris; 6th edition of Organon completed but not yet published
   - 1900: James Tyler Kent publishes *Lectures on Homeopathic Philosophy*
   - 1921: Kent's *Repertory* published
   - Today: Practiced in 80+ countries; WHO recognizes as 2nd largest medical system

2. **Key figures card grid** (Bootstrap cards, 3-column):
   - Samuel Hahnemann — Founder, author of Organon
   - James Tyler Kent — Systematized repertory, developed constitutional types
   - Constantine Hering — "Father of American Homeopathy", Hering's Law of Cure
   - William Boericke — Author of *Pocket Manual of Materia Medica* (most used reference)
   - George Vithoulkas — Modern classical homeopathy; E-learning at vithoulkas.edu.gr

3. **Quick quiz** (JS-powered, 3 MCQ questions, shows score on submit):
   - Q: Who founded homeopathy? A: Samuel Hahnemann
   - Q: What year was the Organon first published? A: 1810
   - Q: What experiment led Hahnemann to discover the Law of Similars? A: Cinchona bark (Quinine)

**Sources listed in-section**:
- Organon of Medicine (6th ed.), Hahnemann (available free at homeopathybooks.in)
- *The Complete Homeopathy Handbook*, Miranda Castro (Boiron recommended — boironusa.com/trainings/books-guides)
- *Impossible Cure*, Amy Lansky PhD (resonatehomeopathy.com recommendation)

---

## MODULE 2: Core Principles
**ID**: `#module-2`
**Badge**: Phase 2 of 7 | Estimated read: 20 min

### Content:

1. **Law of Similars (Similia Similibus Curentur)** — interactive flip card:
   - Front: "Like Cures Like"
   - Back: Full explanation with example (Coffea/coffee causes insomnia → treats insomnia; Allium Cepa/onion causes watery eyes → treats hay fever with watery eyes)
   - Source: Organon of Medicine §26

2. **Law of Infinitesimals** — animated dilution diagram:
   - Visual showing 1:100 dilution repeated → C scale
   - Key point: *the more dilute, the more potent* (counterintuitive)
   - Source: Organon §269–271

3. **Vital Force (Dynamis)** — concept card with diagram:
   - Definition: The immaterial, dynamic energy that animates living beings
   - Disease = Vital Force deranged; remedy = restores harmony
   - Source: Organon §9–11

4. **Hering's Law of Cure** — animated 4-step visual:
   - Cure proceeds: from inside → out | from above → downward | from most vital organs → least vital | in reverse order of appearance
   - Named after Constantine Hering
   - Example walkthrough with eczema case

5. **Doctrine of Drug Proving (Proving)** — accordion:
   - Healthy volunteers take a substance
   - Record ALL symptoms produced
   - These symptoms = what that substance CURES in disease
   - First proving: Cinchona bark on Hahnemann himself (1790)

6. **Comparison Table** (Bootstrap table): Homeopathy vs Conventional Medicine vs Ayurveda (3-col)
   - Rows: Basis | Unit of treatment | Disease view | Remedy selection | Side effects

**Sources**:
- Organon of Medicine (§9, §26, §269) — free at homeopathybooks.in
- *Lectures on Homoeopathic Philosophy*, J.T. Kent

---

## MODULE 3: Potencies & Preparations
**ID**: `#module-3`
**Badge**: Phase 3 of 7 | Estimated read: 20 min

### Content:

1. **Potency Scales** — interactive Chart.js bar chart showing dilution ratios:
   - X / D scale: 1:10 dilutions (6X = 10⁻⁶)
   - C / CH scale: 1:100 dilutions (30C = 10⁻⁶⁰)
   - LM / Q scale: 1:50,000 dilutions
   - Chart: X-axis = potency name, Y-axis = dilution factor (log scale)

2. **Potency Selection Guide** — Bootstrap accordion with decision tree logic:
   - **3X–12X / 3C–12C**: Tissue salts, biochemic remedies, organ support. Low potency for clear local symptoms.
   - **30C**: Standard potency for home use. Safe, effective for most acute conditions.
   - **200C**: Constitutional use. Used when 30C fails or for emotional/mental symptoms.
   - **1M**: High potency. Only with clear constitutional picture. Not for self-treatment.
   - Rule of thumb: *Lower potency = repeat more frequently; higher potency = dose less often*

3. **How Remedies Are Made** — step-by-step animated visual (CSS animation):
   - Step 1: Mother tincture (plant in alcohol)
   - Step 2: 1 drop + 99 drops water/alcohol → succuss (vigorous shaking) 10 times = 1C
   - Step 3: 1 drop of 1C + 99 drops → succuss = 2C
   - Step n: Repeat to desired potency
   - For insoluble substances: trituration in lactose for first 3C, then liquid dilution

4. **Remedy forms** — icon card grid:
   - Pillules (small lactose pellets) — most common
   - Tablets
   - Liquid drops (dilution)
   - Mother tincture (Q)
   - Ointments/creams (topical, e.g., Calendula)
   - Biochemic tissue salts (Schuessler's 12 salts)

5. **Interactive potency calculator** (JS):
   - Input: Number of dilutions + scale (X or C)
   - Output: Total dilution factor, suggested use case

**Sources**:
- *Pocket Manual of Homeopathic Materia Medica*, William Boericke (homeomart.com)
- Organon §269–271 (potentization aphorisms)
- oorep.com (free online repertory with potency guidance)

---

## MODULE 4: Materia Medica
**ID**: `#module-4`
**Badge**: Phase 4 of 7 | Estimated read: 40 min

### Content:

1. **What is Materia Medica?** — definition card:
   - The encyclopedic collection of documented remedy symptom-pictures from provings, toxicology, and clinical observation
   - Currently 3000+ substances documented (Synthesis + Complete Repertory)
   - Practical core: ~100–250 polychrest remedies cover 90%+ of cases
   - Source: hpathy.com (Structured Study Guide by Dr. Manish Bhatia)

2. **Polychrests vs Small Remedies** — visual split:
   - Polychrests: broad application, many symptoms, well-proven
   - Small remedies: narrow action, specific presentations
   - Keynote remedies: use one or two "red thread" symptoms to select

3. **The 10 Core Polychrest Remedies** — interactive tabbed card system (one tab per remedy):
   Each tab contains:
   - Remedy name + Latin name + source (plant/mineral/animal)
   - Constitutional profile summary (body type, temperament)
   - Key symptoms (bullet list, 5-7 points)
   - Keynote (the single most distinctive feature)
   - Key modalities (what makes it better/worse)
   - Common conditions treated
   - Differentiation from 1 similar remedy

   **Remedies to include (all 10)**:

   **1. Sulphur** (Sulfur — mineral)
   - Constitutional: Lean or overweight, philosophical, untidy, "ragged philosopher"
   - Keynote: Burning sensations everywhere; heat aggravates; averse to bathing
   - Key symptoms: Skin diseases with intense itching and burning; heat of top of head; 11am hunger; redness of all orifices; hot feet at night (kicks off covers)
   - Modalities: Worse heat, bathing, 11am; Better cool open air
   - Common uses: Eczema, psoriasis, chronic skin disease, constipation; acts as a clearing agent when a well-chosen remedy fails
   - Source: Hpathy.com Polychrest Review (IJCRT2508254)

   **2. Lycopodium Clavatum** (Club Moss — plant)
   - Constitutional: Intellectually keen but physically weak; lacks self-confidence though appears confident; right-sided
   - Keynote: Bloating and flatulence after eating even a little; 4–8 PM aggravation
   - Key symptoms: Craves sweets; worse right side or symptoms move right to left; anticipatory anxiety; bossy at home, timid outside; deep forehead wrinkles
   - Modalities: Worse 4–8 PM, heat, right side; Better warm food, warm drinks, motion
   - Common uses: Digestive disorders, IBS, liver complaints, urinary infections, right-sided complaints

   **3. Calcarea Carbonica** (Oyster shell — mineral)
   - Constitutional: Chubby, fair, flabby; cold and damp; slow but thorough
   - Keynote: Head sweats at night soaking the pillow; craves eggs
   - Key symptoms: Fears disease, going insane, being observed; slow development in children; profuse sweating on head; cold hands and feet but sweats from head; chilly; sour discharges
   - Modalities: Worse cold, wet, exertion, full moon; Better dry weather, lying on painful side
   - Common uses: Teething problems, growing pains, anxiety, obesity, hypothyroid tendency, nightsweats

   **4. Natrum Muriaticum** (Common salt — mineral)
   - Constitutional: Reserved, closed, grief-holding; introvert; thin but eats well
   - Keynote: Cannot cry in front of others; worse consolation (gets angry if pitied)
   - Key symptoms: Grief that cannot be expressed; craves salt; oily skin with dry hairline; headache like hammers; alternating constipation and diarrhea; hates being in the sun; geographic tongue
   - Modalities: Worse sea air, sun, consolation, 10am; Better open air, cold bathing, fasting
   - Common uses: Depression, grief, migraines, herpes, skin conditions, eating disorders

   **5. Pulsatilla** (Wind flower — plant)
   - Constitutional: Gentle, mild, yielding, weepy; changeable
   - Keynote: Symptoms constantly change; craves open air; thirstless even with fever
   - Key symptoms: Weeps easily; seeks comfort; wandering pains; discharges thick, yellow-green and bland; worse in warm room; better in open air; clings, wants attention
   - Modalities: Worse warmth, rich food, evenings; Better open air, cold applications, gentle motion, consolation
   - Common uses: Colds with yellow-green discharge, ear infections, hormonal irregularities, PMS, childhood complaints

   **6. Nux Vomica** (Poison nut — plant)
   - Constitutional: Ambitious, driven, irritable; Type-A personality; overindulgent
   - Keynote: Over-sensitive to all stimuli (light, noise, smell, criticism); wakes 3am with mental activity
   - Key symptoms: Digestive complaints from overindulgence; constipation with constant urge; chilly; very irritable mornings; worse from coffee, alcohol, spices
   - Modalities: Worse early morning, cold, stimulants, overwork; Better warmth, rest, evening
   - Common uses: Hangover, IBS, constipation, insomnia, office stress, digestive upset from overeating

   **7. Arsenicum Album** (White arsenic — mineral)
   - Constitutional: Fastidious, anxious about health; perfectionist; restless; fears death and disease
   - Keynote: Restlessness with exhaustion; midnight to 2am aggravation; burning pains better by heat
   - Key symptoms: Great anxiety and restlessness; burning sensations relieved by heat; very chilly; cannot bear disorder; thirst for sips of water; prostration out of proportion to illness
   - Modalities: Worse midnight–2am, cold, cold food; Better warmth, hot drinks, company
   - Common uses: Food poisoning, anxiety, asthma (worse midnight), flu with restlessness, skin eruptions that burn

   **8. Phosphorus** (Phosphorus — mineral)
   - Constitutional: Tall, lean, artistic, affectionate, extroverted; craves company; bright and sparkly
   - Keynote: Craves cold drinks (vomited when it gets warm in stomach); fears alone/dark/thunderstorms
   - Key symptoms: Burning pains; haemorrhagic tendency (bleeds easily, bright red blood); great affection — wants to be held; fears dark, ghosts, disease; sympathetic to others; cravings for salt, spice, cold drinks
   - Modalities: Worse evenings, lying on left side, cold air, alone; Better cold food/drinks, company, massage, sleep
   - Common uses: Bronchitis, coughs, nosebleeds, anxiety, liver complaints, haemorrhage

   **9. Ignatia Amara** (St. Ignatius bean — plant)
   - Constitutional: Sensitive, idealistic, romantic; grief or disappointment leads to physical symptoms
   - Keynote: Contradictory symptoms (lump in throat better swallowing solids; fever without thirst); involuntary sighing
   - Key symptoms: Grief, disappointment, loss leading to physical complaints; lump in throat; involuntary sighing; contradictory symptoms; cramping pains; suppressed weeping
   - Modalities: Worse grief, consolation, tobacco, coffee; Better change of position, eating, urinating
   - Common uses: Acute grief, bereavement, performance anxiety, IBS from emotions, hysterical conditions

   **10. Sepia** (Cuttlefish ink — animal)
   - Constitutional: Worn-out woman; indifferent to loved ones; sarcastic; craves solitude
   - Keynote: Bearing-down sensation as if pelvic organs will prolapse; better vigorous exercise (dancing)
   - Key symptoms: Indifference to husband, children, family; sadness, irritability; hot flushes; yellow saddle across nose; aversion to sex; bearing-down in pelvis; loves to dance but too tired
   - Modalities: Worse cold, before periods, morning, consolation; Better vigorous exercise, warmth, fasting
   - Common uses: PMS, menopause, post-partum depression, prolapse, thyroid issues, indifference states

   Source for all 10: IJCRT Polychrest Review (ijcrt.org/papers/IJCRT2508254.pdf), Kent's Materia Medica (materiamedica.info), hpathy.com Structured Study Guide

4. **First Aid Remedy Quick-Reference** — searchable table (JS filter by symptom):
   | Remedy | Key Condition | Keynote |
   |--------|--------------|---------|
   | Arnica Montana | Injuries, bruises, shock | "I'm fine, don't touch me" |
   | Aconite | Sudden fever, shock, fright | After exposure to cold/fright; midnight fear |
   | Belladonna | High fever, sudden inflammation | Redness, heat, throbbing, sudden onset |
   | Calendula | Wounds, cuts, infected skin | Promotes healing, prevents sepsis |
   | Apis Mellifica | Bee sting, allergic swelling | Puffy, rosy, stinging, better cold |
   | Cantharis | Burns, UTI with burning | Intense burning before/during/after urination |
   | Rhus Tox | Joint pain, sprains, skin | Worse first motion, better continued motion |
   | Bryonia | Dry, stitching pain | Worse any motion; wants to lie still |
   | Hypericum | Nerve injuries, puncture wounds | Nerve pain shooting upward |
   | Ledum | Puncture wounds, insect bites | Cold applications relieve |
   | Chamomilla | Teething children; unbearable pain | Child demands things, throws them away; one cheek red |
   | Gelsemium | Flu, anticipatory anxiety | Weak, trembling, drowsy; no thirst with fever |

5. **Study sequence guide** (numbered steps with book icons):
   - Start with Nash's *Leaders in Homeopathic Therapeutics* (200 remedies, beginner-friendly)
   - Then Boericke's *Pocket Manual* for broader reference
   - Then Kent's *Lectures on Homoeopathic Materia Medica*
   - Online free resource: homeopathybooks.in (classic texts, free PDF)
   - Online reference: hpathy.com (Materia Medica database with provings)

---

## MODULE 5: Repertory
**ID**: `#module-5`
**Badge**: Phase 5 of 7 | Estimated read: 25 min

### Content:

1. **What is the Repertory?** — definition + analogy card:
   - A massive indexed database of symptoms → remedies
   - Like a reverse dictionary: you look up the symptom, not the remedy
   - Kent's Repertory: 37 chapters, 647 pages, thousands of rubrics
   - Source: oorep.com (free online Kent's Repertory)

2. **Structure of Kent's Repertory** — interactive visual:
   Chapters listed as clickable accordion with example rubrics:
   Mind → Head → Eyes → Ears → Nose → Face → Mouth → Throat → Stomach → Abdomen → Rectum → Urinary → Genitalia → Respiration → Chest → Back → Limbs → Sleep → Chill → Fever → Perspiration → Skin → Generals

3. **Remedy Grading** — visual legend (color coded):
   - Bold / Grade 3: Remedy strongly produces this symptom (e.g., Sulph, Lyc, Calc)
   - Italic / Grade 2: Remedy moderately produces this symptom
   - Plain / Grade 1: Remedy mildly produces this symptom
   Show example rubric with the three grades visually represented

4. **How to Repertorize — Step-by-step** (numbered card sequence):
   - Step 1: Take a complete case (all symptoms with modalities)
   - Step 2: Evaluate symptoms — Mental > General > Particular in weight
   - Step 3: Translate symptoms into "repertory language" (rubrics)
   - Step 4: Find each rubric in the Repertory
   - Step 5: Note which remedies appear in ALL or most rubrics
   - Step 6: Cross-reference top remedies with Materia Medica
   - Step 7: Select the remedy with closest total picture

5. **Interactive mini-repertorization demo** (JavaScript):
   - Present a simple case: "Patient has fever, thirstless, weepy, better in open air, changeable symptoms"
   - User clicks rubrics: [Thirstless] [Changeable symptoms] [Better open air] [Weeping tendency]
   - JS tallies remedies mentioned in each rubric (hardcoded data)
   - Shows result: Pulsatilla emerges as top remedy
   - Teaches the logic of repertorization interactively

6. **Major Repertories Comparison** — Bootstrap table:
   | Repertory | Author | Year | Rubrics | Best For |
   |-----------|--------|------|---------|----------|
   | Kent's Repertory | J.T. Kent | 1897 | ~7,000 | Classical homeopathy; mental symptoms |
   | Boger-Boenninghausen | Boger | 1905 | ~5,000 | Pathological prescribing |
   | Murphy's Repertory | Robin Murphy | 2005 | ~65,000 | Modern; clinically organized; beginners |
   | Synthesis | Schroyens | 1993 | ~300,000 | Comprehensive digital use |
   | Complete Repertory | van Zandvoort | 1994 | ~290,000 | Most comprehensive |

   Free access: **oorep.com** (Kent's online), **homeoint.org/books/kentrep** (full text)

**Sources**:
- Kent's Repertory — free at homeoint.org/books/kentrep
- oorep.com — free online repertory tool
- hpathy.com (Dr. Bhatia's Foundation Course content)

---

## MODULE 6: Case Taking
**ID**: `#module-6`
**Badge**: Phase 6 of 7 | Estimated read: 25 min

### Content:

1. **Complete Symptom Formula** — visual card (4 quadrants):
   Location + Sensation + Modality + Concomitant = Complete Symptom
   - Location: Where exactly? (right side? below knee? inside the ear?)
   - Sensation: What does it feel like? (burning, stabbing, aching, pressing, pulsating)
   - Modality: What makes it better or worse? (time, weather, motion, food, position)
   - Concomitant: What else occurs simultaneously? (headache with nausea; fever with thirst)

2. **Symptom Hierarchy** — vertical bar diagram (most → least important):
   1. Strange, Rare, Peculiar (PQRS) symptoms — most weight
   2. Mental/emotional symptoms
   3. General symptoms (whole-person — temperature preference, food cravings, perspiration)
   4. Particular symptoms (local, organ-specific)

3. **PQRS — Strange Rare Peculiar Symptoms** — accordion with examples:
   - "Thirstless with high fever" → normally fever = thirst → this is PQRS
   - "Symptoms better from hot applications, but the person is chilly" → contradictory
   - "Headache better when lying in the dark and pressing the head" → distinctive modality
   - These are gold — they narrow the remedy field dramatically
   - Source: Organon §153

4. **Key Modality Categories** — visual grid (icons):
   - Time: Morning, evening, midnight, 4–8pm, periodically
   - Temperature: Worse heat / worse cold / worse change of temperature
   - Weather: Worse in damp, worse in wind, worse thunderstorm
   - Motion: Worse motion (Bryonia) vs. better motion (Rhus Tox)
   - Position: Worse lying, worse standing, better sitting
   - Food: Cravings and aversions (general and local)
   - Mental state: Worse anxiety, worse grief, better company

5. **Interactive Case-Taking Template** (fillable HTML form):
   - Chief complaint text area
   - Onset (sudden/gradual dropdown)
   - Sensation (descriptive text)
   - Location (checkboxes: right/left/bilateral/alternating)
   - Modality inputs (better/worse fields)
   - Concomitants text area
   - Mental state field
   - Generals section (thermal sensitivity, thirst, appetite, sleep, perspiration)
   - Submit → Generates a structured case summary as text (JS)

6. **Common Case-Taking Mistakes** — warning cards:
   - Over-emphasis on diagnosis labels (homeopathy treats the person, not the disease name)
   - Ignoring mental/emotional symptoms
   - Missing modalities (the most differentiating feature)
   - Using leading questions

**Sources**:
- *The Complete Homeopathy Handbook*, Miranda Castro (boironusa.com recommendation)
- Organon §§149–153 (on characteristic symptoms)
- *Lectures on Homoeopathic Philosophy*, J.T. Kent

---

## MODULE 7: Miasms & Chronic Disease
**ID**: `#module-7`
**Badge**: Phase 7 of 7 | Estimated read: 30 min

### Content:

1. **What is a Miasm?** — definition card:
   - A fundamental predisposition or underlying disease tendency that perpetuates illness
   - Hahnemann's theory in *Chronic Diseases* (1828) to explain why acute remedies fail long-term
   - Think of it as an inherited "disease soil" that makes certain types of illness recur
   - Source: *Chronic Diseases*, Hahnemann

2. **The Three Primary Miasms** — three large illustrated cards (distinct colors per miasm):

   **Psora** (Primary miasm — deficiency)
   - Origin: Suppressed scabies (Hahnemann's theory)
   - Theme: Lack, deficiency, under-function, poverty consciousness
   - Expression: Skin conditions (especially dry, itchy), functional disorders, chronic fatigue, anxiety
   - Typical complaints: Eczema, psoriasis, IBS, chronic fatigue, hypersensitivity, mental anxiety
   - Anti-miasmatic remedies: Sulphur, Calcarea Carbonica, Lycopodium, Psorinum (nosode)
   - Covers approximately 80% of chronic diseases (Hahnemann's estimate)

   **Sycosis** (Second miasm — excess)
   - Origin: Suppressed gonorrhea
   - Theme: Excess, overflow, over-production, secrecy, fixity
   - Expression: Overgrowth (warts, cysts, fibroids, tumors); excess secretions; fixed ideas; addictions
   - Typical complaints: Warts, condylomata, ovarian cysts, PCOS, fibroids, joint diseases, asthma, OCD tendency
   - Anti-miasmatic remedies: Thuja, Medorrhinum (nosode), Natrum Sulph, Causticum

   **Syphilinum** (Third miasm — destruction)
   - Origin: Suppressed syphilis
   - Theme: Destruction, ulceration, degeneration, nihilism
   - Expression: Ulcers, bone destruction, mental disturbances, self-destructive tendencies
   - Typical complaints: Ulcerations, bone pains at night, suicidal thoughts, progressive neurological disease, alcoholism
   - Anti-miasmatic remedies: Mercury, Syphilinum (nosode), Kali Iod, Aurum Metallicum

3. **Tubercular Miasm** (later addition by Kent and others) — additional card:
   - Theme: Restlessness, longing for change, romanticism about death, rapid breakdown
   - Expression: Respiratory diseases, allergies, recurring infections, hyperactivity in children, desire to travel
   - Remedies: Tuberculinum (nosode), Drosera, Phosphorus, Calcarea Phosphorica

4. **Miasm Identification Chart** (Chart.js radar/spider chart):
   - Axes: Skin expression | Mental theme | Discharge type | Thermal state | Structural tendency
   - Three overlapping radar shapes for Psora / Sycosis / Syphilinum (color-coded)
   - Interactive: hover over each axis to see characteristics

5. **Nosodes** — explanation section:
   - Remedies made from diseased tissue or secretions
   - Used to address miasmatic background when well-chosen remedies plateau
   - Key nosodes: Psorinum, Medorrhinum, Syphilinum, Tuberculinum, Carcinosin
   - Note: Nosodes are typically prescribed by trained homeopaths, not for self-use

6. **Hering's Law of Cure — reverse of disease progression**:
   Visual timeline showing how cure unfolds:
   - Symptoms move from vital organs → periphery (inside out)
   - From head → downward (above → below)
   - Old symptoms re-appear briefly then disappear (reverse chronological order)
   - This is a GOOD sign — indicates true cure

**Sources**:
- *Chronic Diseases*, Hahnemann (free at homeopathybooks.in)
- Lotus Health Institute curriculum — Miasms and Immunity course (lotushealthinstitute.com)
- hpathy.com miasm articles

---

## MODULE 8: Home Kit & Practical Self-Help
**ID**: `#module-8`
**Badge**: Practical Reference

### Content:

1. **Essential Home Kit — 35 Remedies** (Bootstrap card grid with search filter):
   Display each remedy as a card with:
   - Remedy name (abbreviation + full Latin name)
   - Source (plant/mineral/animal badge)
   - Top 3 uses
   - Potency: 30C for all acute home-use

   Remedies to include:
   Arnica, Aconite, Belladonna, Apis, Arsenicum, Bryonia, Calcarea Carb, Calendula, Cantharis, Carbo Veg, Chamomilla, China, Colocynthis, Drosera, Euphrasia, Ferrum Phos, Gelsemium, Hepar Sulph, Hypericum, Ignatia, Ipecac, Kali Bich, Ledum, Lycopodium, Mag Phos, Mercurius, Natrum Mur, Nux Vomica, Pulsatilla, Rhus Tox, Ruta Grav, Sepia, Silica, Sulphur, Thuja

2. **Potency Selection Decision Tree** (interactive JS flowchart):
   Start: "Is the condition acute or chronic?"
   → Acute → "How severe?" → Mild → 6C | Moderate → 30C | Severe/quick onset → 200C
   → Chronic → "Have you used 30C already?" → No → Start 30C → Yes → See a homeopath

3. **Dosage Rules** — numbered list with visual chips:
   - Rule 1: One remedy at a time (classical homeopathy)
   - Rule 2: Minimum dose — give the least possible to stimulate a response
   - Rule 3: Standard dose: 2–4 pillules under the tongue, let dissolve
   - Rule 4: Stop the remedy when better; repeat only if symptoms return
   - Rule 5: If no change in 48 hours (acute) or 4 weeks (chronic), reassess the remedy
   - Rule 6: Avoid coffee, mint, camphor, strong essential oils, and steroids (may antidote remedies)
   - Rule 7: Handle pillules with clean, dry hands; avoid touching

4. **Common Conditions Quick Reference** — tabbed section (tab per condition category):

   **Tab 1: Injuries & First Aid**
   | Condition | First Choice | If no response |
   |-----------|-------------|----------------|
   | Bruising, shock after injury | Arnica 30C | Ledum if joint |
   | Cuts, open wounds | Calendula (topical + 30C oral) | Hypericum if nerve-rich area |
   | Sprains | Arnica then Rhus Tox | Ruta if tendons/ligaments |
   | Burns | Cantharis 30C | Urtica Urens if superficial |
   | Puncture wounds | Ledum 30C | Hypericum if nerve pain |
   | Bee/wasp sting | Apis 30C | Seek emergency care for anaphylaxis |

   **Tab 2: Fever & Infections**
   | Condition | First Choice | Keynote to confirm |
   |-----------|-------------|------------------|
   | Sudden high fever | Aconite 30C | After cold/fright, anxious, midnight |
   | High fever, red face | Belladonna 30C | Throbbing, glassy eyes, hot and dry |
   | Flu with weakness | Gelsemium 30C | Weak, drowsy, trembling, no thirst |
   | Slow fever, no thirst | Pulsatilla 30C | Changeable, wants open air |
   | Restless, burning | Arsenicum 30C | Better warmth, midnight aggravation |
   | Cold with yellow-green mucus | Kali Bich 30C | Thick, stringy, tough mucus |

   **Tab 3: Digestive Issues**
   | Condition | First Choice | Keynote |
   |-----------|-------------|---------|
   | Overeating, hangover | Nux Vomica 30C | Chilly, irritable, craves stimulants |
   | Food poisoning (burning) | Arsenicum 30C | Restless, burning, better warmth |
   | Food poisoning (vomiting/diarrhea) | China 30C | Exhausted, flatulence, weakness |
   | Colic, cramping | Colocynthis 30C | Doubling up with pain, better pressure |
   | Colic in infants | Chamomilla 30C | Screaming, cannot bear pain, one cheek red |
   | Heartburn, gas | Carbo Veg 30C | Bloating, belching, coldness |

   **Tab 4: Anxiety & Emotions**
   | Condition | First Choice | Keynote |
   |-----------|-------------|---------|
   | Acute grief/loss | Ignatia 30C | Sobbing, lump in throat, sighing |
   | Anticipatory anxiety (exam/event) | Gelsemium 30C | Trembling, weakness, diarrhea |
   | Panic attacks | Aconite 30C | Sudden intense fear of death |
   | Burnout, overwork | Nux Vomica 30C | Driven, chilly, digestive symptoms |
   | Prolonged grief | Natrum Mur 30C | Silent grief, cannot cry with others |

5. **When NOT to Self-Treat — Emergency Red Flags** — red alert cards:
   - Chest pain or pressure (cardiac emergency)
   - Difficulty breathing
   - High fever above 104°F (40°C) that will not come down
   - Stiff neck with fever (meningitis risk)
   - Sudden severe headache ("worst of my life")
   - Loss of consciousness or confusion
   - Suspected fracture
   - Symptoms in infants under 3 months
   - Any rapidly worsening condition
   - Symptoms that do not improve within 48 hours with correct remedy

   **Message**: In any emergency, call for medical help first. Homeopathy can be used alongside emergency care, but never instead of it.

6. **Remedy Storage & Handling** — tips card:
   - Store in a cool, dry place away from sunlight
   - Keep away from strong smells (essential oils, camphor, eucalyptus)
   - Do not store near strong electromagnetic fields (traditional guidance)
   - Shelf life: Indefinite if stored correctly
   - Label all remedies clearly with name and potency

7. **Recommended Resources** — final curated resource list (cards with links):

   **Free Online Resources**:
   - hpathy.com — Largest free homeopathy database (articles, Materia Medica, repertory)
   - homeopathybooks.in — Free PDF downloads of classic texts
   - oorep.com — Free online Kent's Repertory
   - homeoint.org — Classic homeopathic texts digitized
   - alison.com — Free "Understanding Homeopathy" course (CPD certified)
   - academy.doctorbhatia.com — Foundation Course (60+ units, 20,000+ students)

   **Essential Books** (in reading order):
   1. *The Complete Homeopathy Handbook* — Miranda Castro (best for home prescribers; boironusa.com recommended)
   2. *Homeopathy: Start Here* — Ann Jerome (beginners, accessible)
   3. *Impossible Cure* — Amy Lansky PhD (inspiring introduction + case stories)
   4. *Leaders in Homeopathic Therapeutics* — E.B. Nash (best first Materia Medica for beginners)
   5. *Pocket Manual of Materia Medica* — William Boericke (standard reference)
   6. *Organon of Medicine* (6th ed.) — Hahnemann (translated by Wenda O'Reilly for readability)
   7. *Lectures on Homoeopathic Philosophy* — J.T. Kent (after the above)

   **Professional Courses** (for deeper learning):
   - School of Homeopathy — homeopathyschool.com (UK, online + correspondence)
   - Vithoulkas E-Learning — vithoulkas.edu.gr (classical homeopathy, 10-day free trial)
   - Lotus Health Institute — lotushealthinstitute.com (500+ hour clinical certificate program)

---

## SITE-WIDE FEATURES (implement with JavaScript)

### 1. Learning Progress Tracker
- localStorage-based: mark each module as "complete" with a checkbox/button at the bottom of each module section
- Navbar badge updates: "3/7 complete"
- Hero progress bar updates dynamically
- Persist across page refreshes

### 2. Global Remedy Search
- Fixed search button (bottom-right corner, search icon)
- Click opens a modal with a search input
- Searches across ALL remedy names, conditions, and symptoms mentioned in the site
- Returns matching cards/sections with jump links

### 3. Dark Mode Toggle
- Toggle between light and dark theme
- Persist in localStorage
- Adjust all custom CSS variables for dark mode:
  ```css
  [data-theme="dark"] {
    --light-bg: #1A2B20;
    --card-bg: #243330;
    --text: #E8F0E8;
    --muted: #9CA3AF;
  }
  ```

### 4. Scroll-based Section Animations
- Use IntersectionObserver API
- Cards fade in with stagger effect as they enter viewport
- Section headings slide in from left

### 5. Back to Top Button
- Appears after scrolling 400px
- Smooth scroll to top

### 6. Floating Study Tips
- Small dismissible toast notifications at different points:
  - After Module 2: "Tip: Read Organon §26 for the full Law of Similars explanation"
  - After Module 4: "Tip: Print the polychrest table as a quick reference card"
  - After Module 5: "Tip: Practice repertorizing at oorep.com"

### 7. Print / PDF Ready Styles
- @media print CSS: hide navbar, hide dark mode toggle, print each module cleanly

---

## CHARTS TO IMPLEMENT WITH CHART.JS

1. **Module 3**: Bar chart — Dilution scale comparison (X vs C vs LM potencies, log scale Y-axis)
2. **Module 4**: Horizontal bar chart — Breadth of action for top 10 polychrests (conditions covered)
3. **Module 7**: Radar chart — Miasm comparison (Psora vs Sycosis vs Syphilinum across 5 axes)
4. **Module 8**: Doughnut chart — Remedy category breakdown in a home kit (plant/mineral/animal %)

---

## FOOTER

Three columns:
- Column 1: Logo + tagline + "Based on classical homeopathic literature and verified educational sources"
- Column 2: Quick links to all 8 modules
- Column 3: Key sources with links:
  - academy.doctorbhatia.com
  - homeopathybooks.in
  - hpathy.com
  - oorep.com
  - alison.com/course/understanding-homeopathy
  - lotushealthinstitute.com
  - vithoulkas.edu.gr
  - boironusa.com/trainings/books-guides

**Disclaimer** (prominent, bottom of footer):
"This website is for educational purposes only. Homeopathy is a complementary system of medicine. Nothing on this site constitutes medical advice. Always consult a qualified healthcare professional for any health condition, especially in emergencies, for children, during pregnancy, or for any serious or chronic illness."

---

## IMPLEMENTATION NOTES FOR THE LLM

- Build the entire site as **one complete `index.html` file**
- Use Bootstrap grid throughout: container > row > col-*
- All JavaScript inline at bottom of `<body>` in a single `<script>` block
- All custom CSS in a single `<style>` block in `<head>`
- Start with the navbar and hero, then each module as a `<section>` with matching `id`
- Load all CDN libraries before your `<style>` and `<script>` blocks
- The interactive mini-repertorization demo (Module 5) must use hardcoded rubric-to-remedy data in JS
- The case-taking form (Module 6) must generate a formatted text summary on submit using JS only (no backend)
- For the remedy search modal, index all remedy names and conditions in a JS array on page load
- Test that ALL anchor links from the navbar and roadmap stepper scroll correctly to their sections
- Use smooth-scroll behavior via CSS: `html { scroll-behavior: smooth; }`
- Ensure all cards have `role="article"` and headings follow H1 > H2 > H3 hierarchy for accessibility
- All Chart.js charts must be inside a `<div style="position:relative; height:300px">` wrapper to control height

---

*Prompt compiled from research across: academy.doctorbhatia.com, hpathy.com, alison.com, homeopathybooks.in, lotushealthinstitute.com, vithoulkas.edu.gr, boironusa.com, homeoint.org, oorep.com, ijcrt.org, materiamedica.info, and classical homeopathic literature including Hahnemann's Organon and Chronic Diseases, Kent's Materia Medica and Repertory, and Boericke's Pocket Manual.*
