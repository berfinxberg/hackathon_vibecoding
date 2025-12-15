# Vibe Portfolio — Vibe-Coding PRD (UXD Master)

**Project Vibe (1-sentence pitch):**  
A minimalist, AI-assisted portfolio website that helps UX students present projects, skills, and personality quickly and clearly.

**Date:** 15.12.2025  
**Author(s):** Berfin Berg  
**Version:** v0.1

**Links:**  
- Repo: https://github.com/berfinxberg/hackathon_vibecoding  
- Docs: Hackathon Guide / PRD  
- Issue Tracker: GitHub Issues

---

## 1) Core Context — “Master Prompt”

**Problem:**  
UX students often struggle to build a professional portfolio website quickly due to technical barriers, unclear structure, and time constraints.

**Solution:**  
A pre-structured, AI-assisted portfolio website built via vibe coding that enables fast customization of content, layout, and personal branding.

**Target Users:**  
- UX / UI design students  
- Early-career designers  
- Hackathon participants

**Primary Use Cases:**  
- Present personal profile and skills  
- Showcase UX projects  
- Share CV and contact information

**North-Star Success Metric:**  
A fully deployed portfolio website within one hackathon session (≤ 3 hours).

**Non-Goals:**  
- No custom CMS  
- No advanced animations  
- No backend user accounts

---

## 2) UX Foundations (Vibe, Research, Accessibility)

**Personas:**  
- UX Master student with limited coding experience  
- Time-constrained job applicant

**Top Insights / Pain Points:**  
- “I don’t know where to start.”  
- “Coding slows me down.”  
- “My portfolio never feels finished.”

**Emotional & Contextual “Vibe” Principles:**  
- Calm  
- Confident  
- Minimal  
- Professional but personal

**Accessibility & Inclusion Requirements:**  
- Semantic HTML  
- Sufficient color contrast (WCAG AA)  
- Keyboard navigation  
- Alt text for images

**High-Level Journey:**  
Landing → About → Projects → CV → Contact

---

## 3) Scope & Priorities

**MVP (V1) Goals:**  
- Hero section with name & role  
- About section  
- Project list (1–2 projects)  
- CV section  
- Contact links

**Out of Scope for V1:**  
- Blog  
- Multilingual support  
- Analytics dashboard

**Assumptions & Risks:**  
- GitHub Pages deployment works smoothly  
- AI-generated content needs manual review

---

## 4) Tech Stack & Architecture

**Frontend:**  
- Jekyll (Academic Pages Template)  
- HTML / Markdown / CSS

**Backend:**  
- None (static site)

**Database:**  
- None

**Key APIs:**  
- None (optional: OpenAI for content generation during build)

**Deployment:**  
- GitHub Pages

**Security / Privacy:**  
- No personal data storage  
- Public content only

---

## 5) Feature Modules (Prompt-by-Prompt, Build the MVP)

### Module 1: Landing / Hero
**Priority:** P0  
**User Story:**  
As a visitor, I want to immediately understand who this portfolio belongs to and what the person does, so that I can decide if I should keep exploring.

**Acceptance Criteria — To-Prompt Checklist:**  
- [x] Hero section exists on the homepage  
- [x] Name + role/title are visible above the fold  
- [x] One clear CTA exists (e.g., “View Projects” / “Download CV”)  
- [x] Layout works on mobile + desktop  
- [x] Headings use semantic hierarchy (H1, H2...)

---

### Module 2: About / Profile
**Priority:** P0  
**User Story:**  
As a recruiter, I want a quick personal summary, so that I understand the designer’s focus and strengths.

**Acceptance Criteria — To-Prompt Checklist:**  
- [x] About section exists (short bio)  
- [x] Skills or focus areas are listed (3–6 bullets)  
- [x] Profile image has alt text (if used)  
- [x] Tone is professional + personal (consistent “vibe”)

---

### Module 3: Projects Overview
**Priority:** P0  
**User Story:**  
As a recruiter, I want to scan key projects quickly, so that I can evaluate relevance.

