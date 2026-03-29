---
title: "My First Post"
date: 2025-02-21
draft: false
tags: ["hugo", "aws", "s3"]
---

## Welcome to My Hugo Site

This was my first blog post on my new Hugo site. I've sinced started adding my reflections.
This site automatically deploys to AWS S3 whenever I push changes to GitHub.

### How It Works

1. I push code to GitHub
2. AWS CodePipeline detects the change
3. AWS CodeBuild runs Hugo to generate the static files
4. The files are deployed to an S3 bucket configured for static hosting

It's now a fully automated continuous deployment pipeline!

#### See my lab 3 reflection:

	
This lab provided best practices for installing a virtual environment in your folder to test out key functionality of your code including the lint (syntax), black formatting, and test functions. The python scaffold allows me to use this format as baseline for a trusted foundation that I can use repeatedly. The makefile simplifies running linting, testing and formatting and installing pip, python and additional dependencies.

I ran a lint test to test my code, using the Noah example as my baseline and following the instructions in the python scaffold video. The screenshot shows my lint command scored a 10 out of 10. 

I ran into one problem trying to run the project in my windows IDE, since cloud 9 isn’t available. I looked at cloud shell, but the features, including the makefile plug in available in vs studio helps me test and validate my code more efficiently than through cloud shell. The example from the video had different code but I had to use scripts/activate to activate the dependencies.

I really liked this lab because it reviewed basics that I need to reinforce and provided best practices. Having a solid scaffolding can make a big difference, and using tools like lint and black can help prevent errors.

This format is repeatable, efficient and very helpful advice.   My github repo with my makefile is located at: https://github.com/Kunnaspe/pythonscaffold/tree/master
