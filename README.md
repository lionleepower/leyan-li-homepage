# Personal Website - Leyan Li

## Overview

This repository contains the source code for my personal website:

`https://leyan-li.com`

The site is a lightweight static portfolio focused on:

- High Performance Computing (HPC)
- Distributed Systems
- Machine Learning Systems

It is designed to serve as a long-term personal homepage for:

- project showcases
- resume and academic background
- technical notes and learning logs
- future writing and research reflections

## Current Pages

- `index.html`: minimal homepage and main navigation entry
- `projects.html`: project directory with concise summaries and GitHub links
- `resume.html`: resume-style professional profile
- `notes.html`: notes directory
- `note-strong-scaling.html`: first standalone note entry

## Tech Stack

- Hosting: Vercel
- DNS and CDN: Cloudflare
- Version Control: GitHub
- Local Development: WSL on Windows
- Site Type: static HTML and CSS

There is no framework, no build step, and no dependency installation.

## Deployment Flow

`Local (WSL) -> Git -> GitHub -> Vercel -> Cloudflare -> Public Internet`

Pushes to GitHub trigger automatic deployment on Vercel.

## Domain and SSL

### Domain

- Primary domain: `leyan-li.com`
- Secondary domain: `www.leyan-li.com`

### DNS

Cloudflare is configured with CNAME records pointing to Vercel:

- `@ -> cname.vercel-dns.com`
- `www -> cname.vercel-dns.com`

Cloudflare proxy is enabled.

### SSL

- Cloudflare SSL mode: `Full`
- HTTPS handled by Cloudflare and Vercel
- No manual certificate management required

## Project Structure

```text
/
|-- index.html
|-- projects.html
|-- resume.html
|-- notes.html
|-- note-strong-scaling.html
|-- styles.css
|-- cv_old.txt
|-- README.md
`-- docs/
    |-- WORKLOG.md
    `-- USER_MANUAL.md
```

## Why The Structure Is Kept Simple

At the current size of the project, keeping the website pages in the repository root
is the most practical option for Vercel static hosting.

This structure is already clean enough for a small portfolio site because:

- there are only a few pages
- navigation is straightforward
- no build tooling is needed
- deployment remains simple

## Suggested Future Structure

If the site grows, the next sensible step would be:

```text
/
|-- index.html
|-- projects.html
|-- resume.html
|-- notes.html
|-- note-strong-scaling.html
|-- styles.css
|-- assets/
|   |-- images/
|   `-- files/
`-- docs/
```

That future structure would be useful when adding:

- project screenshots
- downloadable `resume.pdf`
- icons or favicon assets
- PDFs, reports, or presentation files

For now, no further structural refactor is necessary.

## Local Development

Typical workflow:

```bash
git add .
git commit -m "update homepage"
git push
```

Then Vercel will redeploy automatically.

If you want to preview locally, you can open the HTML files directly in a browser or
serve the folder with a lightweight static server.

## Content Maintenance Guide

### Homepage

Edit `index.html` when you want to update:

- homepage identity text
- navigation entry points
- homepage buttons
- contact information
- dark mode toggle placement or wording

### Project Directory

Edit `projects.html` when you want to update:

- completed projects
- in-progress work
- planned work
- GitHub repository links

### Resume Page

Edit `resume.html` when you want to update:

- education
- skills
- project experience
- research and publications

### Notes Page

Edit `notes.html` when you want to:

- update the note directory
- move notes between completed, in-progress, and planned
- add links to standalone note pages

### Standalone Notes

Create or edit files like `note-strong-scaling.html` when you want a note to have its
own dedicated page.

### Styling

Edit `styles.css` when you want to change:

- colours
- spacing
- layout
- typography
- responsive behaviour

## Notes For Future Editing

- Keep the site static unless there is a clear reason to add a framework
- Avoid unnecessary dependencies
- Preserve readability and fast loading
- Reuse the current page structure before creating new complexity
- Keep content professional, clear, and easy to scan
- Keep the homepage minimal and avoid turning it into a long scrolling page

## Internal Documentation

- Work log: [docs/WORKLOG.md](docs/WORKLOG.md)
- User manual: [docs/USER_MANUAL.md](docs/USER_MANUAL.md)

## Author

Leyan Li  
MSc High Performance Computing with Data Science  
University of Edinburgh
