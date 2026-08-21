# GB210 · AI-Enabled Business Solutions Lab

Companion website for GB210 (AI-Enabled Business Solutions Lab), Wisconsin School of Business,
University of Wisconsin–Madison. Plain HTML, no build step, no dependencies.

## How the course fits together

- **Canvas** is the operational home: assignments, due dates, grades,
  announcements. Nothing with a deadline lives on this site.
- **This site** is the content home. The root page orients students to the
  ecosystem; the schedule is the connective tissue that links each week into
  the resources below.
- **Two “textbooks,” both webpages:**
  - `solve/` — *The SOLVE Framework*, written by Jordan,
    hosted in this repo.
  - [Vibecoding for Business School Students](https://vibecoding-website-alpha.vercel.app/)
    — written by Xiaoyang, hosted externally. Link to it; don’t mirror it.
- **[Wisconsin Case Lab](https://wisconsincaselab.com)** — interview-driven
  simulations. Students need only the access code for each exercise, which is
  distributed **via Canvas, never on this site** (the site and repo are public).

## Instructor notes

The schedule page has an **Instructor view** toggle (also reachable with
`?instructor=1` in the URL). Notes wrapped in
`<div class="inote"><span class="ilabel">Instructor note</span> …</div>`
are hidden from the default student view and shown in instructor view.
This is cosmetic, not secret — notes are visible in the page source — so
keep anything spoiler-sensitive (case answers, the Flashion data trap,
access codes) out of the repo entirely.

## Structure

```
GB210/
├── index.html        # Root hub — orientation page linking everything below
├── schedule/         # Sample course schedule site (week-by-week, links to materials)
│   └── index.html
├── assignments/      # One page per weekly assignment — collects the exercises
│   ├── week-01.html  #   embedded in that week's readings and Friday tutorial
│   └── week-02.html
└── solve/            # The SOLVE Framework site
    ├── index.html    # Start here: premise, how to use the site
    ├── framework.html
    ├── units.html
    ├── reference.html
    ├── sponsor-scopes.html   # GB410 sponsor scopes read through SOLVE (instructor resource; disguised names)
    └── about.html
```

Planned: a `tutorials/` folder with one page per Friday tutorial
(e.g. `tutorials/week-02-setup-checkpoint.html`), linked from the schedule.

The two subsites are deliberately separate — separate navigation, separate
identity. The root `index.html` is a minimal hub and is reserved for future use.

## Hosting on GitHub Pages

1. Push this folder’s contents to the root of the `jordantong/GB210` repository.
2. In the repo: **Settings → Pages → Source: Deploy from a branch →
   Branch: `main`, folder: `/ (root)` → Save**.
3. Within a minute or two the sites appear at:
   - `https://jordantong.github.io/GB210/` (hub)
   - `https://jordantong.github.io/GB210/schedule/` (course schedule)
   - `https://jordantong.github.io/GB210/solve/` (SOLVE framework)

Any edit pushed to `main` republishes automatically. Every page is
self-contained, so you can also open any `.html` file directly in a browser
to preview locally.

## Style

Pages follow UW–Madison brand guidelines (brand.wisc.edu): Badger Red
`#c5050c`, dark red `#9b0000`, light gray `#e1e5e7`, near-black `#121212`;
headings in Red Hat Display, body copy in Red Hat Text (loaded from Google
Fonts). The `solve/` pages predate this and use system fonts with the same
red palette.

## Editing notes

- Each page carries its own copy of the CSS in a `<style>` block; a styling
  change to the SOLVE site means updating it in all six of its pages.
- `solve/sponsor-scopes.html` uses **fictional sponsor names** and rounded
  figures; the real GB410 scopes are under NDA. The real-name version of the
  page, the fake-to-real mapping, and the source scopes all live outside the
  repo in `_GB210 Course Development/SOLVE Framework Development/` and must
  stay there. When editing the page, keep using the fictional names.
- The Unit 6 descriptions in `solve/units.html` deliberately do **not**
  reveal the Flashion data trap or the diagnosis case’s answers — keep it
  that way; the site is student-facing.