**Acceptance Criteria — To-Prompt Checklist:**  
- [x] A “Projects” section/page exists  
- [x] Each project has: title, 1–2 line summary, role, timeframe (optional)  
- [x] Each project has a link to detail page OR external link (case study / repo)  
- [x] Projects are readable and scannable (cards or clear list)  
- [x] Images (if used) have alt text  

---

### Module 4: CV / Resume
**Priority:** P0  
**User Story:**  
As a recruiter, I want to view or download a CV, so that I can assess experience quickly.

**Acceptance Criteria — To-Prompt Checklist:**  
- [x] CV section/page exists  
- [x] CV is readable in-page OR downloadable as PDF link  
- [x] Education + Experience + Skills are included (short)  
- [x] No private/sensitive information accidentally included  

---

### Module 5: Contact / Links
**Priority:** P0  
**User Story:**  
As a visitor, I want an easy way to contact the designer, so that I can reach out for opportunities.

**Acceptance Criteria — To-Prompt Checklist:**  
- [x] Contact section exists  
- [x] At least 2 links: Email + LinkedIn (optional GitHub/Behance)  
- [x] Links are accessible (clear labels, visible focus state)  
- [x] Works on mobile  

---

## 6) AI Design & Prompting Strategy

**System Prompt:**  
You are a senior UX designer and web content assistant. Help me create concise, professional, accessible portfolio copy and structure for a static site. Keep tone calm, confident, minimal. Ask for missing personal details only when required.

**Prompt Bank (TACO examples):**  
- **T:** Write hero headline + subtitle for a UX portfolio  
  **A:** Produce 3 options, each max 10 words headline + max 16 words subtitle  
  **C:** UX Master student, tone: calm/confident/minimal, avoid buzzwords  
  **O:** Return as a numbered list

- **T:** Generate 2 project summaries for portfolio cards  
  **A:** Each: 1 sentence problem + 1 sentence outcome  
  **C:** Audience: recruiter, include role + impact, no invented metrics  
  **O:** Return in a table: Project | Problem | Outcome | My Role

**Reasoning Boosters (CoT, ToT, Meta):**  
- Generate multiple options → pick best → refine once
- Use checklists for acceptance criteria and accessibility

**Hallucination Mitigation & Safety:**  
- Do not invent facts, employers, certifications, or metrics  
- If information is missing, use placeholders like “[add metric]”  
- Keep personal data minimal (no address, phone optional)

**Vibe-Coding History:**  
- Prompts used iteratively in Cursor/Codex and committed per milestone

---

## 7) IA, Flows & UI

**Information Architecture:**  
Home (Hero + About)  
→ Projects (Overview)  
→ Project Detail (optional 1–2 pages)  
→ CV  
→ Contact

**Key Flows:**  
- Recruiter flow: Home → Projects → CV → Contact  
- Quick scan flow: Home → Projects cards → External links

**Design Tokens & Components:**  
- Minimal layout, generous whitespace  
- Clear typography hierarchy (H1/H2/H3)  
- Card/list components for projects  
- One accent color, high contrast, accessible links

**Localization & Tone Guidelines:**  
- Language: English (or German—consistent across pages)  
- Tone: concise, human, confident; avoid fluff


---

## 8) Iteration Plan & Workflow

**Build Rhythm:**  
Prompt → Generate → Review → Commit

**Versioning & Reviews:**  
- Git commits per milestone

**Risk / Spike Tickets:**  
- Jekyll configuration issues  
- GitHub Pages build errors

---

## 9) Quality: Testing, A11y, Performance

**Testing:**  
- Manual testing  
- Cross-browser checks

**Accessibility:**  
- WCAG AA color contrast  
- Semantic structure

**Performance Budgets:**  
- Static assets only  
- Fast initial load

---

## 10) Metrics & Analytics

**Events & Properties:**  
- Page views  
- Project clicks

**Dashboards / KPIs:**  
- Portfolio live and accessible

---

## 11) Launch & Ops

**Environments & Feature Flags:**  
- Production only (GitHub Pages)

**Rollout Plan:**  
- Immediate publish after MVP completion

**Support & Maintenance:**  
- Manual updates via GitHub