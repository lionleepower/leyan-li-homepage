# User Manual

## What This Project Is

This project is a static personal website for Leyan Li. It contains:

- a homepage
- a projects directory
- a resume page
- a notes directory
- standalone note pages
- shared styling
- internal project documentation

No framework, package manager, or build process is required.

## Main Files

- `index.html`: main homepage
- `projects.html`: project directory
- `resume.html`: resume page
- `notes.html`: notes directory
- `note-strong-scaling.html`: standalone note page example
- `styles.css`: shared styling
- `cv_old.txt`: source reference for older CV content
- `docs/WORKLOG.md`: internal progress record
- `docs/USER_MANUAL.md`: this manual

## How To Edit Content

### Update the homepage

Edit `index.html` to change:

- name, university, and degree text
- homepage navigation
- homepage action buttons
- compact contact footer
- dark mode toggle placement

### Update the project directory

Edit `projects.html` to change:

- completed projects
- in-progress projects
- planned projects
- GitHub links and short descriptions

### Update the resume page

Edit `resume.html` to change:

- education
- skills
- project descriptions
- research experience
- publication section

### Update the notes page

Edit `notes.html` to:

- maintain the notes directory
- move notes between status sections
- add links to standalone note pages

### Update a standalone note

Edit a file such as `note-strong-scaling.html` to change the content of one full note page.

### Update the design

Edit `styles.css` to change:

- colours
- fonts
- card styling
- spacing
- layout behaviour on mobile

## How To Add A New Note

1. Create a new HTML file based on `note-strong-scaling.html`, or duplicate its structure
2. Update the page title, summary, and note body
3. Add a new entry for that note in `notes.html`
4. Save the files and preview them locally

## How To Add A New Project

1. Open `index.html`
2. Open `projects.html`
3. Add a new card in the correct section following the current HTML pattern
4. Include:
   - project name
   - short description
   - GitHub or report link if available
5. If needed, also add the project to `resume.html`

## How To Add A Resume PDF Later

1. Place the file in the repository
2. Recommended future path: `assets/files/resume.pdf`
3. Update links in:
   - `resume.html`
   - `index.html` if you want a direct homepage shortcut
4. Push the change to GitHub

## How To Preview The Site

You can:

- open `index.html` directly in a browser, or
- serve the folder locally with a static file server

Because this is a static site, no build step is required.

In WSL, a practical way to open the project folder is:

```bash
explorer.exe .
```

To open the homepage directly:

```bash
explorer.exe index.html
```

Or:

```bash
wslview index.html
```

## How To Deploy Changes

Typical workflow:

```bash
git add .
git commit -m "describe the update"
git push
```

After pushing:

- GitHub receives the changes
- Vercel automatically redeploys the site
- Cloudflare continues serving the domain

## Recommended Editing Principles

- Keep the structure simple
- Prefer clarity over fancy effects
- Keep project descriptions concrete
- Add measurable results when possible
- Avoid adding frameworks unless the site becomes much larger
- Keep the homepage short and avoid adding scrolling content unless truly needed
- Treat `projects.html` and `notes.html` as directory pages rather than landing pages

## Recommended Next Improvements

- Add a real PDF resume
- Add project screenshots or benchmark charts
- Write the first real technical note
- Add favicon and social share metadata
