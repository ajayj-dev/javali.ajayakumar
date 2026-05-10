# Futuristic Portfolio Website Specification

## 1. Project Overview

**Project Name:** Ajju Portfolio - AI/ML Developer Portfolio
**Project Type:** Single-page animated portfolio website
**Core Functionality:** Showcase AI/ML developer skills, projects, and services with immersive cyberpunk-futuristic animations
**Target Users:** Potential employers, clients, collaborators, and tech enthusiasts

---

## 2. UI/UX Specification

### 2.1 Layout Structure

**Page Sections (in order):**
1. Preloader (full-screen loading animation)
2. Navigation (sticky header)
3. Hero Section (full viewport height)
4. About Section
5. Projects Section
6. Skills Section
7. Services Section
8. Contact Section
9. Footer

**Grid/Layout:**
- Max container width: 1200px
- Section padding: 100px vertical
- Card grid: CSS Grid with auto-fit, minmax(320px, 1fr)

**Responsive Breakpoints:**
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### 2.2 Visual Design

**Color Palette:**
- Background Primary: #050816 (deep space black)
- Background Secondary: #0a0f1e (dark navy)
- Neon Cyan: #00F5FF (primary accent)
- Neon Purple: #8B5CF6 (secondary accent)
- Neon Pink: #FF4D9D (accent highlight)
- Neon Green: #00FF9D (success states)
- Text Primary: #FFFFFF
- Text Secondary: #A0AEC0
- Glass Background: rgba(255, 255, 255, 0.05)
- Glass Border: rgba(255, 255, 255, 0.1)

**Typography:**
- Headings: 'Orbitron', sans-serif (Google Fonts) - futuristic geometric
- Body: 'Exo 2', sans-serif (Google Fonts) - clean tech readability
- Hero Title: 72px (desktop), 40px (mobile)
- Section Titles: 48px (desktop), 32px (mobile)
- Body Text: 16px
- Small Text: 14px

**Spacing System:**
- Base unit: 8px
- Section gaps: 100px
- Card padding: 32px
- Element margins: 16px / 24px / 32px

**Visual Effects:**
- Glassmorphism: backdrop-filter: blur(20px)
- Neon glow: box-shadow with color spread
- Gradient overlays: linear-gradient with transparency
- Grid pattern background: CSS generated pattern

### 2.3 Components

**Navigation:**
- Fixed position, glass background
- Logo (text-based with glow)
- Nav links: Home, About, Projects, Skills, Services, Contact
- Mobile: hamburger menu with slide-in panel
- Active link: neon underline animation
- Hover: cyan glow effect

**Hero Section:**
- Canvas-based particle animation (custom JS, no external lib)
- Floating geometric shapes (CSS animations)
- Glitch text effect on main name
- Typing animation for role using custom JS
- Two CTA buttons with neon borders and hover fill
- Scroll indicator at bottom (animated chevron)

**About Section:**
- Two-column layout (image left, content right on desktop)
- Profile card with tilt effect (Vanilla Tilt.js from CDN)
- Glassmorphism card with glow border
- Skill bars with animated fill on scroll
- Tech badges with hover glow

**Projects Section:**
- 3-column grid (desktop), 2-col (tablet), 1-col (mobile)
- Cards with tilt effect on hover
- Project image (gradient placeholder with icon)
- Title, description, tech tags
- GitHub and Live Demo buttons with icons
- Hover: scale up + neon glow

**Skills Section:**
- Circular progress indicators (SVG-based)
- Category sections: Languages, Frameworks, Tools, Cloud
- Floating tech icons with hover animation

**Services Section:**
- 3-column grid with icon cards
- Each card: icon, title, description, learn more link
- Hover: lift + glow effect

**Contact Section:**
- Centered form layout
- Floating label inputs
- Social links row
- Submit button with loading state

**Footer:**
- Minimal design
- Social icons with hover effects
- Back to top button
- Copyright text

---

## 3. Functionality Specification

### 3.1 Core Features

**Preloader:**
- Circular loader with rotating border
- Progress indication (optional)
- Fade out on complete (2s duration)

**Scroll Animations:**
- Intersection Observer for reveal on scroll
- Elements fade in + slide up
- Staggered delays for grouped elements

**Navigation:**
- Smooth scroll to sections on click
- Active section highlighting based on scroll position
- Mobile menu toggle

**Mouse Effects:**
- Custom cursor (optional - trailing glow)
- Mouse-follow glow effect on background
- Tilt effect on cards (Vanilla Tilt.js)

**Particle System:**
- Canvas-based floating particles
- Connected by lines when close
- Subtle movement and glow

### 3.2 Animations Specification

**Entrance Animations:**
- Hero text: fade in + scale (staggered)
- Navigation: slide down
- Sections: fade in + translate Y (20px)

**Hover Animations:**
- Buttons: glow expand + color shift (0.3s ease)
- Cards: scale 1.02 + shadow increase (0.3s ease)
- Links: underline slide in

**Continuous Animations:**
- Floating elements: translate Y oscillation (3-5s loop)
- Glow pulse: opacity + scale (2s loop)
- Particles: position updates (requestAnimationFrame)

### 3.3 Data

**Projects Data:**
```
1. AfterTask CLI - CLI tool for task management
2. AfterX Programming Language - Custom language implementation
3. AI Chatbot Website - Conversational AI interface
4. E-Waste Management Platform - Environmental tech solution
5. Legal Assistance Chatbot - NLP-based legal advisor
6. Telegram Study Bot - Educational automation bot
```

**Skills:**
- Python, JavaScript, TypeScript, C++
- React, Node.js, TensorFlow, PyTorch
- AWS, Docker, Git, Linux
- AI/ML, Cloud Architecture, REST APIs

**Services:**
- AI Development (ML models, neural networks)
- Web Development (modern web apps)
- Cloud Solutions (AWS, infrastructure)
- Automation Tools (workflow automation)
- UI/UX Design (interface design)

---

## 4. Technical Requirements

### 4.1 External Resources (CDN)

**Google Fonts:**
- Orbitron: https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;700;900&display=swap
- Exo 2: https://fonts.googleapis.com/css2?family=Exo+2:wght@300;400;500;600;700&display=swap

**Libraries:**
- Vanilla Tilt.js: https://cdn.jsdelivr.net/npm/vanilla-tilt@1.7.0/dist/vanilla-tilt.min.js
- Font Awesome: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css

### 4.2 File Structure

```
/code
├── index.html
├── style.css
├── script.js
└── SPEC.md
```

### 4.3 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

---

## 5. Acceptance Criteria

### Visual Checkpoints
- [ ] Preloader displays and fades out smoothly
- [ ] Navigation is fixed and has glassmorphism effect
- [ ] Hero has animated background particles
- [ ] Name has glitch/glow effect
- [ ] Typing animation cycles through roles
- [ ] All sections have scroll reveal animations
- [ ] Project cards have tilt effect on hover
- [ ] Skills show animated progress indicators
- [ ] Contact form has floating label animations
- [ ] Mobile menu works correctly
- [ ] All hover effects are smooth
- [ ] Colors match specification exactly

### Functional Checkpoints
- [ ] Smooth scroll navigation works
- [ ] All external resources load correctly
- [ ] Page is fully responsive
- [ ] No console errors
- [ ] Animations perform smoothly (60fps target)
- [ ] All buttons/interactive elements work

### Performance Targets
- [ ] First Contentful Paint < 1.5s
- [ ] Smooth animations without jank
- [ ] Images lazy loaded
- [ ] CSS/JS optimized (minified-like structure)
