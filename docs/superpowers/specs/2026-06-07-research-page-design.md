# Research Page — Design Spec
Date: 2026-06-07

## Goal

Create a dedicated Research page accessible from the top nav. Move the "What I work on" content out of About, and add Awards & Honors and Conferences sections. About stays purely personal.

---

## New page: `/research/`

**File:** `_pages/research.md`
**Permalink:** `/research/`
**Title:** Research

### Sections (top to bottom)

1. **Opening line** — "My research focuses on understanding molecular-level structure and dynamics in organic electronic materials, combining atomistic simulation with neutron spectroscopy."

2. **Current projects** — two side-by-side cards

   | Card | Institution | Advisor(s) | Project |
   |------|-------------|-----------|---------|
   | Left | University of California, Davis | Adam J. Moulé | Phonon spectra in organic semiconductors — molecular vibrations, structural disorder, charge transport via inelastic neutron scattering |
   | Right | Max Planck Institute for Polymer Research | Denis Andrienko, Paul W.M. Blom | TADF emitters for OLEDs — polarizable force fields, structural correlation, photophysics; contributing to VOTCA |

3. **Questions that drive my research** — existing bullet list from About, moved verbatim:
   - How do we design organic semiconductors with better charge carrier mobility, and can we predict it before synthesizing anything?
   - What can neutron spectroscopy tell us about disorder that optical methods can't reach?
   - How do polarizable force fields change what we can reliably predict for TADF emitters?
   - Where does computational cost become the real bottleneck, and how do we push that boundary?

4. **Awards and Honors** — table with columns: Award name | Issuing body | Date | Short description

   | Award | Issuer | Date | Description |
   |-------|--------|------|-------------|
   | UC Davis Dissertation Fellowship | Graduate Studies, UC Davis | Mar 2026 | ~$71k covering stipend, tuition, and research allowance for one year |
   | Max Planck Institute Fellowship | UCD Graduate Studies | Jul 2025 | ~$5k covering tuition for one quarter |
   | UCD Graduate Research Award | UC Davis | Mar 2025 | $3k for research supplies |
   | 1st Place — Eureka, Kshitij 2020 | IIT Kharagpur | Feb 2020 | Techno-innovation competition; presented new innovative ideas |
   | Top 25 Teams in India — Empresario 2020 | E-Cell IIT Kharagpur | Jan 2020 | Selected from 1,400 teams across India in a global entrepreneurship event |
   | 1st Place — Azeotropy Entrepreneurship Competition | IIT Bombay | Mar 2019 | Nanotechnology theme; developed a novel nicotine delivery concept with a supporting business case |

5. **Conferences**

   - **APS March Meeting 2026** — Denver, CO
     - *Talk:* Understanding the effect of fluorination on charge transport in organic semiconductors
     - *Poster:* Structural effects of TADF molecules on device performance

   - **ACS Spring 2026** — Atlanta, GA
     - *Talk:* Understanding structure and phonon signatures using a voxelization approach to MD simulations
     - *Talk:* Structural effects of TADF molecules on device performance

   - **Gordon Research Seminar (GRS) / Gordon Research Conference (GRC)** — Electronic Processes in Organic Materials, Italy
     - Selected as speaker (GRS) and poster presenter (GRC) — unable to attend due to funding constraints

6. **Google Scholar button** — same CTA button style as About page

---

## Changes to About page (`_pages/about.md`)

Remove entirely:
- `<h2>What I work on</h2>` and its 3 paragraphs
- `<h3>Questions that drive my research</h3>` and its `<ul>`

Keep everything else unchanged: bio, How I got here, How I work, Skills and tools, Outside the lab, CTA buttons.

---

## Navigation (`_data/navigation.yml`)

Add Research before Teaching:

```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Teaching"
    url: /teaching/
```

---

## Style

Follow the existing About page HTML style exactly: inline CSS, `max-width:800px`, `margin:auto`, `padding:2rem`, `font-family:'Inter',sans-serif`, `line-height:1.7`, `color:#222`. Project cards use `display:flex; gap:1.5rem` with `flex:1` children. Awards use an HTML table. CTA buttons use the existing `.about-section` button styles.
