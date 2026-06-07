# Research Page Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a dedicated /research/ page, move "What I work on" content out of About, and add Research to the top nav before Teaching.

**Architecture:** Three file changes — one new page, one nav edit, one About edit. Pure HTML-in-Markdown (Jekyll/academicpages), inline CSS matching the existing About page style. No build tooling beyond `bundle exec jekyll serve`.

**Tech Stack:** Jekyll (academicpages theme), Markdown with raw HTML blocks, YAML front matter, `_data/navigation.yml` for nav.

---

### Task 1: Create the Research page

**Files:**
- Create: `_pages/research.md`

- [ ] **Step 1: Create `_pages/research.md` with the following content**

```markdown
---
permalink: /research/
title: "Research"
author_profile: true
---
<section id="research" style="max-width:800px;margin:auto;padding:2rem;font-family:'Inter',sans-serif;line-height:1.7;color:#222;">

  <p>
    I work on organic electronic materials. Specifically, how molecular-level structure determines
    the way charge moves through them, and why it's so hard to predict. Simulation and neutron
    spectroscopy are how I try to get at it.
  </p>

  <h2 style="margin-top:2rem;font-size:1.5rem;">Current projects</h2>

  <div style="display:flex;gap:1.5rem;margin-top:1rem;flex-wrap:wrap;">
    <div style="flex:1;min-width:260px;border:1px solid #ddd;border-radius:6px;padding:1.2rem;">
      <div style="font-size:0.8rem;font-weight:700;color:#555;text-transform:uppercase;letter-spacing:0.05em;margin-bottom:0.4rem;">University of California, Davis</div>
      <div style="font-size:0.9rem;color:#666;margin-bottom:0.8rem;">Advisor: Adam J. Moulé</div>
      <p style="margin:0;">
        Phonon spectra in organic semiconductors — specifically how molecular vibrations and
        structural disorder shape charge transport. Phonon spectroscopy in disordered organic systems
        doesn't get a lot of attention, partly because it's genuinely hard to do well. But the answers
        it produces are fundamental: understanding <em>why</em> these materials behave the way they do,
        not just recording that they do.
      </p>
    </div>
    <div style="flex:1;min-width:260px;border:1px solid #ddd;border-radius:6px;padding:1.2rem;">
      <div style="font-size:0.8rem;font-weight:700;color:#555;text-transform:uppercase;letter-spacing:0.05em;margin-bottom:0.4rem;">Max Planck Institute for Polymer Research</div>
      <div style="font-size:0.9rem;color:#666;margin-bottom:0.8rem;">Advisors: Denis Andrienko, Paul W.M. Blom</div>
      <p style="margin:0;">
        Thermally activated delayed fluorescence (TADF) emitters for OLEDs. The structural correlation
        in TADF materials — how molecular arrangement shapes photophysical behavior — is still largely
        uncharted. I'm developing polarizable force fields to work out that picture and contributing
        to the <a href="https://www.votca.org/" target="_blank">VOTCA</a> open-source software
        platform. Get the structural correlation right, and the payoff is better OLED materials.
      </p>
    </div>
  </div>

  <h2 style="margin-top:2rem;font-size:1.5rem;">Questions that drive my research</h2>
  <ul style="margin-left:1.5rem;">
    <li>How do we design organic semiconductors with better charge carrier mobility, and can we predict it before synthesizing anything?</li>
    <li>What can neutron spectroscopy tell us about disorder that optical methods can't reach?</li>
    <li>How do polarizable force fields change what we can reliably predict for TADF emitters?</li>
    <li>Where does computational cost become the real bottleneck, and how do we push that boundary?</li>
  </ul>

  <h2 style="margin-top:2rem;font-size:1.5rem;">Awards and honors</h2>

  <table style="width:100%;border-collapse:collapse;margin-top:0.5rem;">
    <tbody>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">UC Davis Dissertation Fellowship</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">Graduate Studies, UC Davis</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Mar 2026</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">~$71k covering stipend, tuition, and research allowance for one year.</td>
      </tr>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">Max Planck Institute Fellowship</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">UCD Graduate Studies</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Jul 2025</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">~$5k covering tuition for one quarter.</td>
      </tr>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">UCD Graduate Research Award</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">UC Davis</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Mar 2025</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">$3k for research supplies.</td>
      </tr>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">1st Place — Eureka, Kshitij 2020</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">IIT Kharagpur</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Feb 2020</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">Techno-innovation competition; presented new innovative ideas.</td>
      </tr>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">Top 25 Teams in India — Empresario 2020</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">E-Cell IIT Kharagpur</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Jan 2020</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">Selected from 1,400 teams across India in a global entrepreneurship event.</td>
      </tr>
      <tr style="border-bottom:1px solid #eee;">
        <td style="padding:0.6rem 0.4rem;font-weight:600;">1st Place — Azeotropy Entrepreneurship Competition</td>
        <td style="padding:0.6rem 0.4rem;color:#555;">IIT Bombay</td>
        <td style="padding:0.6rem 0.4rem;color:#888;white-space:nowrap;">Mar 2019</td>
      </tr>
      <tr>
        <td colspan="3" style="padding:0.2rem 0.4rem 0.8rem;font-size:0.9rem;color:#666;">Nanotechnology theme; developed a novel nicotine delivery concept with a supporting business case.</td>
      </tr>
    </tbody>
  </table>

  <h2 style="margin-top:2rem;font-size:1.5rem;">Conferences</h2>

  <h3 style="margin-top:1.5rem;font-size:1.1rem;">APS March Meeting 2026 — Denver, CO</h3>
  <ul style="margin-left:1.5rem;">
    <li><em>Talk:</em> Understanding the effect of fluorination on charge transport in organic semiconductors</li>
    <li><em>Poster:</em> Structural effects of TADF molecules on device performance</li>
  </ul>

  <h3 style="margin-top:1.5rem;font-size:1.1rem;">ACS Spring 2026 — Atlanta, GA</h3>
  <ul style="margin-left:1.5rem;">
    <li><em>Talk:</em> Understanding structure and phonon signatures using a voxelization approach to MD simulations</li>
    <li><em>Talk:</em> Structural effects of TADF molecules on device performance</li>
  </ul>

  <h3 style="margin-top:1.5rem;font-size:1.1rem;">Gordon Research Seminar (GRS) / Gordon Research Conference (GRC) — Electronic Processes in Organic Materials, Italy</h3>
  <ul style="margin-left:1.5rem;">
    <li>Selected as speaker (GRS) and poster presenter (GRC) — unable to attend due to funding constraints</li>
  </ul>

  <div style="margin-top:2rem;">
    <a href="https://scholar.google.com/citations?user=uno6C3UAAAAJ&sortby=pubdate" target="_blank"
       style="display:inline-block;padding:0.5rem 1.2rem;background:#333;color:#fff;border-radius:4px;text-decoration:none;font-size:0.95rem;">
      Google Scholar
    </a>
  </div>

</section>
```

