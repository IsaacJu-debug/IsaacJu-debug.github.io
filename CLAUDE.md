# CLAUDE.md - Website Update Guide

This is Isaac Ju's personal portfolio website. The site uses vanilla HTML/CSS/JS with Markdown content files.

## Quick Reference

### Site Structure
```
docs/
├── index.html      # Main HTML (rarely needs editing)
├── about.md        # Profile, bio, social links
├── news.md         # Latest updates and announcements
├── publications.md # Research papers
├── resume.md       # Education, experience, skills
├── styles.css      # Styling (edit for design changes)
├── script.js       # Functionality (edit to add/remove sections)
└── assets/
    ├── profile.jpg              # Profile photo
    ├── favicon.ico              # Browser tab icon
    └── Resume_Isaac_Ju_Beta.pdf # Downloadable CV
```

### Local Development
```bash
python -m http.server 8000 -d docs/
# Open http://localhost:8000
```

## How to Update Content

### Adding a New Publication
Edit `docs/publications.md` and add a new publication card:
```html
<div class="publication-card">
    <div class="publication-content">
        <h3 class="publication-title">
            <a href="PAPER_URL" class="publication-link">Paper Title</a>
        </h3>
        <div class="publication-venue">Conference/Journal Name</div>
        <div class="publication-authors"><strong>Xin Ju</strong>, Co-Author1, Co-Author2</div>
        <div class="publication-year">YEAR</div>
        <div class="publication-tags">
            <span class="tag tag-safety">Topic Tag</span>
            <a href="ARXIV_URL" class="tag tag-arxiv">ARXIV</a>
            <a href="GITHUB_URL" class="tag tag-github">GITHUB</a>
        </div>
    </div>
</div>
```

### Adding News
Edit `docs/news.md`:
```markdown
**Month Year** - Your news item here.
```

### Updating Resume
Edit `docs/resume.md`. Timeline items follow this format:
```html
<div class="timeline-item">
    <span class="timeline-dot"></span>
    <div class="timeline-header">
        <span class="timeline-org">Organization Name</span>
        <span class="timeline-role">Your Role</span>
        <span class="timeline-dates">Start – End</span>
    </div>
    <div class="timeline-meta">Location</div>
    <div class="timeline-desc">Description of work.</div>
</div>
```

### Updating Profile Photo
Replace `docs/assets/profile.jpg` with a new image (keep the same filename).

### Updating CV
Replace `docs/assets/Resume_Isaac_Ju_Beta.pdf` (or update the link in `resume.md`).

### Updating Social Links
Edit the `<div class="about-socials">` section in `docs/about.md`.

## Deployment
The site auto-deploys via GitHub Pages from the `docs/` folder on the `main` branch.

After changes:
```bash
git add -A
git commit -m "Update: description of changes"
git push
```

## Key URLs
- Live site: https://IsaacJu-debug.github.io
- Google Scholar: https://scholar.google.com/citations?user=NldX0YsAAAAJ
- GitHub: https://github.com/IsaacJu-debug
- LinkedIn: https://www.linkedin.com/in/xin-isaac-ju-005290150/
