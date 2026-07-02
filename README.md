# WuGroup Onboarding Tutorials

A self-paced onboarding curriculum for new members of the **Wu Research Group (XJTLU)**,
covering foundational tooling and computational-science foundations.

The site is **standalone static HTML** — open `index.html` directly in a browser
(no build step, no server, no CDN, works offline).

## View it

Open `index.html` in any browser, or serve the folder:

```bash
python3 -m http.server   # then visit http://localhost:8000
```

## Structure

```
index.html              Landing page + module catalog
assets/style.css        Shared stylesheet (self-contained, no external fonts/CDN)
assets/img/             Generated figures (e.g. matplotlib SVG/PNG), committed locally
modules/_TEMPLATE.html  Canonical page template — copy this for a new module
modules/<slug>.html     One page per module
```

## Curriculum (17 modules)

**Area 1 — Foundational & Tooling Skills**
1. Unix/Linux Basics · 2. Bash Scripting · 3. Version Control with Git ·
4. Python for Scientific Computing · 5. Scientific Software & Environments ·
6. HPC & SLURM Job Submission · 7. Working with AI Coding Agents

**Area 2 — Scientific Domain Foundations**
8. Statistical Mechanics · 9. Molecular Simulations · 10. Polymer Physics ·
11. Machine Learning for Chemistry & Materials

**Area 3 — Research Skills**
12. Reading Academic Literature · 13. Doing a Literature Review ·
14. Managing Research Data & Computational Projects *(planned)* ·
15. Scientific Writing & Publishing *(planned)* ·
16. Presenting Research: Talks & Posters *(planned)* ·
17. Research Integrity & Responsible AI Use *(planned)*

## How to add / write a module

1. Copy `modules/_TEMPLATE.html` to `modules/<slug>.html` and fill in the sections.
2. Change the badge on that module's card in `index.html` from `badge--soon` ("Coming soon")
   to `badge--ready` ("Ready").
3. Follow the house rules (also in the template's header comment):
   - **Standalone**: no build step, no CDN, only `assets/style.css`.
   - **No Notion links.** Extract the content and write it here; cite only permanent
     primary sources (journal DOI, YouTube, textbook, official docs) — never Notion URLs
     or expiring Notion S3 file links.
   - **Figures**: add original schematics where they help — inline `<svg>` for concept
     diagrams, locally-committed generated plots (matplotlib → `assets/img/`) for data.
     No external image hot-links, no copied textbook/paper figures; every figure gets a
     caption and accessible `<title>`.
