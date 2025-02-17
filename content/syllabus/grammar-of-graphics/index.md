---
title: "Visualizations and the grammar of graphics"
date: 2022-08-24T12:25:00-05:00
publishDate: 2019-04-03T12:25:00-05:00
draft: false

aliases: ["/cm002.html"]

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
time_end: 2022-08-24T14:20:00-05:00
all_day: false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors: []

# Abstract and optional shortened version.
abstract: ""
summary: "Introduction to data visualizations, the grammar of graphics, and ggplot2."

# Location of event.
location: Hollister Hall 162

# Is this a selected talk? (true/false)
selected: false

# Tags (optional).
#   Set `tags: []` for no tags, or use the form `tags: ["A Tag", "Another Tag"]` for one or more tags.
tags: []

# Links (optional).
url_pdf: ""
url_slides: "/slides/visualizations-and-the-grammar-of-graphics/"
url_video: ""
url_code: ""

# Does the content use math formatting?
math: false
---



## Overview

* Identify the importance of graphics in communicating information
* Define the layered grammar of graphics
* Demonstrate how to use layered grammar of graphics to build Minard's graph of Napoleon's invasion of Russia
* Practice generating layered graphics using [`ggplot2`](https://github.com/hadley/ggplot2)

## Before class

* Read chapters 1-4 from [R for Data Science](http://r4ds.had.co.nz/)
    * Chapters 1, 2, and 4 are very short but set the stage for the next few weeks
    * Chapter 3 is crucial - you need to read this chapter and complete some of the exercises before coming to class. Exercise solutions can be found [here](https://jrnold.github.io/r4ds-exercise-solutions/).
* Read [The grammar of graphics](/notes/grammar-of-graphics/)
    * If you have additional time, also read/skim [A Layered Grammar of Graphics](https://www.tandfonline.com/doi/pdf/10.1198/jcgs.2009.07098)
* [Install and setup software](/setup/)
    * Definitely have R and RStudio installed and operational for class today
    * If you haven't gotten GitHub setup yet, that's fine but you will need it to complete [homework 1](/homework/edit-readme/)

## Class materials

* [Why visualize data?](/notes/why-visualize-data/)
* [How to build a complicated, layered graphic](/notes/minard/)
* [Practice generating layered graphics using `ggplot2`](/notes/gapminder/)

* [Exploring Minard's 1812 plot with `ggplot2`](https://github.com/andrewheiss/fancy-minard) - a much fancier (and more complex) version

## Additional resources

### Graphical design

* [Tufte, Edward R. *The Visual Display of Quantitative Information*.](https://www.edwardtufte.com/tufte/books_vdqi) Classic book on statistical graphics and visualization design.
* [Healey, Kieran. *Data Visualization: A Practical Guide*.](https://socviz.co/) An applied introduction to graphical design with lots of applications in `ggplot2` (and many code examples).

### `ggplot2`

* [ggplot2: Elegant Graphics for Data Analysis, 2nd Edition](https://ggplot2-book.org/) -- Hadley Wickham. Excellent resource for learning the intricacies of `ggplot2`.
* [Documentation for ggplot2](http://docs.ggplot2.org/current/)
* [R Graphics Cookbook, 2nd edition](https://r-graphics.org/) -- Winston Chang. A practical guide with 150 examples to generate quality statistical graphics based on the data you wish to present.
* Why do we learn the `ggplot2` graphics library and not the base [`graphics`](https://cran.r-project.org/web/views/Graphics.html) system? David Robinson explains it well in [Don't teach built-in plotting to beginners (teach ggplot2)](http://varianceexplained.org/r/teach_ggplot2_to_beginners/), and follows up with a longer defense of `ggplot2` in [Why I use ggplot2](http://varianceexplained.org/r/why-I-use-ggplot2/)

### Useful cheatsheets

* [Data visualization with ggplot2 cheat sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/data-visualization.pdf)
* [RStudio IDE Cheat Sheet](https://raw.githubusercontent.com/rstudio/cheatsheets/main/rstudio-ide.pdf) - if you don't know what all the buttons and panels do in RStudio, this is a great decoder

## What you need to do after class

* [Complete the first homework assignment](/homework/edit-readme/)
* If you [installed your software locally](/setup/#option-2---install-the-software-locally), install the [`rcis`](https://github.com/cis-ds/rcis) library from GitHub. To install the package, run the command `remotes::install_github("cis-ds/rcis")` in the console. We will be using data from this package in class next week.

{{% callout note %}}

If you do not already have the `remotes` library installed, you will get an error. Go back and install this first using `install.packages("remotes")`, then run `remotes::install_github("cis-ds/rcis")` in the console.

{{% /callout %}}
