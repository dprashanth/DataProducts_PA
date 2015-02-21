---
title       : Coursera Poll
subtitle    : Pitch for the Coursera Poll Application
author      : Prashanth
job         : 
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---


## Introduction - Coursera Poll App

Coursera Poll is an application that prompts user to select the 3 most interesting courses from the "Data Specialization Courses"

User is given the option to select Rank 1, Rank 2 & Rank 3 courses. 

- For Rank1 -  3 points are credited
- For Rank2 -  2 points are credited
- For Rank3 -  1 point is credited

This app can be used to assess the popularity of the courses among the users and plan for any changes in the course content to increase their popularity.

--- 

## Working of the app

### Inputs provided by the User

- User Name
- Course that is Rank 1
- Course that is Rank 2
- Course that is Rank 3
- Remarks

### Information stored by the app

1. Application stores the rankings assigned by the user in an excel database.
2. Keeps track of number of users who have participated in the poll

--- 
## Processing performed by the app 

1. Retrieves all the courses and their rankings that are stored in the database

2. Adds points to the courses that are selected based on the raking provided by the user
   - 3 points for Rank 1
   - 2 points for Rank 2
   - 1 point for Rank 1
   
3. Calculates the total points for all the courses

4. Calculates the mean points for all courses by dividing by number of users

5. Plots a bar plot using ggplot 

6. Displays the table of mean ranks for all courses

---

## Illustration of calculations done by app

If the Course 1 has 3 points and user assigns Rank 1 and the user count is 2, below code sinppet of R represents the calculation done:


```r
Course1 <- 3

Ucount <- 2

Course1 <- Course1 + 3

mCourse1 <- Course1/Ucount
```
### Values Calculated by R code

New value for Course1 = 6 

Mean for Course1 = 3


- - -  
