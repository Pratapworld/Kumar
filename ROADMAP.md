# Grid Engineer's Notebook — Project Roadmap

**Owner:** Pratap Kumar — Relay Protection & Testing Engineer, POWERGRID (400/220 kV Substation) | B.Tech CSE
**Experience:** Relay protection & testing — GIS, AIS, STATCOM, FSC. Interest: Computer Science learning.
**Goal:** Build one website that combines protection notes, free relay calculators, a Bihar grid tracker, and a personal/social section — and keep it alive for years.
**Status:** Planning (no code yet)

---

## 1. The Big Picture (read this first)

You are not building a portfolio. You are building a **digital asset** — a site that gets more useful every year because you keep adding to it. Three things make a site like this survive:

1. **Tools people return to** — calculators give repeat traffic.
2. **Notes people search for** — protection/commissioning knowledge ranks on Google over time.
3. **A tracker nobody else maintains** — Bihar grid data becomes unique because you update it weekly.

Everything below is ordered so you get a **live site in week 1**, then grow it slowly. Do not try to build all four sections at once — that is the #1 reason side projects die.

---

## 2. What We Are Building

Final site has six sections, but we build them in stages:

| Section | What it is | Build stage |
|---|---|---|
| Home | Landing page + intro | Stage 1 |
| Protection Notes | Knowledge base (MiCOM, SIPROTEC, SEL, ABB/Hitachi, AR, distance, diff, busbar, transformer) | Stage 2 |
| Calculators | CT ratio, fault level, per-unit, relay setting, battery sizing, transformer loading | Stage 3 |
| Bihar Grid Tracker | POWERGRID/BSPTCL projects, substations, lines, recruitment | Stage 4 |
| AI for Engineers | Prompts + AI workflows for protection/commissioning | Stage 5 |
| **My Updates** | Trip photos, ongoing project status, LinkedIn link | Stage 2 |
| About Me | Who you are, experience, contact + LinkedIn | Stage 1 |

---

## 3. Tech Choices (kept simple on purpose)

You are learning to code, so we choose tools that are **free, beginner-friendly, and won't trap you**.

- **Hosting:** GitHub Pages (free, no server, your URL becomes `pratapkumar.github.io`). Buy `pratapgrid.com` later and point it here — that's a 10-minute change, not a reason to wait.
- **Stage 1–2 build:** plain **HTML + CSS + a little JavaScript**. No frameworks. This teaches you the fundamentals and runs forever with zero maintenance.
- **Calculators:** plain JavaScript (the math is simple; you already understand the engineering).
- **Notes:** start as HTML pages. If you get 30+ notes, switch to a static site generator (Eleventy or Hugo) — but **not before**, that's premature.
- **Editor:** VS Code (you already have it).
- **Version control:** Git + GitHub (this doubles as your Git practice for CSE).

Why no React/frameworks yet: they add 10 steps before "hello world." You'll learn far more by writing the basics first, and the site will be faster and last longer.

---

## 4. Folder Structure

```text
grid-engineer-site/
├── index.html              # Home
├── about.html              # About Me
├── style.css               # Shared styling for whole site
├── script.js               # Shared small scripts (menu, etc.)
├── notes/
│   ├── index.html          # Notes landing / list
│   ├── micom-p44x.html
│   ├── ct-polarity-check.html
│   └── ...                 # one file per note
├── calculators/
│   ├── index.html          # List of all calculators
│   ├── ct-ratio.html
│   ├── fault-level.html
│   └── ...                 # one HTML file per calculator
├── bihar-tracker/
│   ├── index.html          # The tracker table/page
│   └── data.json           # Project data you update weekly
├── ai-for-engineers/
│   └── index.html
├── updates/
│   ├── index.html          # "My Updates": trips, project status, LinkedIn
│   └── updates.json        # one entry per update (date, title, photo, text)
└── assets/
    └── images/             # logos, diagrams, screenshots, trip photos
```

Keep it flat and obvious. You should be able to find any file in 2 seconds.

---

## 5. Build Order (step by step)

### Stage 1 — Get something LIVE (Week 1) ⭐ most important
Goal: a real URL you can share, even if it's nearly empty.

