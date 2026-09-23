# ABYSS visual + choreography spec

## Visual language
- Deep-water palette: `#061015`, `#0B2028`, `#124653`, `#76D6D2`, `#F2F5F3`.
- Instrument Sans for primary UI/headlines, Inter for body copy, JetBrains Mono for technical labels.
- Minimal borders, restrained glass surfaces, large editorial typography, generous negative space.
- Glass is reserved for navigation, dropdowns, and one cinematic quote surface.

## Choreography
1. Hero: full-viewport ocean footage; oversized statement; tiny pointer depth shift; nav is visually transparent at the top.
2. Navigation: hides on downward scroll, returns in a translucent glass pill on upward scroll, and loses the glass surface again at the hero.
3. Logo: original ABYSS symbol performs a controlled 360° spin on hover.
4. Hero-to-editorial bridge: short color-gradient bridge makes the video color feel continuous into the light section.
5. Media story: three media states map directly to three text states; right column is pinned on desktop; clicking a `+` opens the state and smoothly scrolls to its media.
6. Media transition: active media receives a restrained scale/blur treatment plus a single circular mask reveal instead of a hard swap.
7. Mobile: the media story interleaves video and text; sticky behavior and pointer-only effects are removed/reduced; tap targets are enlarged.
8. Pipeline: active project gets a subtle ambient tint and lift, preserving the editorial left/right split.
9. Quote: full-bleed ocean footage with a translucent quote surface using opposing depth cues.
10. Footer: deep-water gradient with a slow independent background drift behind the fixed left statement and naturally scrolling links.

## Media behavior
- Videos are lazy-loaded with `IntersectionObserver`.
- On touch/mobile, decorative canvas fallbacks are frozen to reduce CPU load; real video carries the motion.
- Reduced-motion users receive a simplified static presentation.
