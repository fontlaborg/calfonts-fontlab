---
title: Repository File Catalog
this_file: REVIEW/FILES-cod.md
---

# Repository File Catalog

Scope: Complete catalog of files and folders currently in this repository, with a tree dump and short descriptions. Version-control internals (the contents of `.git/`) are not expanded.

## Filesystem Tree

repo-root/
├── .git/  [Git metadata; not expanded]
├── .gitignore
├── _config.yml
├── LICENSE
├── README.md
├── CALAsterisk/
│   ├── CALAsterisk.vfj
│   └── LICENSE-CC0.txt
└── CALTutorial/
    ├── Archivo-VariableFont_wdth,wght.zip
    ├── cal-cleaning-paths.vfj
    ├── cal-context-kern-necklaces.zip
    ├── cal-curve-tension.vfj
    ├── cal-curve-types.vfj
    ├── cal-delta-filter-final.vfj
    ├── cal-delta-filter-start.vfj
    ├── cal-diacritic-height.vfj
    ├── cal-exclusion.vfj
    ├── cal-family-starter-instances.vfj
    ├── cal-family-starter.vfj
    ├── cal-frankenfont.vfj
    ├── cal-kerning-exceptions.vfj
    ├── cal-letter-heights.vfj
    ├── cal-making-overlaps.vfj
    ├── cal-merging.vfj
    ├── cal-minus-overlap.vfj
    ├── cal-mouse-kern-necklaces.zip
    ├── cal-myfont-regular-2b.vfj
    ├── cal-non-destructive-transform.vfj
    ├── cal-ps-hinting.vfj
    ├── cal-replacing-segments.vfj
    ├── cal-reusing-shapes-1.vfj
    ├── cal-setting-up-italics.vfj
    ├── cal-sidebearings.vfj
    ├── cal-slant.vfj
    ├── cal-smoothing-out-rough-h.vfj
    ├── cal-style-groups.vfj
    ├── cal-weight-axis.vfj
    ├── cal-width-axis.vfj
    └── one-window-variations.fl_workspace

## Descriptions

- repo-root: Top-level folder of the project.
- `.git/`: Git version-control metadata directory. Not part of the distributable content.
- `.gitignore`: Git ignore rules (e.g., OS files like `.DS_Store`).
- `_config.yml`: GitHub Pages/Jekyll configuration; selects `jekyll-theme-minimal` theme.
- `LICENSE`: MIT license for the repository content authored by the Fontlab community.
- `README.md`: Project overview. Links to the “Type design in FontLab 7 with Dave Lawrence (California Type Foundry)” YouTube playlist and describes the CALAsterisk sample.

### Folder: `CALAsterisk/`

- `CALAsterisk/`: Sample font project folder referenced in README; licensed CC0.
- `CALAsterisk/CALAsterisk.vfj`: FontLab 7 project file containing a sample font with multiple asterisks built using element references (per README note). Used as downloadable example.
- `CALAsterisk/LICENSE-CC0.txt`: CC0/public-domain notice specific to CAL Asterisk by California Type Foundry.

### Folder: `CALTutorial/`

Tutorial source files and assets supporting the FontLab 7 video series. Unless noted, `.vfj` files are FontLab 7 project files that illustrate the topic named in the filename; `.zip` files are asset bundles used in those tutorials.

- `CALTutorial/Archivo-VariableFont_wdth,wght.zip`: Variable font (Archivo) archive; likely used in variable font demonstrations.
- `CALTutorial/cal-cleaning-paths.vfj`: Demonstrates cleaning and optimizing Bézier paths in FontLab 7.
- `CALTutorial/cal-context-kern-necklaces.zip`: Assets for context kerning “necklaces” example.
- `CALTutorial/cal-curve-tension.vfj`: Shows curve tension adjustment techniques.
- `CALTutorial/cal-curve-types.vfj`: Explores different curve/segment types.
- `CALTutorial/cal-delta-filter-final.vfj`: Final state of a delta filter tutorial example.
- `CALTutorial/cal-delta-filter-start.vfj`: Starting state of a delta filter tutorial example.
- `CALTutorial/cal-diacritic-height.vfj`: Demonstrates managing diacritic heights.
- `CALTutorial/cal-exclusion.vfj`: Shows exclusion techniques (combining/removing shapes).
- `CALTutorial/cal-family-starter-instances.vfj`: Family starter with instances set up.
- `CALTutorial/cal-family-starter.vfj`: Base family starter project.
- `CALTutorial/cal-frankenfont.vfj`: “Frankenfont” example combining glyph components.
- `CALTutorial/cal-kerning-exceptions.vfj`: Demonstrates kerning exceptions handling.
- `CALTutorial/cal-letter-heights.vfj`: Shows letter height management and alignment.
- `CALTutorial/cal-making-overlaps.vfj`: Techniques for creating overlaps.
- `CALTutorial/cal-merging.vfj`: Merging shapes/contours examples.
- `CALTutorial/cal-minus-overlap.vfj`: Example of removing overlaps (boolean operations).
- `CALTutorial/cal-mouse-kern-necklaces.zip`: Assets for mouse-assisted kerning “necklaces”.
- `CALTutorial/cal-myfont-regular-2b.vfj`: Example regular font state used in tutorials.
- `CALTutorial/cal-non-destructive-transform.vfj`: Non-destructive transform workflows.
- `CALTutorial/cal-ps-hinting.vfj`: PostScript hinting example.
- `CALTutorial/cal-replacing-segments.vfj`: Replacing segments while preserving shapes.
- `CALTutorial/cal-reusing-shapes-1.vfj`: Reusing shapes/components example (part 1).
- `CALTutorial/cal-setting-up-italics.vfj`: Setting up italics and slant systems.
- `CALTutorial/cal-sidebearings.vfj`: Managing sidebearings and spacing.
- `CALTutorial/cal-slant.vfj`: Applying slant operations.
- `CALTutorial/cal-smoothing-out-rough-h.vfj`: Smoothing irregular contours (example with letter ‘h’).
- `CALTutorial/cal-style-groups.vfj`: Using style groups in a family.
- `CALTutorial/cal-weight-axis.vfj`: Working with a weight axis.
- `CALTutorial/cal-width-axis.vfj`: Working with a width axis.
- `CALTutorial/one-window-variations.fl_workspace`: FontLab workspace layout file for “one-window variations”.

Notes:
- Descriptions for tutorial files are inferred from filenames and common FontLab workflows; see the video series for authoritative context.