1. Create a GitHub repo named `pratapkumar.github.io`.
2. Add `index.html` with: your name, role, and a one-line description of the site.
3. Add a simple navigation menu (Home, Notes, Calculators, Tracker, About).
4. Add basic `style.css` so it looks clean (not fancy).
5. Turn on GitHub Pages in repo settings.
6. **Result:** site is live. This early win keeps you motivated.

### Stage 2 — First real content: Protection Notes (Weeks 2–4)
Goal: prove the notes format works with a few high-value pages.

1. Build `notes/index.html` (a simple list of links).
2. Write **3 notes you already know cold**, e.g.:
   - CT polarity check
   - IR value test procedure
   - "P444 not communicating with S1 Agile" troubleshooting
3. Use a consistent layout for every note (title → summary → steps → common faults).
4. Add 1 note per week after that. Consistency beats volume.

### Stage 3 — First calculator (Weeks 5–6) ⭐ highest repeat-value
Goal: one working tool. Start with the easiest.

1. Build **CT Ratio calculator** first (simplest input → output).
2. Layout: input boxes → "Calculate" button → result. Pure JavaScript.
3. Once one works, the rest are copies with different formulas:
   - Fault level → Per-unit → Battery sizing → Transformer loading → Relay setting.
4. Add a `calculators/index.html` listing them all.

### Stage 4 — Bihar Grid Tracker (Weeks 7+)
Goal: the unique asset. Start small, update forever.

1. Make `bihar-tracker/index.html` with a simple table: Project | Type (220/400/765 kV, HVDC, etc.) | Status | Source | Date updated.
2. Store data in `data.json` so updating = editing one file.
3. **Set a weekly 15-minute habit** to add/update one entry. After 2–3 years this is irreplaceable.

### Stage 2.5 — My Updates (personal + social) (alongside notes)
Goal: a living page that shows you're active — good for recruiters and contacts.

1. Build `updates/index.html` as a simple feed: newest update on top.
2. Each update = date + short title + one photo + 2–3 lines. Examples:
   - "Site visit / trip photo" — a picture + one line about it.
   - "Ongoing project status" — e.g. "STATCOM commissioning — testing stage."
   - "Learning update" — e.g. "Started DSA / finished C pointers."
3. Add your **LinkedIn** button here and in the footer + About page (links out to your profile).
4. Store entries in `updates.json` so posting = adding one block, no redesign.
5. Keep photos in `assets/images/` and compress them so the page stays fast.

Tip: this is your "social media" section but on a site **you** own — no algorithm, no ads, and it stays yours forever. Cross-post the same update to LinkedIn for reach.

### Stage 5 — AI for Engineers (later)
Goal: niche authority. Add once the rest is stable.

1. Collect prompts you actually use (relay settings, test reports, troubleshooting).
2. Write short pages: "Using AI to draft a commissioning test report," etc.

---

## 6. Priorities (if you only have limited time)

1. 🥇 **Get it live** (Stage 1) — without a URL, nothing else matters.
2. 🥈 **One working calculator** (Stage 3) — proves the "tool" value and you'll be proud of it.
3. 🥉 **Three protection notes** (Stage 2) — these start earning Google traffic.
4. Then the tracker, then AI section.

Do **not** redesign, buy a domain, or pick a framework until Stages 1–3 are done.

---

## 7. Habits That Keep It Alive

- **15 minutes, 3 days a week** beats a 6-hour weekend that never repeats.
- One note OR one tracker update per week — pick one, do it Sunday.
- Every change is a Git commit — this also builds your CSE/Git skills.
- Don't polish old pages; add new value instead.

---

## 8. What I Can Help You Build Next

When you're ready, I can:
- Generate the **Stage 1 starter site** (index, about, nav, style) directly in this folder.
- Build the **CT Ratio calculator** as your first working tool, with comments so you learn from it.
- Set up a **note template** so every protection note looks consistent.
- Build the **My Updates** feed page with a LinkedIn link and your first few entries.
- Walk you through turning on **GitHub Pages** step by step.

Just tell me which one and I'll create the files.

---

*This roadmap lives in your GitHub folder. Update it as the project grows.*
