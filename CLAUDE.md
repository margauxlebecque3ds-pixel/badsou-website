# BADSOU — Design System & Instructions for Claude Code

## Brand Identity
BADSOU is a premium French artisan brand specializing in personalized engraving, 
3D printing and custom souvenirs. Founded by Noam Mauvais, engineer & creator, 
based in Bar-le-Duc, France.
Tagline: "Fabriqué ici, offert partout."

## Aesthetic Direction
**Luxury Dark Atelier** — think high-end Parisian jeweler meets artisan workshop.
- Dark, cinematic, moody
- Gold accents that feel warm and handcrafted, not flashy
- Editorial typography, refined spacing
- Every detail must feel intentional and premium
- NEVER generic, NEVER AI-looking, NEVER cookie-cutter

## Color Palette
```
--gold:        #c9a96e   /* primary accent — warm artisan gold */
--gold-light:  #e8d5a3   /* hover states, highlights */
--gold-glow:   rgba(201, 169, 110, 0.4)  /* glows, shadows */
--bg-primary:  #030102   /* near-black background */
--bg-secondary:#0d0a07   /* slightly lighter sections */
--bg-card:     #120e08   /* product cards */
--text-primary:#f5e6c8   /* warm white for headings */
--text-muted:  rgba(245, 230, 200, 0.55) /* body text */
--border:      rgba(201, 169, 110, 0.2)  /* subtle borders */
```

## Typography
- **Display / Logo**: Pompeii New Light — used for BADSOU wordmark only
- **Headings**: Georgia, serif — elegant, warm, editorial
- **Body**: 'Cormorant Garamond', Georgia, serif — refined, literary
- **Labels / Nav**: letter-spacing: 0.35em, text-transform: uppercase, font-size: 0.7rem
- **Tagline**: italic, Georgia, gold color
- NEVER use: Inter, Roboto, Arial, system-ui, sans-serif for display text

## Logo Usage
- File: `images/logo.png` (white PNG with transparent background)
- To render in gold: 
  `filter: invert(72%) sepia(55%) saturate(500%) hue-rotate(5deg) brightness(1.1)`
- To add glow:
  `drop-shadow(0 0 25px rgba(201,169,110,0.9)) drop-shadow(0 0 50px rgba(201,169,110,0.4))`
- Navbar size: height 40px, width auto
- Hero size: max-width 45% of screen, centered

## Animations — Rules
- **Philosophy**: one well-orchestrated moment > scattered micro-interactions
- **Page load**: staggered fade-in with translateY(20px) → translateY(0)
- **Hover cards**: subtle scale(1.03) + border-color gold, duration 0.3s ease
- **Gold glow pulse**: 3s ease-in-out infinite, never harsh or flashy
- **Scroll reveals**: IntersectionObserver, elements fade in as they enter viewport
- **Transitions**: always ease-out or cubic-bezier(0.25, 0.46, 0.45, 0.94)
- **Duration**: 0.3s for micro, 0.6s for reveals, 3s for ambient loops
- NEVER: jarring, bouncy, or fast-flashing animations
- NEVER: animations that distract from the content

## Layout Principles
- Generous negative space — luxury breathes
- Section padding: min 80px top/bottom
- Max content width: 1200px, centered
- Cards: dark background, 1px gold border (low opacity), border-radius 4px
- Images: object-fit cover, slight dark overlay on hover
- Asymmetry is welcome — don't center everything

## Components

### Navbar
- Fixed top, background: rgba(3,1,2,0.95) with backdrop-filter blur
- Logo left, nav links right
- Links: uppercase, spaced, gold on hover
- Smooth scroll to sections

### Hero
- Fullscreen (100vh)
- Background: images/hero.jpg with overlay rgba(0,0,0,0.55)
- Logo centered with gold filter + glow pulse animation
- Tagline below in gold italic
- Floating gold dust particles (canvas, subtle)

### Product Carousels
- One per category, horizontal scroll
- Center card bigger and highlighted (scale 1.05)
- Each card: product photo + name + gold price badge
- Arrow navigation, smooth slide

### About / Bio Section
- Two-column: photo left, text right
- Photo of Noam with "FONDATEUR" badge
- Text compact, well-spaced paragraphs
- Separator: thin gold horizontal line

### Footer
- Dark background, centered
- Logo, contact info, social links in gold

## Contact Info
- Phone: 06 43 98 39 66
- Email: chez.badsou@gmail.com

## File Structure
```
badsou-site/
├── index.html
├── CLAUDE.md          ← this file
├── images/
│   ├── logo.png       ← white transparent PNG
│   ├── hero.jpg       ← laser engraver cinematic photo
│   ├── noam.jpg       ← portrait of Noam
│   ├── objets-3d/
│   ├── gravures/
│   ├── crystal/
│   ├── personnalises/
│   ├── collectionbarleduc/
│   └── collectionnancy/
└── ressources/        ← reference screenshots (do not display)
```

## What to NEVER do
- Never use purple gradients or blue/white SaaS aesthetics
- Never use generic card shadows (box-shadow: 0 4px 6px rgba(0,0,0,0.1))
- Never use rounded corners > 6px (keeps it refined, not playful)
- Never use bright white backgrounds
- Never use emojis in the UI
- Never center ALL text — mix alignments intentionally
- Never make animations faster than 0.3s or slower than 4s
- Never add unnecessary elements — luxury = restraint
