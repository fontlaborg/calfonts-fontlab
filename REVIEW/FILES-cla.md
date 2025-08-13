# File Catalog - calfonts-fontlab Repository

## Repository Overview
This repository contains educational materials for type design in FontLab 7, accompanying the YouTube video series by Dave Lawrence from California Type Foundry. It includes sample fonts and tutorial files demonstrating various FontLab techniques.

## Repository Structure

```
.
├── CALAsterisk/           # Sample font directory
├── CALTutorial/           # Tutorial files directory  
├── REVIEW/               # Analysis and review files
├── .gitignore            # Git ignore rules
├── LICENSE               # MIT license
├── README.md            # Repository documentation
└── _config.yml          # Jekyll configuration
```

## Detailed File Catalog

### Root Directory Files

#### `.gitignore`
- **Type**: Configuration file
- **Purpose**: Git ignore rules for macOS .DS_Store files
- **Content**: Simple ignore pattern for .DS_Store files

#### `LICENSE`
- **Type**: Legal document
- **Purpose**: MIT License for the repository
- **Content**: Standard MIT license text with copyright to Fontlab community (2021)

#### `README.md`
- **Type**: Documentation
- **Purpose**: Repository overview and description
- **Content**: Brief description linking to YouTube playlist, mentions CALAsterisk sample font

#### `_config.yml`
- **Type**: Jekyll configuration
- **Purpose**: GitHub Pages theme configuration
- **Content**: Sets jekyll-theme-minimal as the site theme

### CALAsterisk Directory

#### `CALAsterisk.vfj`
- **Type**: FontLab project file (JSON format)
- **Purpose**: Sample font demonstrating element references with multiple asterisk designs
- **Size**: Binary font project file
- **License**: CC-0 (public domain)

#### `LICENSE-CC0.txt`
- **Type**: Legal document
- **Purpose**: CC-0 public domain dedication for CAL Asterisk font
- **Content**: Waives all copyright and neighboring rights

### CALTutorial Directory

This directory contains 30+ FontLab project files (.vfj) and supporting materials for various type design tutorials:

#### Font Project Files (.vfj)
All .vfj files are FontLab 8 project files in JSON format containing font data, glyphs, and metadata:

1. **`cal-cleaning-paths.vfj`** - Tutorial on path cleanup and optimization
2. **`cal-context-kern-necklaces.zip`** - Contextual kerning examples (compressed)
3. **`cal-curve-tension.vfj`** - Curve tension adjustment techniques
4. **`cal-curve-types.vfj`** - Different curve type demonstrations
5. **`cal-delta-filter-start.vfj`** - Delta filter tutorial starting point
6. **`cal-delta-filter-final.vfj`** - Delta filter tutorial final result
7. **`cal-diacritic-height.vfj`** - Diacritic positioning and height management
8. **`cal-exclusion.vfj`** - Character exclusion techniques
9. **`cal-family-starter.vfj`** - Font family creation basics
10. **`cal-family-starter-instances.vfj`** - Font family with multiple instances
11. **`cal-frankenfont.vfj`** - Font combining/merging demonstration
12. **`cal-kerning-exceptions.vfj`** - Advanced kerning exception handling
13. **`cal-letter-heights.vfj`** - Letter height standardization
14. **`cal-making-overlaps.vfj`** - Creating overlapping shapes
15. **`cal-merging.vfj`** - Shape merging techniques
16. **`cal-minus-overlap.vfj`** - Overlap removal operations
17. **`cal-mouse-kern-necklaces.zip`** - Mouse-based kerning tutorials (compressed)
18. **`cal-myfont-regular-2b.vfj`** - Regular weight font example
19. **`cal-non-destructive-transform.vfj`** - Non-destructive transformation methods
20. **`cal-ps-hinting.vfj`** - PostScript hinting techniques
21. **`cal-replacing-segments.vfj`** - Segment replacement operations
22. **`cal-reusing-shapes-1.vfj`** - Shape reuse and component creation
23. **`cal-setting-up-italics.vfj`** - Italic setup and configuration
24. **`cal-sidebearings.vfj`** - Sidebearing management
25. **`cal-slant.vfj`** - Slant transformation techniques
26. **`cal-smoothing-out-rough-h.vfj`** - Letter smoothing and refinement
27. **`cal-style-groups.vfj`** - Style group organization
28. **`cal-weight-axis.vfj`** - Weight axis setup for variable fonts
29. **`cal-width-axis.vfj`** - Width axis setup for variable fonts

#### Supporting Files

#### `Archivo-VariableFont_wdth,wght.zip`
- **Type**: Compressed font file
- **Purpose**: Variable font example with width and weight axes
- **Size**: 252KB
- **Content**: Archivo variable font for reference/comparison

#### `one-window-variations.fl_workspace`
- **Type**: FontLab workspace file
- **Purpose**: Predefined workspace layout for variation editing
- **Content**: FontLab workspace configuration

### REVIEW Directory

#### `files-list.txt`
- **Type**: Generated file list
- **Purpose**: Complete listing of all files in repository
- **Content**: Sorted list of file paths excluding .git

#### `dirs-list.txt`
- **Type**: Generated directory list
- **Purpose**: Complete listing of all directories in repository
- **Content**: Sorted list of directory paths excluding .git

#### `tree-dump.txt`
- **Type**: Empty placeholder
- **Purpose**: Intended for tree structure dump (tree command not available)

## File Type Summary

- **FontLab Projects (.vfj)**: 29 files - Tutorial and example font projects
- **Compressed Archives (.zip)**: 3 files - Additional tutorial materials
- **Documentation (.md)**: 1 file - Repository README
- **Configuration Files**: 2 files - Git and Jekyll configs
- **License Files**: 2 files - MIT and CC-0 licenses
- **Workspace Files**: 1 file - FontLab workspace layout
- **Total Files**: 39 files across 4 directories

## Repository Statistics

- **Primary Content**: Educational FontLab 7/8 tutorials
- **License**: MIT (repository), CC-0 (CALAsterisk font)
- **Maintainer**: Fontlab community
- **Target Audience**: Type designers learning FontLab
- **File Formats**: Primarily FontLab .vfj projects with supporting materials