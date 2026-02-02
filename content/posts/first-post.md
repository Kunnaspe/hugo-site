---
title: "My First Post"
date: 2025-02-21
draft: false
tags: ["hugo", "aws", "s3"]
---

## Welcome to My Hugo Site

This is my first blog post on my new Hugo site. 
This site is automatically deployed to AWS S3 whenever I push changes to GitHub.

### How It Works

1. I push code to GitHub
2. AWS CodePipeline detects the change
3. AWS CodeBuild runs Hugo to generate the static files
4. The files are deployed to an S3 bucket configured for static hosting

It's a fully automated continuous deployment pipeline!
