---
title: "My Second Post"
date: 2025-02-26
draft: false
tags: ["hugo", "aws", "s3"]
---

## Welcome to My Hugo Site

This is my second blog post on my new Hugo site. 


### Reflections

Going into this project, I honestly wasn't sure what to expect. I'd heard of static site generators before but never actually used one, and the idea of wiring together GitHub, AWS CodeBuild, CodePipeline, and S3 all at once felt like a lot of moving parts.
                                                                                                                                                                                                                                                                                                                                                                                                                                 
Getting Hugo set up locally was pretty straightforward — picking the PaperMod theme and getting a basic site running didn't take long. The harder part was understanding how all the AWS pieces fit together. CodePipeline makes sense in theory: something changes in GitHub, AWS notices, builds the site, and drops the files into S3. But actually configuring it — IAM roles, artifact buckets, service permissions —
there's a lot that has to be right before anything works.

The issue that tripped me up most was the git submodule problem. CodeBuild pulls your source code as a ZIP, which means it has no git history, so running git submodule update just fails. Once I understood why it was failing it was an easy fix — clone the theme directly during the build instead — but it took some digging to get there.

What actually stuck with me from this is how much infrastructure lives behind something as simple as "push code, site updates." Before this I would've just dragged files into an S3 bucket manually. Now I have a pipeline that handles it automatically, and I have a much better sense of how CI/CD works in practice, not just as a concept. That part felt genuinely useful, not just as an assignment but as something
I'd actually use again.
