# Arcsin Engineering

Arcsin Engineering is a startup building stage-first tools for performing musicians — compact hardware, fast software, and everything designed to work under pressure.

## About the Site

This website showcases our products in development:

- **LIMIT-1** – A mobile multieffects unit with iOS companion app
  - JUCE-powered C++ audio processing engine
  - SwiftUI interface with sub‑10ms round-trip latency
  - Physical knobs + touch screen control for stage use
  
Built by a small team of engineers and artists, we build in the open on GitHub.

## Links

- **GitHub**: https://github.com/rawporkchop  
- **Email**: hello@arcsin.engineering (oliveklars@gmail.com)  
- **Site navigation**
  - [About](docs/about.html) – Our mission and values, architecture overview  
  - [Products](docs/products.html) – Current products in development  
  - [Upcoming](docs/upcoming.html) – Development milestones & roadmap  
  - [Community](docs/community.html) – Discussions, issue logs, forum  

## Tech Stack (Web Site)

The website itself is a **static HTML site** with vanilla JavaScript:

- Custom CSS animations and interactions
- Dark/light theme toggle using localStorage
- Responsive design for desktop/tablet/mobile
- Cursor tracking effects
- Intersection Observer–based scroll reveal animations

Assets in `docs/`:
- HTML pages (`*.html`)
- Stylesheet (`styles.css`)
- Fonts (custom TTF/OFF files)  
- Images

### Git Ignore Note

This repo doesn't use a build tool; it's pure static. Consider adding:

```bash
git clean -fdx docs/fonts/*  # remove local font caches if needed
# Add these to .gitignore as appropriate for your workflow:
docs/images/.DS_Store
*.ttc
*.otf.lock
```

---

## LIMIT-1 — The Product

### What It Is

LIMIT‑1 is a hardware multieffects processor paired with an iOS companion app. Load impulse responses, chain AUv3 plugins, and control every parameter from 8 physical knobs — built for the stage, not the studio.

### Key Specs

| Spec | Value |
|------|-------|
| Latency | <10ms round-trip audio |
| Controls | 8 physical knobs (≥88pt targets) |
| Platform | iOS → macOS (Catalyst) → Windows (JUCE backend) |
| Engine | JUCE / C++20 with Objective-C++ bridge |
| Plugin Format | AUv3 (XPC process isolation, live chain reordering) |

### Roadmap Status

**Milestone 2 of 9 complete.** See [upcoming](docs/upcoming.html#milestone-list).

- ✅ **01: C++ Audio Pass‑Through** — AUGraph RemoteIO dry signal  
- 🚧 **02: IR Convolution** — JUCE ConvEngine, .wav loading, normalisation (in progress)  
- ⏳ **03–09**: AUv3 hosting, full bridge layer, UI screens, MIDI, persistence, iPad/macOS layouts, Windows

### Future Concepts

| Project | Status | Description |
|---------|--------|-------------|
| LIMIT‑1 Desktop | Concept | Full macOS app via Catalyst + native Windows build on same C++ DSP |
| IR Library | Research | Curated cabinet impulse responses tagged by speaker type and genre |
| LIMIT‑2 | Concept | Next-gen hardware: USB-C audio I/O, larger form factor for studio/stage portability |

---

## Values & Principles

- **Stage First** – Every design decision tested against one question: does this work at a gig?  
- **Zero Latency** – Sub‑10ms target. We don't compromise on audio responsiveness.  
- **Hardware + Software** – Physical knobs, digital intelligence. The best interface is the one you don't have to look at.  
- **Open Build** – Development happens in public; we document process and failures as much as shipping features.

--- 
