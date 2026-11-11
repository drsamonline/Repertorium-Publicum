# Repertorium Publicum Explorer — user guide

**Version 1.3.0 · GPL v3 (the dataset and the app) · one 1.9 MB HTML file**

A homoeopathic repertory you can search in repertory language, build a case from, and analyse.

- Open it: <https://drsamonline.github.io/Repertorium-Publicum/>
- It works offline after the first visit, and from `file://`.

## What the data is

**Repertorium Publicum** by **Vladimir Polony (2008)**, published as part of the
[OpenRep](https://github.com/nondeterministic/oorep) source and licensed **GPL v3**.

It is **not** Kent's *Repertory of the Homoeopathic Materia Medica* (1897). It has its own chapter
structure — separate *Clinical*, *Appetite*, *Blood* and *Heart & Circulation* chapters, which Kent
does not have — and its own additions. Earlier releases of this app called it Kent 1897; that was
wrong and is corrected throughout.

| | |
|---|---|
| Rubrics | 74,480 |
| Graded remedy links | 735,460 |
| Remedies | 669 |
| Chapters | 41 |

Every link carries a grade from the printed repertory's typography: **3** strongest (71,582 links),
*2* moderate (198,591), 1 least (465,287).

## The one habit that matters

**Search in repertory language, not the patient's words** — `anxiety night`, `thirstless`,
`weeping consolation`. Results are ranked **narrowest first**, because a rubric with three remedies
narrows a case and a rubric with 250 tells you almost nothing.

1. Search, and prefer the narrow rubrics.
2. **Add** the ones that survive to your case.
3. Open **Analysis** to rank remedies across them.
4. Treat the ranking as a **shortlist to study in the materia medica**. The repertory narrows; the
   materia medica decides.

## Working a case

- **Named cases** — keep several at once, switch, rename, delete. Each holds its own rubrics and notes.
- **Undo/redo** with `Ctrl+Z`.
- **Three weightings** — 3·2·1, 1·1·1 and 9·4·1 — plus an eliminative filter that keeps only
  grade-2-or-better coverage. The formula is printed under the control, and every export records
  which one produced the numbers.
- **Why a remedy ranks** — click it in the analysis to see every rubric of *this* case it covers, at
  which grade, and which it misses.
- **Remedy → rubrics** — click a remedy chip to see every rubric it appears in, by chapter and grade.
- **Matrix** — a remedy × rubric grid showing each grade.

## Keyboard

`/` search · `↑` `↓` move · `Enter` add · `c` case · `a` analysis · `m` matrix · `t` theme · `Esc` close.

## Exporting and printing

Plain text, CSV, JSON, copy to clipboard, and a **print sheet that is the case** — rubrics, notes,
analysis and matrix without the interface.

## Deep links

`#q=anxiety+night`, `#tab=analysis`, `#demo=case`, `#remedy=Ars`, `#rubric=<id>`. No router and no
dependency; this is what drives the live demo on the landing page.

## Offline

A service worker precaches the app and serves the HTML network-first, so a new release lands on your
next visit. The header says **Offline ready** once cached, and offers **New version — reload** when
one arrives. The footer carries a build stamp, so "am I on the new one?" is answerable from inside
the app.

## Licence

GPL v3 — see [LICENSE](../LICENSE) and [LICENSE-GPL-3.0.txt](../LICENSE-GPL-3.0.txt). The dataset
carries the same licence as the OpenRep source it comes from.
