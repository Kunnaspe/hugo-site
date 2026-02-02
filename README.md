# Kunnas Hugo Site (PaperMod) deployed to AWS S3

This repository contains my Hugo static website. I’m using the **PaperMod** theme and deploying the generated site to an **AWS S3 bucket** via **AWS CodePipeline**.

# What’s in this repo

- `hugo.toml` — Hugo configuration (site title, baseURL, theme, menu)
- `content/` — site pages and posts
  - `content/about.md`
  - `content/posts/first-post.md`
  - `content/posts/second-post.md`
- `buildspec.yml` — build instructions for **AWS CodeBuild** (installs Hugo, clones theme, builds the site)

# Requirements

- Hugo **Extended** (recommended)
- Git

# Clone the repo

```bash
git clone https://github.com/Kunnaspe/hugo-site.git
cd hugo-site
```

# Run the site locally

```bash
hugo server -D
```

Then open:

- http://localhost:1313

# Build the static site

```bash
hugo --minify
```

Hugo outputs the static files to:

- `public/`

# AWS / Deployment notes

- My `baseURL` is set to an S3 static website endpoint.
- The `buildspec.yml` is designed for CodeBuild:
  - installs a specific Hugo version
  - clones the PaperMod theme directly
  - runs `hugo --minify`
  - publishes the `public/` directory as build artifacts

# About Cloud9

AWS Cloud9 may not be available in some AWS accounts/regions anymore.  
For development, I’m using either:
- a local IDE + Git (SSH/HTTPS), or
- GitHub Codespaces

Both workflows still support the same CI/CD deployment pattern (GitHub → CodeBuild/CodePipeline → S3).
# Technologies

- [Hugo](https://gohugo.io/) - Static site generator
- [PaperMod Theme](https://github.com/adityatelange/hugo-PaperMod) - Hugo theme
- [AWS S3](https://aws.amazon.com/s3/) - Static hosting
- [AWS CodePipeline](https://aws.amazon.com/codepipeline/) - CI/CD
- [AWS CodeBuild](https://aws.amazon.com/codebuild/) - Build service

# S3 Bucket 

<img width="2628" height="544" alt="image" src="https://github.com/user-attachments/assets/fb312ffe-78c8-4a72-85e8-395404fe5ada" />

# Additinonal References
- TESU Course 4300 References and Assignment Instructions
- https://github.com/davidbuenonnoleto/amplify_build_hugo - yml example
- https://github.com/Kaimiri/PaperMod_site - Paper Mod Theme

# Site URL (Temporarily Hosted on AWS)
- http://kunnaspe-hugo-site.s3-website-us-east-1.amazonaws.com/
