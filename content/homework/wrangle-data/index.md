---
title: 'HW03: Wrangling and visualizing data'
date: '2022-09-12T13:30:00-06:00'
publishdate: '2019-03-01'
draft: false
type: post
aliases: /hw03-wrangle-data.html
summary: Wrangle and explore messy datasets in practical research environments
---




# Overview

DUE by 11:59 PM on September 20th.

The goal of this assignment is to practice wrangling and exploring data in a research context.

# Accessing the `hw03` repository

Go [here](https://github.coecis.cornell.edu/cis-fa22) and find your copy of the `hw03` repository. It follows the naming convention `hw03-<USERNAME>`. Clone the repository to your computer.

# Part 1: Tidying messy data

In the `rcis` package, there is a data frame called `dadmom`.


```
## # A tibble: 3 x 5
##   famid named  incd namem  incm
##   <dbl> <chr> <dbl> <chr> <dbl>
## 1     1 Bill  30000 Bess  15000
## 2     2 Art   22000 Amy   18000
## 3     3 Paul  25000 Pat   50000
```

Tidy this data frame so that it adheres to the tidy data principles:

1. Each variable must have its own column.
1. Each observation must have its own row.
1. Each value must have its own cell.

{{% callout note %}}

You can accomplish this task in a single piped operation using only `tidyr` functions. Code which does not use `tidyr` functions is acceptable, but will not merit a "check plus" on your evaluation.

{{% /callout %}}

Once you have tidied the data frame, generate a plot using the exact code below.

```r
ggplot(data = dadmom_tidy, mapping = aes(x = parent, y = inc)) +
  geom_point() +
  geom_line(mapping = aes(group = famid)) +
  scale_y_continuous(labels = scales::dollar) +
  labs(
    title = "Gender parity and household income",
    subtitle = "Each line identifies a distinct family",
    x = "Mom or Dad",
    y = "Income",
  ) +
  theme_minimal()
```

If you tidied the data frame correctly, then you will not have to make any changes to this code.

# Part 2: Wrangling and visualizing messy(ish) data

The [Supreme Court Database](http://scdb.wustl.edu/) contains detailed information of every published decision of the U.S. Supreme Court since its creation in 1791. It is perhaps the most utilized database in the study of judicial politics.

In the `hw03` repository, you will find two data files:

1. `scdb-case.csv`
1. `scdb-vote.csv`

These contain the exact same data you would obtain if you downloaded the files from the original website, but reformatted to be stored as relational data files. That is, `scdb-case.csv` contains all **case-level** variables, whereas `scdb-vote.csv` contains all **vote-level** variables.

The data is structured in a tidy fashion.

* `scdb-case.csv` contains one row for every case and one column for every variable
* `scdb-vote.csv` contains one row for every vote by a justice in every case and one column for every variable

The current dataset contains information on every case decided from the 1791-2020 terms.[^terms] There are several ID variables which are useful for other types of research: for our purposes, the only ID variable you need to concern yourself with is `caseIssuesId`. Variables you will want to familiarize yourself with include:

* `chief`
* `dateDecision`
* `decisionDirection`
* `decisionType`
* `declarationUncon`
* `direction`
* `issueArea`
* `justice`
* `justiceName`
* `majority`
* `majVotes`
* `minVotes`
* `term`

{{% callout note %}}

Please read the [documentation](http://scdb.wustl.edu/documentation.php) to see how these variables are coded.

{{% /callout %}}

Once you import the data files, use your data wrangling and visualization skills to answer the following questions:

{{% callout note %}}

Pay careful attention to the unit of analysis required to answer each question. Some questions only require case-level variables, others only require vote-level variables, and some may require combining the two data frames together. Be sure to choose an appropriate relational join function as necessary.

{{% /callout %}}

1. What percentage of cases in each term are decided by a one-vote margin (i.e. 5-4, 4-3, etc.)?
1. For justices [currently serving on the Supreme Court](https://www.supremecourt.gov/about/biographies.aspx), how often have they voted in the conservative direction in cases involving criminal procedure, civil rights, economic activity, and federal taxation?
    * Organize the resulting graph by justice in descending order of seniority. Note that the chief justice is always considered the most senior member of the court, regardless of appointment date.
1. In each term, how many of the term's published decisions (decided after oral arguments) were announced in a given month?
    * You may want to skim/read chapter 16 in [R for Data Science](http://r4ds.had.co.nz/dates-and-times.html) as it discusses working with dates and times using the `lubridate` package
    * Let me emphasize: you want to skim/read chapter 16 in [R for Data Science](http://r4ds.had.co.nz/dates-and-times.html) as it discusses working with dates and times using the `lubridate` package
    * Also note, the Supreme Court's calendar runs on the federal government's [fiscal year](https://en.wikipedia.org/wiki/Fiscal_year#Federal_government). That means the first month of the court's term is October, running through September of the following calendar year.
1. Which justices are most likely to agree with with the Court's declaration that an act of Congress, a state or territorial law, or a municipal ordinance is unconstitutional?
    * Identify all cases where the Court declared something unconstitutional and determine the ten justices who most and least frequently agreed with this outcome as a percentage of all votes cast by the justice in these cases
    * Exclude any justice with fewer than 30 votes in cases where the Court's outcome declares something unconstitutional
1. For each term he served on the Court, in what percentage of cases was Justice Antonin Scalia in the majority?
1. Create a graph similar to #5 that compares the percentage for all cases versus non-unanimous cases (i.e. there was at least one dissenting vote)
1. In each term, what percentage of cases were decided in the conservative direction?
1. The Chief Justice is frequently seen as capable of influencing the ideological direction of the Court. Create a graph similar to #7 that also incorporates information on who was the Chief Justice during the term.

# Submit the assignment

Your assignment should be submitted as two RMarkdown documents using the `github_document` format. Follow instructions on [homework workflow](/faq/homework-guidelines/#homework-workflow).

# Rubric

Needs improvement: Displays minimal effort. Doesn't complete all components. Code is poorly written and not documented. Uses the same type of plot for each graph, or doesn't use plots appropriate for the variables being analyzed. No record of commits other than the final push to GitHub.

Satisfactory: Solid effort. Hits all the elements. No clear mistakes. Easy to follow (both the code and the output). Nothing spectacular, either bad or good.

Excellent: Finished all components of the assignment correctly and used efficient code to complete the exercises. Code is well-documented (both self-documented and with additional comments as necessary). Graphs and tables are properly labeled. Use multiple commits to back up and show a progression in the work. Analysis is clear and easy to follow, either because graphs are labeled clearly or you've written additional text to describe how you interpret the output.

[^terms]: Terms run from October through June, so the 2020 term contains cases decided from October 2020 - June 2021.
