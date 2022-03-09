# Mini-Project 2

# Overview

In this mini-project, you will wrangle the [Open Payments](https://openpaymentsdata.cms.gov/) dataset in order to reveal at least three findings about the financial relationships between drug and device companies and certain healthcare providers in MA. You will then write up your findings in a short investigative report (400-500 words), written in RMarkdown. You will study the data documentation, review the data dictionary to select variables for your analysis, and then finally produce your analysis. In your blot post, you will key summarize findings from your analysis.

# Learning Goals

* Navigate different forms of data documentation
* Import a dataset and prepare it for analysis
* Apply the verbs of data wrangling to produce insights from data
* Produce a well-styled RMarkdown report
* Communicate data findings in writing
* Evaluate the ethical dimensions of data resources

# Detailed Instructions

## Get to know Open Payments data

1. Watch:

[![Open Payments](http://img.youtube.com/vi/2IT2YjXFP2U/0.jpg)](http://www.youtube.com/watch?v=2IT2YjXFP2U)

[![Nature of Payments](http://img.youtube.com/vi/5f5eIDI0cW8/0.jpg)](http://www.youtube.com/watch?v=5f5eIDI0cW8)

> Note that we will be working with the *General Payments* data for 2020.

2. Review the [data documentation](https://www.cms.gov/OpenPayments/Downloads/OpenPaymentsDataDictionary.pdf). Specifically, the data dictionary for this dataset spans pages 21-33. To help you make sense of this data, I will note that the unit of observation in this dataset is a transaction (not a physician or recipient!). You should be able to identify each row using the `record_id` column.  

3. Explore the [Data Overview](https://www.cms.gov/OpenPayments/Data) page on the Center for Medicare and Medicaid Service's website to learn more. 

4. Check out ProPublica's [Dollars for Docs](https://projects.propublica.org/docdollars/) platform for inspiration on how this dataset can be used in investigate journalism. 

## Set up your environment

1. In RStudio, `File` > `New Project` > `Version Control` > `Git` and then copy the URL to this repo. Open `open_payments_analysis.Rmd` and add your group member's names to the header (lines 5, 7, and 9). 
2. Navigate to the [General Payment Data – Detailed Dataset 2020 Reporting Year](https://openpaymentsdata.cms.gov/dataset/a08c4b30-5cf3-4948-ad40-36f404619019/data).
3. Create a filter so that the data only includes Payments made to recipients in Massachusetts. The updated table should have just under 75,000 rows. 
4. Under the box labeled 'Access', click the link to download the filtered CSV. 
5. Move this CSV file into the data folder on your local machine. **Note that only one student in your group needs to do this.** The dataset can be pushed to other members of your group.

## Import and prepare data

1. On line 36 of `open_payments_analysis.Rmd`, read the CSV file you just downloaded into a data frame. Be sure to use a descriptive variable name for your data frame. 
2. Following instructions in the `clean` code chunk to clean the data for analysis. 

## Wrangle the data

1. Based on your review of the CMS videos, the data documentation, and Dollars for Docs, decide upon one specific question about the financial relationships represented in the data that will motivate your data analysis.
2. Analyze the data, applying the data wrangling verbs towards answering the question you've identified. There's likely many different ways you can answer your question. I encourage you to start off **simple**, producing an analysis that just touches the surface of the question. You can layer in more complicated analysis as you go along. You should be able to summarize at least three findings from your analysis. 

## Write report

1. In 400-500 words, you should write up your findings:
  * Paragraph 1: Introduce the dataset, and the question motivating your analysis
  * Paragraph 2: Report on findings from your analysis.
  * Paragraph 3: Summarize the key takeaway from your analysis and describe at least one ethical concern we should consider when analyzing this data. As a reminder of our ethics framework for this course:
    * What assumptions and commitments informed the design of this dataset?
    * Who has had a say in data collection and analysis regarding this dataset? Who has been excluded?
    * What are the benefits and harms of this dataset, and how are they distributed amongst diverse social groups?
2. Style your report. You may assign headers, fold code, add a table of contents, add images, etc. Be sure to cite any external sources if applicable. Knit your document. 

## Record standards and submit assignment

1. Open `standards.Rmd`, and under each heading, indicate how the work you completed for this project demonstrated fluency in that standard. Just 1-2 sentences per standard!
2. When you are done, you should save both .Rmd files, knit the documents, commit changes, and then push changes back to GitHub. That's it for submission. You don't need to submit anything on Moodle. 

# Evaluation 

You will be evaluated on the extent to which your mini-project demonstrates fluency in the following course learning dimensions:

* GitHub
  * Everyone that submits an assignment will get credit for this!
* RMarkdown
  * Has your report been knitted to HTML?
  * Have you effectively applied RMarkdown syntax to style your report?
* Subsetting Data
  * Have you used the `select()` or `filter()` function to effectively subset the data?
* Aggregating Data
  * Have you used the `group_by()` function in combination with other data wrangling verbs to effectively aggregate the data?
* Importing Data
  * Have you successfully imported a CSV into your environment?
* Code Styling
  * Have you used descriptive variable names?
  * Are you variable names formatted with snake_case?
  * Do you use indenting and white space effectively in your code?
* Cleaning Data
  * Have you successfully convert relevant variables into date formats?
  * Have you successfully cleaned up name variables in the dataset?

You may also layer in any learning dimensions evaluated in the previous Mini-Project. 

