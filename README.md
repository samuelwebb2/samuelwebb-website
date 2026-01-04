# Samuel Webb's Personal Website

My personal website and blog, built with Hugo and hosted at [samuelwebb.co.uk](https://samuelwebb.co.uk).

This site serves as a space to document homelab projects, share technical writings, and showcase work I'm doing in data analytics, automation, and infrastructure.

## About

I'm a mathematics graduate (MMath, University of Edinburgh) currently working as an insurance consultant and studying to become an actuary at LCP in London. My homelab - a collection of servers and systems I use to learn about networking, containerisation, deployment, and infrastructure.

This website is where I write about projects I'm working on, technical problems I've solved, and things I'm learning along the way.

## Previous Work

I previously built and maintained [mathsoc.uk](https://mathsoc.uk) - the website for the University of Edinburgh Mathematics Society.

## Local Development

### Prerequisites

- [Hugo](https://gohugo.io/installation/) (extended version recommended)
- Git

### Setup

```bash
# Clone the repository
git clone https://github.com/samuelwebb2/samuelwebb-website.git
cd samuelwebb-website

# Initialize and update theme submodule
git submodule update --init --recursive

# Run local development server
hugo server -D

# Visit http://localhost:1313
```

### Creating Content

```bash
# Create a new blog post
hugo new posts/my-post-name.md

# Create a new project page
hugo new projects/my-project.md
```

Edit the markdown file, set `draft: false` when ready to publish.

### Building

```bash
# Build the site (output to public/)
hugo

# Build with minification
hugo --minify
```

## Deployment

The site automatically deploys via GitHub Actions when changes are pushed to the `main` branch.

For manual deployment, see `deploy.sh.template` for the deployment pattern.

## Project Structure

```
.
├── archetypes/          # Content templates
├── content/             # Markdown content
│   ├── posts/          # Blog posts
│   ├── projects/       # Project pages
│   └── about.md        # About page
├── static/             # Static assets (images, files)
├── themes/             # Hugo themes (git submodule)
│   └── PaperMod/
├── hugo.toml           # Site configuration
└── .github/
    └── workflows/
        └── deploy.yml  # CI/CD pipeline
```
