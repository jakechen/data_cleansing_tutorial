# data_cleansing_tutorial
Data cleansing tutorial in Pandas for Chipy Scientific SIG

## Introduction
Data cleansing is an important part of the data analysis / data science workflow because in many cases, these practices require a very clean and standardized data set. Unfortunately, in many cases raw data sets usually contain potential errors such as containing missing values, coming in different file formats, redundancies, inconsistent naming, incorrect data types, just plain wrong values, amongst many problems. All of these concerns should be addressed in the data cleansing phase so that subsequent analysis proceeds smoothly and repeatably.

## Goals
### Goals for this tutorial
- Introduce some commonly used data cleansing techniques in Pandas including:
    - Data import from CSV (excel and stuff to come later)
    - Pandas Series and DataFrames
    - Simple exploration and summaries of data
    - Selecting data
    - Adding and removing data
    - Removing nulls
    - Fixing data types
    - Sorting
    - Concatenation and joining
    - Aggregations and group operations
    - Simple plotting (more to come in a separate tutorial)

### Goals for this example study
With all the media about vaccines causing autism spiking ~2009, we want to explore the rates of vaccinations over the past few years.

For this tutorial, we will focus on Polio in the state of Illinois. Some potential end goals are:

- Has there been an overall decrease in the vaccination rates?
    - Looking at data from years ending in 2005, 2010, and 2015
- What schools decreased the most from 2005 to 2015?
- What vaccines decreased the most from 2005 to 2015?
- OPTIONAL: What schools are at the highest risk of decreasing further?

## Dataset information
Our dataset will come from the Illinois State Board of Education. The dataset is the Immuniation School Survey from the Health Requirements/Student Health Data page. The link is: http://www.isbe.net/research/htmls/immunization.htm 

## Methodology (important)
In order to get a quick sense of the impact of the media coverage ~2009, we decided to pull data from 3 years: 2004-2005, 2009-2010, and 2014-2015.

To measure the impact, we will be looking at the percentage of immunized kids to see if the media decreased (or increased?) that amount at all. This percentage will be **number of kids immunized at the school / total kids enrolled at the school**.