# Akash Suriya Narayanan — Portfolio

A single-file portfolio site with a top navigation bar and smooth-scrolling sections,
styled as a chemical-engineering process flowsheet. No build step, no dependencies — it
runs anywhere you can host a static file.

```
portfolio/
├── index.html                  ← the entire website (HTML + CSS + JS in one file)
├── assets/
│   ├── img/                    ← your photos go here
│   │   ├── akash.jpg           ← profile photo (nav avatar + hero)
│   │   └── gallery-1..8.jpg    ← carousel slides (8 now)
│   └── docs/
│       ├── Akash-CV.pdf        ← already added (your uploaded CV)
│       ├── Akash-Resume.pdf    ← one-page résumé (add)
│       ├── Akash-Europass.pdf  ← Europass CV (add)
│       ├── abstracts/          ← one PDF per project (see §3)
│       └── certs/              ← certificate PDFs (see §4)
└── README.md                   ← this file
```

The site works right now with placeholders. As you drop real files in with the exact
names below, the placeholders are replaced automatically — nothing else to edit.

---

## 1. Your photo

Save a portrait as **`assets/img/akash.jpg`**. It appears in two places: the round avatar
in the top-left of the navigation bar (where the "AS" mark is now) and the framed photo at
the start of the home section. Until added, both show a clean "AS" placeholder.

- Best shape: portrait (taller than wide), e.g. 800 × 1000 px, under ~1 MB.
- Name it exactly `akash.jpg` (lowercase). If it's a PNG, open `index.html`, search
  `akash.jpg`, and change both mentions to `akash.png`.

## 2. Gallery carousel images

Drop up to eight images in `assets/img/` named `gallery-1.jpg` … `gallery-8.jpg`. Captions
are editable: in `index.html`, search `var caps = [` and change the lines. The current
order is: 1 Erasmus+ trek, 2 BASF Ludwigshafen, 3 Cargill Rovigo, 4 UniPd dinner,
5 CUMI joining day, 6 CUMI promotion, 7 SASTRA graduation, 8 SASTRA Class of 2018–2022.

## 3. Project abstracts  (new)

Every project card has a **"Read abstract ↗"** link. Save each abstract PDF in
`assets/docs/abstracts/` with the exact name below and the links start working.

| Project (card)                            | Save as                                       |
|-------------------------------------------|-----------------------------------------------|
| P-01 IBPE Plant design                    | `assets/docs/abstracts/p01-ibpe.pdf`          |
| P-02 MVR ethanol column                   | `assets/docs/abstracts/p02-mvr-ethanol.pdf`   |
| P-03 VSM snagging wheels                   | `assets/docs/abstracts/p03-vsm-snagging.pdf`  |
| P-04 Power BI dashboard                   | `assets/docs/abstracts/p04-powerbi.pdf`       |
| P-05 CFD orifices in series               | `assets/docs/abstracts/p05-cfd-orifice.pdf`   |
| P-06 CFD ducting network                  | `assets/docs/abstracts/p06-cfd-ducting.pdf`   |
| P-07 Boiler efficiency / HAZOP            | `assets/docs/abstracts/p07-boiler-hazop.pdf`  |
| P-08 Particle-size analyser (C++)         | `assets/docs/abstracts/p08-psd-cpp.pdf`       |

If a project has no abstract, just delete that card's `<a class="pc-link" …>` line in
`index.html`.

## 4. Certificate PDFs

Save each in `assets/docs/certs/` with the exact name:

| Certificate                              | Save as                                   |
|------------------------------------------|-------------------------------------------|
| Lean Six Sigma Yellow Belt               | `assets/docs/certs/lean-six-sigma.pdf`    |
| Oil & Gas Operations (Duke)              | `assets/docs/certs/oil-gas-duke.pdf`      |
| Design Engineer — SolidWorks             | `assets/docs/certs/solidworks.pdf`        |
| Successful Negotiation (Michigan)        | `assets/docs/certs/negotiation.pdf`       |
| Leadership & Emotional Intelligence      | `assets/docs/certs/leadership-ei.pdf`     |
| Developing Soft Skills (IIT Kanpur)      | `assets/docs/certs/soft-skills.pdf`       |
| Employment Communication (IIT Kharagpur) | `assets/docs/certs/employment-comm.pdf`   |
| SCHEMCON 2021 paper                      | `assets/docs/certs/schemcon-2021.pdf`     |

## 5. CV / résumé documents

Detailed CV is already at `assets/docs/Akash-CV.pdf`. Add `assets/docs/Akash-Resume.pdf`
and `assets/docs/Akash-Europass.pdf`.

> File-name rules everywhere: no spaces (use hyphens); GitHub Pages is **case-sensitive**.

---

## 6. Test locally
Double-click `index.html` — it opens exactly as it will appear live.

## 7. Publish with a custom domain (GitHub Pages)

1. Create a public repo and upload the **contents** of this folder so `index.html` sits at
   the repo root with `assets/` beside it.

```bash
git init && git add . && git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/akash-portfolio.git
git push -u origin main
```

2. Repo → **Settings → Pages** → Source **Deploy from a branch** → Branch **main**,
   folder **/ (root)** → Save. Live in ~1 min.

3. Custom domain: add it under **Settings → Pages → Custom domain**, then at your registrar
   add four **A records** for `@` → `185.199.108.153`, `185.199.109.153`,
   `185.199.110.153`, `185.199.111.153`, and a **CNAME** for `www` →
   `<your-username>.github.io`. Tick **Enforce HTTPS** when available.

---

## 8. Common edits (all inside `index.html`)
- Headline — search `I design the`.
- Stats — search `hero-stats`.
- Add a project — copy any `<article class="proj-card" …>` block; `data-cat` controls the
  filter (`design`, `cfd`, `lean`, `code`).
- Colours — the `:root { --copper / --teal / --bg … }` block at the top of `<style>`.
- Contact details — search `mailto:` and `tel:`.
- Carousel captions — search `var caps = [`.

© 2024–2026 Akash Suriya Narayanan.
