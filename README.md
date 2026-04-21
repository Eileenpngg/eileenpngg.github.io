# yourname.github.io

Personal cybersecurity portfolio built with Jekyll and hosted on GitHub Pages.

---

## Customising

All personal details live in one place — `_config.yml`. Edit the `author` block and every page updates automatically:

```yaml
author:
  name: "Your Name"
  initials: "YN"                          # shown in the hero avatar circle
  github_username: "yourname"
  linkedin_url: "https://linkedin.com/in/yourname"
  hashnode_url: "https://yourname.hashnode.dev"
  email: "your@email.com"
```

To update projects or write-ups, edit the data files:

| File | Controls |
|---|---|
| `_data/projects.yml` | Projects page + homepage featured cards |
| `_data/writeups.yml` | Write-ups listing |

Set `featured: true` on a project entry to have it appear on the homepage.

---

## Running locally

**Prerequisites:** Ruby 3.x and Bundler (`gem install bundler`).

```bash
bundle install
bundle exec jekyll serve
```

Open [http://localhost:4000](http://localhost:4000). The server rebuilds on file saves.

---

## Deploying to GitHub Pages

1. Create a repository named `yourname.github.io` on GitHub.
2. Push this repo to that remote:
   ```bash
   git remote add origin https://github.com/yourname/yourname.github.io.git
   git push -u origin main
   ```
3. GitHub Pages detects the Jekyll project and builds automatically.
4. The live site appears at `https://yourname.github.io` within a minute or two.

No Actions workflow or extra configuration needed — GitHub Pages has native Jekyll support.

---

## File structure

```
.
├── _config.yml          # Site-wide config and personal details
├── _data/
│   ├── projects.yml     # Project entries
│   └── writeups.yml     # Write-up entries
├── _layouts/
│   ├── default.html     # Base layout (nav + footer)
│   └── page.html        # Thin wrapper extending default
├── assets/
│   └── css/
│       └── style.css    # All styles — plain CSS, no framework
├── index.html           # Homepage
├── projects.html        # Projects listing
├── writeups.html        # Write-ups listing
├── contact.html         # Contact page
└── Gemfile              # Ruby dependencies
```
