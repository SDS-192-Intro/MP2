# Mini-Project 2

# Overview

> Please note that many aspects of this project are informed by similar projects designed for Professor Albert Kim's and Professor Ben Baumer's SDS 192: Introduction to Data Science courses at Smith College. 

Every year the U.S. Federal Election Commission publishes data that details how candidates and committees raise and spend money in federal elections. In this mini-project, you will perform some data wrangling in order to extrapolate insights from the FEC's campaign contributions dataset in the 2019-2020 election cycle. You will then write up your findings in a short blog post (400-500 words). You will be expected to engage the data wrangling verbs, perform at least one join, and showcase your ability to collaborate effectively in GitHub. In your blog post, you will detail how the data in this dataset was produced, along with what we learn through data wrangling. 

To access the data for this project, you will engage the `fec20` package. The `fec16` package was originally developed by fellow Smithies: Prof Ben Baumer, Rana Gahwagy, Irene Ryan, and Marium A. Tapal! We will use an updated version for this project.

# Learning Goals

* Apply the verbs of data wrangling to produce insights from data
* Join data across multiple tables
* Effectively collaborate with team members in GitHub
* Communicate data findings in writing
* Evaluate the ethical dimensions of data resources

# Detailed Instructions

## Establish a GitHub Workflow

In this lab, I will expect you to develop a GitHub workflow for the project submission. This means that all group members should create issues associated with tasks they are assigned to in GitHub, work in separate branches of the repo to make those changes, and issue Pull Requests to merge their changes into the project. You should also establish a review process to review each other's code before merging. 

1. After reading all of the requirements of this project, I recommend that you delegate tasks amongst group members, start recording those as Issues in the GitHub repo, and assign Issues to group members. 

2. Create separate branches of the repo for each team member.

3. Decide who will be group member 1, 2, 3, and so on.

## Set up your environment

4. In RStudio, `File` > `New Project` > `Version Control` > `Git` and then copy the URL to this repo. **Switch to your branch.** 

5. Open `fec_analysis.qmd` and add your name to the header at the appropriate location (lines 5, 7, and 9). Keep in mind that if you enter your name in the same line number as one of your teammates, you will be dealing with a merge conflict later. This is why it was important to assign numbers in Step 3. At this point I would recommend that you save the file, stage and commit your changes, push the changes to GitHub, have all team members issue their first pull request, merge all of the changes, delete the personal branches, and then recreate the branches for the next round of changes. This will help you practice the workflow and work out any kinks early on. After you've followed these steps, be sure to pull the changes back into RStudio before moving on with the project. 

4. Install the `fec20` package:

`install.packages("remotes")`
`remotes::install_github("lindsaypoirier/fec20")`

## Get to know the FEC data

5. Read about the history and mission of the FEC [here](https://www.fec.gov/about/mission-and-history/).

6. You should review this [README](https://github.com/lindsaypoirier/fec20) as a reference for the data included in these files and as inspiration for your project. Note however, that you may not use the examples in these vignettes in your submission.  

## Wrangle the Data

7. As a group, devise a question about the 2019-2020 campaign contributions, spending, and/or results that you would like to answer with your data. Your question should be concise and should be a question that can be answered with the data available to you via descriptive data analysis. Avoid questions that require predictive analysis or analysis of variables not represented in this dataset.

8. Write one code chunk per team member that leverages some combination of the 6 data wrangling verbs to produce a plot that offers insight into campaign contributions, spending, and/or results in the 2019-2020 election cycle. You must both subset and aggregate the data in some way, and use at least one join in the analysis. All plots must be labeled with all five components of data context. You may help each other write your code chunks, but every team member should ultimately push their own chunk to GitHub. **You should not use the `individuals` table in `fec20`. This table is too large for many computers to handle.**

> Note that I recommend that you try your best to work within the lines allotted to you, without adding new lines to your code chunk. This means using the down arrow instead of the return key to move to a new line. This will help avoid merge conflicts later on. ...even though I fully trust that you'll become whizzes at fixing those when they arise! :)

9. All code chunks must be reviewed on GitHub.com by at least one other team member following a pull request and before merging, and all team members must review at least one chunk. Reviewers may request changes to the code, edits to the comments, suggestions for better labeling/aeshetics, and/or simply commend their peers' work. The course grader and I will be checking for this when evaluating your submission.

## Write blog post

> Note that you do not need to use the long and elegant GitHub workflow for composing the blog post, as I understand that many students would perfer to write this up in Google Docs and the copy it over to RStudio. The long and elegant workflow is only required for the coding sections of the project. 

10. In 400-500 words, you should write a blog post reporting on your visualization:
  * Paragraph 1: Introduce the dataset and the question you posed when approaching the analysis. 
  * Paragraph 2: Report on findings from your analysis.
  * Paragraph 3: Summarize the key takeaway from your analysis and describe at least one ethical concern we should consider when analyzing this data. As a reminder of our ethics framework for this course:
    * What assumptions and commitments informed the design of this dataset?
    * Who has had a say in data collection and analysis regarding this dataset? Who has been excluded?
    * What are the benefits and harms of this dataset, and how are they distributed amongst diverse social groups?
11. Open `contributions.qmd` and briefly describe each team member's contributions to the project. 
12. When you are done, you should save all .qmd files, render the documents, commit changes, and then push changes back to GitHub. That's it for submission. You don't need to submit anything on Moodle. 

# Evaluation 

You will be evaluated on the extent to which your mini-project demonstrates fluency in the following course learning dimensions:

* Transforming Data (15 points)
  * Does the project demonstrate an ability to subset data?
  * Does the project demonstrate an ability to aggregate data?
  * Does the project demonstrate an ability to interpret the results of data? wrangling
* Joining Data (15 points)
  * Does the project demonstrate an ability to join to data frames?
  * Does the project demonstrate an ability to select the most appropriate type of join?
* GitHub (15 points)
  * Does the project demonstrate an ability to delegate tasks effectively via Issues?
  * Does the project demonstrate an ability to collaborate across multiple GitHub branches?
  * Does the project demonstrate an ability to review collaborators' code?
* Ethics (10 points)
  * Does your blog post demonstrate thoughtful consideration of the ethics of this data collection?

Additionally the following will be factored into your grade:

* All components of the assignment were complete (10 points)
  * Did you complete the group contract, fill out the contributions statement, and meet the minimum word count?
  * Was the assignment submitted as an HTML document rendered from Quarto?
* Relevance of Question and Effectiveness of Analysis (10 points)
  * Did you develop a question that could be answered with descriptive data analysis?
  * Did the data analysis that you performed provide enough relevant evidence to address that question?
* Accuracy and Effectiveness of Conclusions (10 points)
  * Did your interpretations of the plots demonstrate a thorough understanding of the underlying data?
  * Were your interpretations of the plots/analysis accurate?
  * Did the evidence that you cited from your plots support the argument that you developed in the blog post?
* Visualization Conventions (15 points)
  * Do you use visual cues effectively on the plot?
  * Are your axes set to an appropriate scale?
  * Are the values on your plot legible and clear?
  * Are there titles and labels for all variables on your plot?
  * Do your titles and labels accurately identify the unit of observation, variables, filters, geographic context, and temporal context?
  
