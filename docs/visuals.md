# Visual Aesthetic

## Table of Contents
- [Stylistic Pillars](#stylistic-pillars)
- [State-Based Visual Shifts](#state-based-visual-shifts)
- [Emotional Progression Through Color](#emotional-progression-through-color)
- [Transitional "Wave of Restoration"](#transitional-wave-of-restoration)
- [Glitch Persistence](#glitch-persistence)

## Stylistic Pillars

| Pillar | Description | Implementation |
|--------|-------------|----------------|
| **16-bit-plus pixel art** | SNES/Genesis era aesthetic with modern enhancements | 320×180 internal resolution; sprites capped at 64×64 px; modern lighting effects |
| **Neon cyber-fantasy lighting** | Vibrant, glowing highlights against darker backgrounds | Emissive values ≤ 80% for readability; orange/purple reserved for protagonists |
| **Dynamic 2.5D depth** | Multilayered parallax creating sense of scale | ≥ 3 parallax bands per scene; atmospheric color ramping |
| **Readable silhouettes** | Clear character outlines ensuring gameplay clarity | 1-px keyline outlines; distinctive head shapes and proportions |
| **Glitch ↔ Restore dichotomy** | Visual contrast between corrupted and fixed states | Paired palettes; shader toggles; particle density shifts |

## State-Based Visual Shifts

| State | Visual Characteristics | Audio Effects |
|-------|------------------------|---------------|
| **Glitched** | RGB offset, noise overlay, increased saturation, occasional frame stutter, CRT scanlines | Bit-crushed audio, minor-key themes, modem screeches, noise-gate clicks |
| **Restored** | Clean palette, reduced saturation, smooth framerate, bloom effects | Full 16-bit audio, richer instrumentation, ambient synth pads, clean UI sounds |

## Emotional Progression Through Color

| Narrative Phase | Dominant Palette | Intent |
|-----------------|------------------|--------|
| **Act I – Discovery** | Cyan-dominant with cool violets | Mystery, beginnings, minimal corruption |
| **Act II – Descent** | Magenta-dominant with dark indigos | Rising tension, increasing glitch prevalence |
| **Act III – Repair** | Balanced spectrum with orange accents | Hope resurfaces, balance returning |
| **Finale – Restoration** | Warm ambers/gold with soft whites | Triumph, completion, harmony |

## Transitional "Wave of Restoration"

When a major corruption node is cleared:
1. White-to-amber radial bloom emanates from the node (250ms)
2. Palette-swap shader sweeps outward at 400px/s
3. Audio transitions from bit-crushed to hi-fi
4. Particle effects show data fragments returning to proper position
5. Background elements shift from chaotic to ordered patterns

## Glitch Persistence

Even after full restoration, worlds retain subtle "scars" of their previous corruption:
- Faint circuit patterns occasionally visible on natural surfaces
- Brief moments of code visibility during specific interactions
- Minor visual glitches in background elements
- Harmonious integration of digital and natural elements
- These elements serve as reminders of the world's history and evolution rather than flaws 