- [ ] **Step 2: Commit**

```bash
git add _pages/research.md
git commit -m "Add Research page with projects, awards, and conferences"
```

---

### Task 2: Add Research to the navigation

**Files:**
- Modify: `_data/navigation.yml`

- [ ] **Step 1: Open `_data/navigation.yml` and replace the `main:` block**

Current content:
```yaml
main:
  - title: "Teaching"
    url: /teaching/
```

Replace with:
```yaml
main:
  - title: "Research"
    url: /research/
  - title: "Teaching"
    url: /teaching/
```

- [ ] **Step 2: Commit**

```bash
git add _data/navigation.yml
git commit -m "Add Research to top nav before Teaching"
```

---

### Task 3: Remove "What I work on" from About

**Files:**
- Modify: `_pages/about.md`

- [ ] **Step 1: In `_pages/about.md`, delete the block from `<h2 style="margin-top:2rem;font-size:1.5rem;">What I work on</h2>` through the closing `</ul>` of the research questions, including the two HTML comments below it**

The exact block to remove (lines ~32–58 in the file):

```html
  <h2 style="margin-top:2rem;font-size:1.5rem;">What I work on</h2>

  <p>
    At UC Davis, my work is on phonon spectra in organic semiconductors, specifically how molecular
    vibrations and structural disorder shape charge transport. Phonon spectroscopy in disordered organic systems
    doesn't get a lot of attention, partly because it's genuinely hard to do well. But the answers
    it produces are fundamental: understanding <em>why</em> these materials behave the way they do,
    not just recording that they do.
  </p>

  <p>
    At MPIP, I work on thermally activated delayed fluorescence (TADF) emitters for OLEDs. The
    structural correlation in TADF materials (how molecular arrangement shapes photophysical
    behavior) is still largely uncharted. I'm developing polarizable force fields to work out that
    picture and contributing to the
    <a href="https://www.votca.org/" target="_blank">VOTCA</a> open-source software platform.
    Get the structural correlation right, and the payoff is better OLED materials. The path from
    atomistic simulation to device performance is long, but the connection is real.
  </p>

  <p>
    Both projects involve problems where the answer matters and nobody has a clean path to it yet.
    That's usually where I end up.
  </p>

  <h3 style="margin-top:1.5rem;font-size:1.2rem;">Questions that drive my research</h3>
  <ul style="margin-left:1.5rem;">
    <li>How do we design organic semiconductors with better charge carrier mobility, and can we predict it before synthesizing anything?</li>
    <li>What can neutron spectroscopy tell us about disorder that optical methods can't reach?</li>
    <li>How do polarizable force fields change what we can reliably predict for TADF emitters?</li>
    <li>Where does computational cost become the real bottleneck, and how do we push that boundary?</li>
  </ul>

  <!-- ADD LINK: Link your /publications/ page or Google Scholar profile here as "See my publications →" -->
  <!-- ADD PDF: A one-page research overview PDF (export from PPT) in /files/ could go here as a download button -->
```

After removal, the `<h2>How I got here</h2>` section should follow directly after the second intro paragraph about growing up in West Bengal.

- [ ] **Step 2: Verify the About page still reads cleanly** — the two opening paragraphs (UC Davis intro + West Bengal background) should flow directly into `<h2>How I got here</h2>` with no gap or orphaned content.

- [ ] **Step 3: Commit**

```bash
git add _pages/about.md
git commit -m "Remove 'What I work on' section from About page"
```

---

### Task 4: Visual verification

- [ ] **Step 1: Start Jekyll locally**

```bash
bundle exec jekyll serve
```

Expected output includes `Server address: http://127.0.0.1:4000` and `Server running...`

- [ ] **Step 2: Check each page**

Open `http://127.0.0.1:4000/research/` — verify:
- "Research" appears in the top nav
- Opening paragraph renders
- Two project cards appear side by side (may stack on narrow windows — that's fine, `flex-wrap:wrap` handles it)
- Awards table renders with three columns
- All three conference entries appear with their talk/poster details
- Google Scholar button appears at bottom

Open `http://127.0.0.1:4000/about/` — verify:
- "What I work on" heading is gone
- "Questions that drive my research" bullet list is gone
- Bio flows directly from the West Bengal paragraph into "How I got here"
- Nothing else changed

Open `http://127.0.0.1:4000/` — verify the top nav shows Research before Teaching.

- [ ] **Step 3: Stop the server** (`Ctrl+C`)
