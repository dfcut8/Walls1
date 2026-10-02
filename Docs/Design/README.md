# Walls — iOS 27 UI mockups

Version 1 · October 2, 2026 · Working app name: Walls

An artwork-first wallpaper browser with quiet typography, generous images, and floating Liquid Glass controls. The four requested categories are Characters, Landscapes, Nature, and Games. The initial design uses light appearance; the immersive preview uses controls suited to a dark photographic background.

## Screens

| File | Purpose |
| --- | --- |
| [01-discover-light.png](Mockups/01-discover-light.png) | Featured wallpaper and fresh recommendations |
| [02-categories-light.png](Mockups/02-categories-light.png) | Four visual category entry points |
| [03-landscapes-light.png](Mockups/03-landscapes-light.png) | Representative category gallery with sorting |
| [04-wallpaper-preview.png](Mockups/04-wallpaper-preview.png) | Immersive artwork, favorite, share, and Save Image actions |

Open [index.html](index.html) to compare the screens together.

## Navigation and behavior

Three persistent top-level destinations: Discover, Categories, Favorites. Categories opens the corresponding gallery. The category gallery retains the Categories selection; back returns to the category overview. All four categories share this gallery layout. A wallpaper opens a full-screen modal preview; closing it restores the previous gallery and scroll position.

Search opens native search from Discover or Categories. Latest opens a native sorting menu. Favorite toggles membership in Favorites, with an accessible selected state. Share opens the system share sheet. Save Image exports the artwork to Photos; the user then sets their wallpaper in Photos. Only report success after the save completes. Any required Photos access is requested when the user invokes saving.

Favorites, search results, sort menu, permission/error/success states, and alternate appearance screens are follow-up designs; their destinations/actions are represented here without separate mockups.

## Design intent

- Use system typography, semantic colors, and native SF Symbols in implementation. The raster images approximate these assets.
- Target a compact portrait composition around 402 × 874 points. PNG dimensions are concept exports, not a pixel-exact layout specification. Follow actual device safe areas and system insets.
- Starting tokens: 20-point horizontal margins, 12-point grid spacing, 20–24-point image corners, 34-point large title, 17-point body, 11-point minimum tab labels. Dynamic Type and native layout take priority over fixed values.
- Keep artwork in the content layer. Reserve Liquid Glass for navigation and controls. Prefer native regular glass for readability; use media-overlay treatments only where contrast remains clear.
- Keep tab labels visible, use blue plus a selection shape, and retain the tab bar through pushed category navigation. The full-screen preview is a separate modal context with Close.
- Titles over images require a dark scrim. Avoid unnecessary badges and per-thumbnail controls.

## Accessibility and native validation

These mockups are HIG-informed visual direction, not proof of complete Apple guideline compliance. During implementation, use native iOS 27 components so material behavior responds to the OS. Validate all controls at a minimum 44 × 44-point hit area, safe-area spacing, VoiceOver names/order/selected states, Dynamic Type, contrast over every artwork, and Reduce Transparency, Increase Contrast, and Reduce Motion. Provide semantic opaque fallbacks and adaptive layouts. Test dark appearance, larger accessibility sizes, localization, and multiple devices before sign-off.

Static PNGs cannot demonstrate live glass refraction, scrolling, motion, assistive-technology behavior, or interaction. Generated status bars, icons, typography, and artwork crops are illustrative; the native build must use actual system chrome and a single shared asset per wallpaper. Artwork here is concept content, not a finished downloadable catalog.

## Apple references

Guidance reviewed October 2, 2026:

- [Materials](https://developer.apple.com/design/human-interface-guidelines/materials) — content/control hierarchy and Liquid Glass variants.
- [Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars) — stable destinations, labels, and SF Symbols.
- [Layout](https://developer.apple.com/design/human-interface-guidelines/layout) — hierarchy, margins, and adaptation.
- [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility) — implementation review reference.
- [UI Design Dos and Don’ts](https://developer.apple.com/design/tips/) — touch targets and legibility.
- [Adopting Liquid Glass](https://developer.apple.com/documentation/TechnologyOverviews/adopting-liquid-glass) — native implementation reference.

## Provenance

Created with the built-in image generation tool. Categories established the visual reference for the other screens. Exact generation prompts are recorded in [PROMPTS.md](PROMPTS.md). No application code was changed.
