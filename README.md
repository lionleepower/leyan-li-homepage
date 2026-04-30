# Personal Website – Leyan Li

## Overview

This repository contains the source code for my personal website:

👉 https://leyan-li.com

The site serves as a lightweight portfolio showcasing my background in:

- High Performance Computing (HPC)
- Distributed Systems
- Machine Learning Systems

It is deployed using a modern cloud-based workflow with automatic CI/CD.

---

## Deployment Architecture

The website is deployed using the following stack:

- Hosting Platform: Vercel
- Domain Provider & DNS: Cloudflare
- Version Control: GitHub
- Local Development: WSL (Windows Subsystem for Linux)

### Deployment Flow

Local (WSL) → Git → GitHub → Vercel → Cloudflare → Public Internet

- Changes pushed to GitHub automatically trigger a redeployment on Vercel
- Cloudflare handles DNS resolution, CDN, and TLS termination

---

## Domain & DNS Configuration

### Domain

- Primary domain: `leyan-li.com`
- Secondary: `www.leyan-li.com`

### DNS (Cloudflare)

Configured as:


Type: CNAME
Name: @
Target: cname.vercel-dns.com
Proxy: Enabled (Cloudflare proxy ON)

Type: CNAME
Name: www
Target: cname.vercel-dns.com
Proxy: Enabled


### Notes

- No A records are used
- Cloudflare proxy (orange cloud) is enabled for CDN and protection
- DNS propagation typically completes within minutes

---

## SSL / HTTPS Configuration

Managed by:

- Cloudflare (edge)
- Vercel (origin)

Settings:

- Cloudflare SSL Mode: `Full`
- Automatic HTTPS enabled
- No manual certificate management required

---

## Vercel Configuration

- Framework: None (static HTML)
- Build Command: None
- Output Directory: Root (`.`)

Deployment is triggered automatically on:


git push


### Domain Binding

- `leyan-li.com` connected to Production environment
- `www` also mapped to the same deployment

---

## Project Structure


/
├── index.html # Main entry point
├── README.md # Project documentation


This is a minimal static site with no framework dependencies.

---

## Local Development

Environment:

- OS: Windows + WSL
- Shell: Bash
- Git: CLI-based workflow

Typical workflow:

```bash
git add .
git commit -m "update"
git push

No build step required.

Design Philosophy
Minimal
Fast-loading
No unnecessary frameworks
Focus on content over styling
Future Improvements

Planned enhancements include:

Improved layout and styling (CSS)
Structured sections (Projects, Experience, Contact)
Possible migration to a lightweight framework (e.g. Next.js)
Integration with APIs or dynamic content
Notes for AI Agents (Codex / LLMs)

When modifying this project:

Treat it as a static HTML site
No build pipeline exists
Do not introduce unnecessary dependencies unless explicitly required
Maintain simplicity and readability
Ensure compatibility with Vercel static hosting
Author

Leyan Li
MSc High Performance Computing with Data Science
