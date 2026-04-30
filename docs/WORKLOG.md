# Work Log

## Purpose

This file records major updates made to the personal website so the project history
is easier to understand later.

## 2026-04-30

### Homepage Redesign

- Reworked the homepage into a fuller portfolio landing page
- Added a stronger hero section with clearer personal positioning
- Expanded the projects area from a basic list into structured project cards
- Added dedicated sections for About, Resume, Notes, and Contact
- Improved the visual design and mobile responsiveness

### Resume Integration

- Added a standalone `resume.html` page
- Organised education, skills, projects, research experience, and publication content
- Reused details from `cv_old.txt` as source material
- Linked the homepage resume entry points to the new resume page

### Notes Integration

- Added a standalone `notes.html` page
- Created starter note categories and a reusable writing structure
- Updated navigation across the site to include the notes page

### Directory Structure Refinement

- Converted `projects.html` into a minimal directory page with `Completed`, `In Progress`, and `Planned` sections
- Converted `notes.html` into a minimal directory page with the same three-part structure
- Added `note-strong-scaling.html` as the first standalone note page
- Simplified `resume.html` so it matches the quieter directory-style visual language

### Theme Support

- Added a light and dark mode toggle in the navigation
- Stored theme preference in `localStorage`
- Applied the same theme behaviour across the homepage, resume, projects, and notes pages

### Homepage Tightening

- Reduced homepage vertical spacing to keep the front page closer to a single-screen experience
- Simplified the homepage footer into a more compact contact bar
- Fixed the missing `home-page` body class so the homepage-specific layout rules apply correctly

### Styling Improvements

- Moved styling into `styles.css`
- Introduced reusable layout, card, and typography styles
- Added responsive behaviour for smaller screens

### Documentation Improvements

- Rewrote `README.md` to match the current state of the project
- Added internal documentation under `docs/`
- Documented the current project structure and future growth direction

## Next Suggested Tasks

- Add a polished `resume.pdf`
- Add more real project entries to `projects.html`
- Add more standalone notes linked from `notes.html`
- Add project screenshots or charts in a future `assets/` directory
- Add favicon and optional social preview metadata
