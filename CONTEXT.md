# Portfolio Project Context

## Owner
**Kishor Chamua** — Senior Product Designer at Microsoft, 11 years of experience in Product/UX Design and Motion/Interaction Design. IIT Delhi alumnus. Building this portfolio for job applications.

## Project Goal
A visually attractive, fast-loading portfolio website that showcases Kishor's design work. Recruiters spend ~30 seconds on a portfolio — the site must make an immediate impression.

## Design Philosophy
- **Minimal yet bold & expressive** — constrained palette, strong color, large type, high contrast
- **Playful & motion-rich** — scroll-triggered animations, horizontal scroll, interactive elements
- **Primary inspiration**: [isadeburgh.com](https://isadeburgh.com), [yucca.co.za](https://yucca.co.za) (fonts & color direction)
- **Original portfolio**: [kishorc.art](https://kishorc.art) (Wix-based, being replaced)

---

## Tech Stack
| Layer | Technology |
|-------|-----------|
| Framework | Next.js 16 (App Router, SSG via `generateStaticParams`) |
| Styling | Tailwind CSS v4 with `@theme inline` design tokens |
| Animation | GSAP + ScrollTrigger (scroll-linked, horizontal scroll, parallax) |
| Smooth Scroll | Lenis |
| Fonts | **Koh Santepheap** (display/headings — organic serif, inspired by yucca.co.za) + **DM Sans** (body — warm, readable) via `next/font/google` |
| Deployment | Static export ready, Vercel-compatible |

## Design Tokens (globals.css)
```
--color-background: #F5F2ED (warm parchment)
--color-foreground: #1D1D1B
--color-accent: #3D5A47 (earthy green, inspired by yucca.co.za)
--color-accent-light: #5B7B6A
--color-muted: #8E918F
--color-border: #DDD9D2
--color-surface: #FDFCFA
--font-sans: DM Sans (body)
--font-display: Koh Santepheap (headings — organic serif)
```

---

## Project Structure

```
src/
├── app/
│   ├── layout.tsx          # Root layout — fonts, Preloader, CustomCursor, ScrollProgress, Navbar, grain overlay
│   ├── page.tsx            # Home — Hero → WorkSection → AboutSnippet → ContactSection
│   ├── globals.css         # Tailwind theme, Lenis, animation helpers
│   ├── about/page.tsx      # About — organic layout, journey timeline, tools, interests
│   ├── contact/page.tsx    # Contact page
│   └── work/[slug]/page.tsx # Dynamic case study routes (SSG)
├── components/
│   ├── hero.tsx            # Mixed filled+outlined typography, floating orbs, GSAP timeline
│   ├── work-section.tsx    # Horizontal scroll pinned section, gradient mesh cards
│   ├── about-snippet.tsx   # Home page — 4 typographic belief statements with project proof
│   ├── contact-section.tsx # Light CTA section with outlined accent text, copy-to-clipboard email
│   ├── case-study-content.tsx # Full case study template (quote, challenge, discovery, process, solution, metrics, impact, reflection, key learning)
│   ├── navbar.tsx          # Sticky nav with scroll blur, mobile menu
│   ├── custom-cursor.tsx   # Dot + morphing follower, data-cursor labels
│   ├── preloader.tsx       # Counter 0→100% entry animation
│   └── scroll-progress.tsx # Fixed accent progress bar
└── lib/
    ├── projects.ts         # All 6 projects with enriched case study data
    └── lenis-provider.tsx  # Lenis smooth scroll wrapper
```

---

## Visual Features Implemented
1. **Custom cursor** — animated dot + morphing follower circle, shows labels from `data-cursor` attribute, hidden on mobile
2. **Grain texture overlay** — SVG feTurbulence noise fixed over entire page
3. **Preloader** — branded counter 0→100%, dark bg, slides up to reveal
4. **Scroll progress** — 3px accent bar at top of page
5. **Outlined/stroke typography** — `WebkitTextStroke` + `WebkitTextFillColor` for mixed filled+outlined headings
6. **Gradient mesh cards** — layered radial gradients + blur blobs per project color
7. **Horizontal scroll** — GSAP ScrollTrigger pinned section for project cards
8. **Floating parallax elements** — scattered decorative elements with scroll-driven motion
9. **Marquee** — rolling tools ticker on about page

---

## Projects (from kishorc.art)

### 1. SMS Organiser (2019) — #4A90D9
AI-powered SMS classification app. Won Microsoft Hackathon 2015, 100K+ downloads, featured as best SMS app in India. Reduced OTP flow from 6 to 2 steps.

### 2. Tech Help — Bing.com (2018) — #7B61FF
Structured tech support answers on Bing. Step-by-step visual framework, multi-solution tabs, carousel. Improved TCX/DSAT/APSAT scores.

### 3. Software Search & Download (2017) — #2ECC71
Safe software discovery on Bing. +5 SBS vs competitor, +21M monthly DSQs. Integrated with Windows OS.

### 4. Routofy (2016) — #E8614D
Visual interactive travel booking. One-click route discovery, slider duration controls, seat availability without external sites.

### 5. Bing Translator (2018) — #F39C12
Visual makeover of translator answer. +5 SBS score. Responsive font scaling, mobile keyboard fix, comprehensive state system.

### 6. Contextual Help on Windows 10 (2017) — #9B59B6
In-context help using device/task context. Conversational search, OS Settings integration. Evolution of Tech Help project.

---

## Personal Details (for About page)
- **Contact**: kishorchamua@outlook.com, WhatsApp +91 9717481197
- **Social**: LinkedIn (/in/kishorchamua/), Instagram (@kishorc_), Facebook (/kishorc87/)
- **Education**: Indian Institute of Technology Delhi (IITD)
- **Interests**: Music (keyboard, guitar, ukulele, Launchpad — has YouTube channel), Photography (human stories & expressions), Videography (inclusiveness & community), Explorer
- **Philosophy**: "A good designed product is the one in which there is nothing left to take away from it."

---

## What's Still Needed
- **Real project images** — all case study and card images are placeholders
- **Profile photo** — placeholder emoji on about page
- **Resume PDF** — `/public/resume.pdf` needs to be added
- **Social link URLs** — LinkedIn/Instagram/Facebook hrefs need verification
- **Mobile testing** — responsive behavior needs thorough testing
- **Performance audit** — GSAP bundle size, image optimization
- **SEO** — meta tags, OG images, structured data
- **Analytics** — tracking integration
- **Dark mode** — not implemented (could be a future enhancement)
- **Case study images** — the original site has screenshots/mockups that should be added

---

## Key Decisions & Rationale
- **Syne + DM Sans fonts** chosen for "lively and organic" feel (user feedback that previous fonts were too generic)
- **Horizontal scroll** for project showcase — matches inspiration site's boldness
- **No dark mode** — warm cream background (#FAFAF9) is intentional for warmth
- **Static generation** — fast loading for recruiter audience
- **GSAP over Framer Motion** — more control over scroll-linked animations and timeline sequencing
- **Tailwind v4** with inline theme — design tokens defined once, used everywhere

## Important Notes for AI Agents
- This is **Next.js 16** — check `node_modules/next/dist/docs/` for any API changes before writing code
- Async params pattern: `params: Promise<{ slug: string }>` (Next.js 16 breaking change)
- Lenis CSS import: use `lenis/dist/lenis.css` (not `lenis/css`)
- The `cursor-none` class on body is intentional — custom cursor replaces default
- `font-display` class applies Syne to any element — use it on all headings
