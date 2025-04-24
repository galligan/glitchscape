# 🎨 Glitchscape Visual Style Guide (v1.2)

> **Retro‑future neon meets cozy pixel platformer** – a CRT day‑dream where brilliant colour, deep parallax and systemic glitches always remind the player that the world itself is *code*.

---

## 1 · North‑Star Vision
Glitchscape feels like booting a self‑aware ‘80s cartridge. Every pixel, shader, and parallax layer reinforces the loop: **repair corruption → restore beauty**.

---

## 2 · Stylistic Pillars
| Pillar | Why it matters | Guard‑rails |
| --- | --- | --- |
| **16‑bit‑plus pixel art** | Nods to SNES/Genesis era; approachable for a family art pipeline | Cap sprite frames ≤ 64 × 64 px; avoid sub‑pixel gradients |
| **Neon cyber‑fantasy lighting** | Synth‑wave glow à la *Narita Boy* | Emissive values ≤ 80 % to keep silhouettes readable |
| **Dynamic 2.5‑D depth** | Layers ala *Dead Cells* & *Ori* sell scale | ≥ 3 parallax bands; use atmospheric colour ramp instead of fog |
| **Readable silhouettes** | *Hollow Knight*‑style outlines | 1‑px keyline; add unique head shapes (see § 6) |
| **Glitch ↔ Restore dichotomy** | Core feedback loop | Paired palettes + CRT / chroma shaders toggle |
| **Progressive emotion palette** | Guides player mood across acts | See § 4.3 for hue‑shift roadmap |

---

## 3 · Inspiration Matrix
| Game | Borrow | Leave / Tweak |
| --- | --- | --- |
| **Narita Boy** | CRT scanlines, techno‑myth iconography | Reduce particle density |
| **Dead Cells** | Normal‑mapped pixels, baked lighting | Remove clutter for younger readability |
| **Ori (WotW)** | Painterly multilayer BGs, volumetric rays | Preserve chunky pixel read |
| **Hyper Light Drifter** | Synth‑wave palette, minimalist HUD | Tone down camera shake |
| **Celeste** | Expressive micro‑animation | Stick to 16‑bit fidelity |
| **Hollow Knight** | DOF layering, thick outlines | Keep neon palette |
| **Tron / Matrix** | Cyan‑magenta grid & falling‑code shaders | Use Matrix green sparingly |

---

## 4 · Colour & Lighting
### 4.1 Global Palette
(unchanged from v1.1 – orange reserved for **Patch**, purple for **Hack**; cyan/magenta/amber support palette.)

### 4.2 State‑Based Shifts
| State | Hue Δ | Sat Δ | Extra Pass |
| --- | --- | --- | --- |
| Glitched | +12° | +20 % | RGB offset 1–2 px + noise overlay |
| Restored | — | −15 % | Bloom & CA off |

### 4.3 Emotional Progression Roadmap
| Narrative Arc | Dominant Hue | Added Accent | Intent |
| --- | --- | --- | --- |
| **Act I – Discovery** | Cyan | Cool violets | Sense of mystery, minimal corruption |
| **Act II – Descent** | Magenta | Dark indigos | Heightened tension, glitch prevalence |
| **Act III – Repair** | Balanced | Orange sparks | Hope resurfaces |
| **Finale – Restoration** | Warm ambers / gold | Soft whites | Triumph & completion |

> **Implementation tip:** Pre‑bake palette LUTs for each act; swapping LUT at level load is cheaper than per‑pixel HSV shifts.

---

## 5 · Environment Blueprint & Storytelling
| Layer | Purpose | Parallax | Story Hooks |
| --- | --- | --- | --- |
| Foreground FX | Sparks, code shards | 1.15 | Immediate glitch debris |
| Gameplay Plane | Colliders & props | 1.00 | Corrupted terminals players can repair |
| Mid‑BG A | Architecture (server towers) | 0.70 | ASCII murals hinting world’s origin |
| Mid‑BG B | Fog, lightshafts | 0.55 | Hidden silhouettes of early NPCs |
| Deep BG | Code nebula | 0.35 | Shows increasing “order” post‑repair |
| Skybox | Data‑void gradient | 0.20 | Amber constellations appear when 100 % restored |

---

## 6 · Character & Animation
### 6.1 Patch (Hero)
* **Sprite:** 32 × 48 px, orange suit `#FF6A28`.
* **Visor:** `#0D0D1A`; two 6 × 6 px eyes.
* **Exclusive silhouette cue:** Rounded helmet, broad gloves.
* **Emotion:** brightness, shape & spacing of eyes.

### 6.2 Hack (Antagonist)
* **Sprite:** 40 × 56 px, purple suit `#9A33FF`.
* **Visor:** narrow red slits.
* **Silhouette cue:** Angular shoulder “antennae”, longer legs.
* **Aura:** violet bloom spikes during attacks.

### 6.3 Shared Guidelines
* 1‑px outline (charcoal); Hack gains 50 % magenta bleed in boss phase 2.
* Hit‑pause: 80 ms + CRT flicker.
* Palette exclusivity enforced by pipeline scripts.

---

## 7 · Camera & Screen FX
| State | Behaviour |
| --- | --- |
| **Glitched** | Occasional 1‑frame stutter every 6–10 s; 2‑px chroma shift ripple on heavy corruption |
| **Restored** | Butter‑smooth ease‑in/out; parallax exaggeration +10 % to reward clarity |

> *Accessibility:* stutter and CA can be disabled in Eye‑Saver preset.

---

## 8 · Transitional “Wave of Restoration”
At the exact moment a node is repaired:
1. Emit radial **white‑to‑amber bloom** (250 ms).
2. Trigger **pal‑swap shader** that sweeps outwards at 400 px/s.
3. Play **“reboot” SFX** (bit‑crush resolves into hi‑fi chime; see § 9).
4. Spawn **data‑fracture reversal particles** that fly back into terrain.

---

## 9 · Audio & Soundscapes
| Aspect | Glitched | Restored |
| --- | --- | --- |
| **Music** | Minor‑key chiptune, 10‑bit sample rate | Full 16‑bit, richer instrumentation |
| **Ambience** | Low‑bit hum, intermittent modem screech | Gentle synth pads, distant fan whirr |
| **UI SFX** | Noise‑gate clicks, skewed pitch | Clean, centred beeps |

> *Tip:* Duck music volume by 3 dB when CRT mask > 80 % opacity to reduce fatigue.

---

## 10 · FX & Shaders
(Original table unchanged **plus** …)
* **Restoration Wave Shader** – radial LUT blend + additive bloom (see § 8).

---

## 11 · Technical Spec Cheat‑Sheet
(unchanged – see v1.1)

---

## 12 · Second‑Order Considerations
* **Visual Fatigue** – Gradually introduce neon & particle density over first 3 stages.
* **Display Variance** – Test CA/bloom across LCD, OLED and Steam Deck IPS; auto‑tune brightness by display resolution.
* **Silhouette Clarity** – Maintain > 4 px colour contrast around sprite perimeters.

---

## 13 · Next Steps
1. Build **vertical slice** validating palette shift & camera stutter.
2. Prototype **Restoration Wave** shader & test on Switch‑class GPU.
3. Export **ASE/ACO palette** and **FMOD event tree** for audio plan.
4. Schedule **family playtest** for silhouette & fatigue feedback.

