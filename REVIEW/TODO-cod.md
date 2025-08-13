---
title: Repository Improvement Plan (Proposals Only)
this_file: REVIEW/TODO-cod.md
---

# Repository Improvement Plan (Proposals Only)

Purpose: Concrete, example-illustrated proposals to improve structure, documentation, portability, and publishing of this repository. No implementation is performed here.

## Goals

- Improve discoverability and learning: clear mapping from videos → files.
- Make large binary assets manageable with Git LFS and releases.
- Ensure licensing clarity across folders (MIT + CC0 distinctions).
- Provide a simple website (GitHub Pages) to browse and download examples.
- Add minimal validation to prevent broken archives or accidental bloat.

## Proposed Changes (Detailed)

1) Documentation overhaul
- Add `CALTutorial/README.md` and `CALAsterisk/README.md` with per-file blurbs and usage notes.
- Expand root `README.md` with a table mapping each tutorial file to the corresponding video episode and timestamp.
- Include FontLab version expectations and how to open `.vfj` files.

Example snippet for `CALTutorial/README.md`:

```md
# CALTutorial

This folder contains FontLab 7 tutorial sources used in the video series.

| File | Topic | Video |
|------|-------|-------|
| cal-kerning-exceptions.vfj | Kerning exceptions | Ep. 12 (link) |
| cal-weight-axis.vfj | Weight axis setup | Ep. 7 (link) |
| Archivo-VariableFont_wdth,wght.zip | Variable font asset | Ep. 9 (link) |

Open `.vfj` files in FontLab 7.2+ via File → Open.
```

2) Licensing clarity
- Keep root `LICENSE` (MIT) as-is for repo-level content (docs, READMEs).
- Retain `CALAsterisk/LICENSE-CC0.txt` for the CAL Asterisk sample; add a short `README` noting that CAL Asterisk is CC0 and a trademark notice applies.
- Add a one-paragraph licensing note at the top of `CALTutorial/README.md` clarifying that tutorial source files are examples; if any specific files differ, add per-file notices.

3) Git LFS + attributes for large binaries
- Track `.vfj`, `.zip`, `.fl_workspace` with Git LFS to improve clone performance and storage.
- Add linguist overrides to prevent misclassification.

Example `.gitattributes` lines:

```
*.vfj filter=lfs diff=lfs merge=lfs -text
*.zip filter=lfs diff=lfs merge=lfs -text
*.fl_workspace filter=lfs diff=lfs merge=lfs -text

# Optional GitHub Linguist tweaks
*.vfj linguist-documentation
*.fl_workspace linguist-generated
```

4) Release packaging
- Create GitHub Releases for each “season” or milestone of the tutorial series.
- Attach zipped bundles per topic (e.g., kerning, variable fonts) with a concise CHANGELOG for what’s included.

Proposed release layout example:

```
calfonts-v1.0/
  CALAsterisk/CALAsterisk.vfj
  CALTutorial/kerning/
    cal-kerning-exceptions.vfj
    cal-context-kern-necklaces.zip
    cal-mouse-kern-necklaces.zip
  CALTutorial/axes/
    cal-weight-axis.vfj
    cal-width-axis.vfj
  ...
```

5) GitHub Pages site (uses existing `_config.yml`)
- Add an index page that lists tutorials with direct download links to files in `main` and to Release bundles.
- Provide short embedded GIFs (optional) or screenshots illustrating outcomes per tutorial.

Example `index.md` structure:

```md
# Type design in FontLab 7 – Companion Files

## Getting Started
- Install FontLab 7.2+
- Open any `.vfj` from CALTutorial

## Tutorials
- Kerning Exceptions — [file](CALTutorial/cal-kerning-exceptions.vfj) — [video](…)
- Weight Axis — [file](CALTutorial/cal-weight-axis.vfj) — [video](…)
```

6) Validation and maintenance CI
- Add a small GitHub Actions workflow that:
  - Verifies `.zip` archives are readable (`unzip -t`), without extracting to the repository.
  - Checks that no single file exceeds a size threshold unless tracked by LFS (e.g., >100 MB guardrail).
  - Regenerates a file tree and basic catalog to keep docs in sync (dry-run with PR comment).

Example workflow skeleton:

```yaml
name: repo-sanity
on: [push, pull_request]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          lfs: true
      - name: Check zip integrity
        run: |
          set -e
          find CALTutorial -name '*.zip' -print0 | xargs -0 -r -I{} unzip -t {}
      - name: Size guardrail
        run: |
          find . -type f -size +100M -ls || true
```

7) Folder structure refinements (non-breaking)
- Keep existing flat layout for `CALTutorial/` but add topical subfolders in future additions (e.g., `axes/`, `kerning/`, `contours/`) while maintaining current files for backward compatibility.
- Add per-topic `README.md` when creating new subfolders.

8) Provenance and episode mapping
- Add a machine-readable index (e.g., `tutorials.json`) mapping filenames → topic → episode URL → FontLab version.
- Use it to auto-generate tables for README and the Pages site.

Example `tutorials.json` entry:

```json
{
  "cal-kerning-exceptions.vfj": {
    "topic": "Kerning exceptions",
    "episode": "https://youtu.be/…",
    "fontlab_version": ">=7.2"
  }
}
```

9) Integrity and orientation aids
- Add SHA256 checksums file for large archives in Releases.
- Include quickstart “Open this first” notes in each folder.

10) Contributor guidance (optional)
- Add `CONTRIBUTING.md` with notes on using Git LFS, how to add new tutorial files, and naming conventions (`cal-<topic>.vfj`).

## Risks and Mitigations

- LFS adoption: Ensure contributors install Git LFS; document it clearly and enable via repo settings.
- Link rot to videos: Prefer full YouTube URLs and optionally mirror episode metadata in JSON.
- Pages maintenance: Auto-generate index from `tutorials.json` to avoid manual drift.

## Minimal, Sequenced Rollout Plan

1. Add folder READMEs + root README table.
2. Introduce `.gitattributes` with LFS patterns (no history rewrite).
3. Add GitHub Pages index using existing theme; link key files.
4. Create one initial Release with a curated bundle.
5. Add CI for zip integrity + size guardrail.
6. Add `tutorials.json`; generate tables in docs.

## Out-of-Scope (for now)

- Converting `.vfj` to UFO/DesignSpace automatically (may be revisited later).
- Rewriting history to retroactively add LFS (beneficial but disruptive).

