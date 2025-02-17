---
title: "HW01: Edit README.md"
date: 2022-08-22T13:30:00-06:00  # Schedule page publish date
publishdate: 2019-03-01

draft: false
type: post
aliases: ["/hw01-edit-README.html"]

summary: "Test your software installation, our GitHub setup, and our homework submission process via pull request, as well as demonstrate competency in Markdown."
---



# Overview

Due by 11:59pm on August 30th.

The goal is to test your software installation, our GitHub setup, and our homework submission process via pull request, as well as demonstrate competency in Markdown.

# Accessing the `hw01` repository

Go [here](https://github.coecis.cornell.edu/cis-fa22) and find your copy of the `hw01` repository. It follows the naming convention `hw01-<USERNAME>`. Clone the repository to your computer using the process below.

In RStudio, start a new Project:

* *File > New Project > Version Control > Git*. In the "repository URL" paste the URL of your new GitHub repository.
* Decide where to store the local directory for the project. Don't scatter everything around your computer - have a central location, or some meaningful structure. For repositories you create in this course, you can setup a `cis` directory and clone all your repos there.
* I suggest you check "Open in new session", as that's what you'll usually do in real life.
* Click "Create Project" to create a new sub-directory, which will be all of these things:
    * a directory on your computer
    * a Git repository, linked to a remote GitHub repository
    * an RStudio Project
* **Whenever possible, this will be the preferred route for setting up your R projects.**

{{% callout note %}}

Make sure you followed the configuration steps [here](/setup/git-configure/) and are able to authenticate yourself before attempting to clone the repository.

{{% /callout %}}

# Edit `README.md`

When you create the repository, you will notice there is only one file in the repo: `README.md`. In future assignments, the repo will be seeded with additional files/data that are necessary to get started.

[Your general workflow](/faq/homework-guidelines/#homework-workflow) will be:

* Pull from GitHub (just an empty precaution now, but will matter when you collaborate with others)
* Make changes locally to `README.md` in RStudio
* Save your changes
* Commit your changes to your repo
* Push the commit to GitHub

## Practice using Markdown

Written assignments will be submitted using [Markdown](https://daringfireball.net/projects/markdown/). Markdown is a lightweight text formatting language that easily converts between file formats. It is integrated directly into [Quarto](http://rmarkdown.rstudio.com/), which combines R code, output, and written text into a single document (`.Rmd`). RegulaQuarto files (`.md`) are rendered on the GitHub website and can be directly read on the website. GitHub includes [a guide](https://guides.github.com/features/mastering-markdown/) for writing Markdown documents.

Your `README.md` should contain a brief biography of yourself. To achieve full marks, you should include at least 4 of the following elements:

* Headers
* Emphasis (italics or bold)
* Lists
* Images[^image]
* Links

# Submit the assignment

Follow instructions on [homework workflow](/faq/homework-guidelines/#homework-workflow).

# Rubric

Needs improvement: `README.md` says equivalent of "This is the repository of Benjamin Soltoff". All work done via browser at github.com ... but that's just a guess, because student doesn't actually say how it was done.

Satisfactory: something in between

Excellent: `README.md` provides a proper introduction of student to the class. It also demonstrates experimentation with 4 or more aspects of the Markdown syntax. Examples: section headers, links, bold, italic, bullet points, image embed, etc. The student describes how they got the changes into `README.md` and offers a few reflections on their GitHub workflow and their experience with Markdown.

## Acknowledgments


* This page is derived in part from ["UBC STAT 545A and 547M"](http://stat545.com), licensed under the [CC BY-NC 3.0 Creative Commons License](https://creativecommons.org/licenses/by-nc/3.0/).

[^image]: Perhaps add a picture of yourself to your repo and embed it in your readme.
