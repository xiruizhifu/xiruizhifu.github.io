---
title: A Story about Prosper Online Loan Business using Tableau
author: Yajie
date: '2017-08-10'
slug: prosper-loan-business-story-tableau
categories: ["Data Science"]
tags: ["Data Visualisation", "Tableau"]
summary: "Personal online loan business has been an important way for borrowers to raise money and for investors to earn interest. However, the risk of this type of investment is definitely higher than T-bills, T-notes and T-bonds, so it's important to address the default risk for this business. In this story, we explored many aspects for personal loan business based on the Prosper Loan Dataset, including the default rates across different states of US, the factors that have clear impact on default rate, etc."
---

## Project Links

[GitHub Links](https://github.com/yajiez/create-tableau-story)

**Tableau Public Workbooks:**

- Story First Version: [Click Here](https://public.tableau.com/shared/Y6H9T3577?:display_count=yes)

- Story Final Version: [Click Here](https://public.tableau.com/views/ProsperLoanData_4/StoryFinalVersion?:embed=y&:display_count=yes)

<div><img src="/img/prosper-loan-final-story.png" width="90%"></div>

## Summary

Personal online loan business has been an important way for borrowers to raise money and for investors to earn interest. However, the risk of this type of investment is definitely higher than T-bills, T-notes and T-bonds, so it's important to address the default risk for this business. In this story, we explored many aspects for personal loan business based on the [Prosper](https://www.prosper.com) Loan Dataset, including the default rates across different states of US, sereval factors which have clear impact on default rate, etc. Moreover, this analysis showed that higher risk loans don't guarantee higher return so a useful tip for investors was given.

## Personal Loan Business over Time

Since 2009, the online personal loan business has increased steadily and climbed up quickly since 2013 and then droped down at the beginning of 2014. However, the borrower credit score has went down over time.

![](/post/prosper-loan-tableau/prosper-loan-trends.png)

## Default Rates across US

Default rates for different states of US have obvious variance, and the default rate in some states were higher than 30%.

![](/post/prosper-loan-tableau/prosper-loan-map.png)

## Relevant Factors about the Default Rate

Higher Income, Lower BorrowerRate and Better Credit Rating imply Lower Default Rate. An interesting pattern was found among the college student group which shows that higher grade students would have more loans and lower default rate, with exception for sophomore student.

![](/post/prosper-loan-tableau/prosper-loan-default-rate-factors.png)

## Higher Return, Higher Risk

It's clearly that ProsperRating is a good indicator and the general principle is: **higher return means higher risk**. However, loans with rating HR have the highest risk but don't have the highest estimated return and loans with C&D have higher actual principal loss than E&HR. So don't put your money in C&D loans.

![](/post/prosper-loan-tableau/prosper-loan-risk.png)

## Final Story

![](/post/prosper-loan-tableau/prosper-loan-final-story.png)

You can found the online version of this story [Here](https://public.tableau.com/views/ProsperLoanData_4/StoryFinalVersion?:embed=y&:display_count=yes).

## Additional Information

### Design of the First Version

The prosper dataset is a complex dataset which contains 113,937 loans with 81 variables, so before I began to create the visualisation, I asked one question to myself again and agian: 

- **What do I want to learn from this dataset?**

My answer was: The most important things that I cared about for this dataset are the status and the relevant factors about the **default rate**. So the story about this dataset was focus on the default rate and I divided them into three groups:

- Trends of the loans over time and the spatial distribution of the default rate;
- The relationships between the default rate and the relevant factors;
- Interesting patterns and useful insights that were found in this process.

**Group One**

- **Trends of the loans over time:** Line Chart;
- **Trends of the ProsperScore over time:** Line Chart;
- **Spatial distribution of the default rate**: Thematic Maps.

In order to see whether each state had the similar tread or not, I chose to use different colors to stand for different state. Also, I created an action to connect the trends of the loans and the default rate map.

**Group Two**

I found three obvious relevant factors of the default rate, so I made three visualisations to show the relatioships between them:

- **Default rate & IncomeRange:** Bar Chart;
- **Default rate & ProsperRating:** Stacked Bar Chart, with one bar for each `ProsperRating` and using color to stand for each `IncomeRange` within that `ProsperRating` loans;
- **Default rate & BorrowerRate:** Scatter Plot, with using color to stand for each `Occupation`, and I added a filter for different `ProsperRating`. Also, I found an interesting patter about the college student group, so I created a group named "College Student", and then used "size" to encode this new group variable to make the "College Student" standing out.

For the interesting patter about the "College Student" group, I created a new chart to show the loans number and default rate among them:

- **Default rate of the College Student:** I used two Bar Charts to show the loans number and defualt rate for different grade of the college students. And I used the "red color" to draw attention for the "Sophomore" student.

**Group Three**

Based on the analysis I found that `ProsperRating` is a good indicator for the default risk of the loans, so I created four bar charts to show `EstimatedEffectiveYield`, `EstimatedLoss`, `EstimatedReturn`, and the Actual Net Principal Loss for loans of different rating. Also, I used "color" to draw attention for the "HR", "C", "D" loans.

Finally, I came up a 3-steps story as follows:

1. Demonstrate the trends and status of the Loans using time series line plot and thematic map;
1. Explore the relationships between the default rate and its relevant factors;
1. Emphasise that higher return means higher risk, and tell the audience don't put money in C&D loans based on this dataset.

### Changes after Feedback

I sent my story to a friend and the response was that it looks like a mess. Well, so sad.

The main point was that I put too many charts in just one screen, and the elements were not rendered clearly in the laptop screen, which would make people stop reading this story entirely.

Upon hearing this feedback I realized that I didn't take different screen sizes of various kinds of the devices today into consideration. I just chose the automatic layout and tweak them to look pretty on my own laptop which has a very high resolution.

Therefore, I divided the 3-steps story into a 5-steps story, and the important changes were:

- In the step 1 of the original story, I created a line chart of the loans number as well as the loans amount, and the trends of them were quite similar, so I removed the line chart of the loans number because the loans amount is more imoortant than the loan number. After the removal of one line chart, it looks more clearly and tidy;
- In the step 2 of the original story, I put all the relevant factors into one place, which made it a messy and different to understand, so I divided the step 2 of the original story into 3 pieces and ordered them in a way which is easy to follow;
- In the step 3 of the original story, I created four bar charts to show `EstimatedEffectiveYield`, `EstimatedLoss`, `EstimatedReturn`, and the Actual Net Principal Loss for loans of different rating. However, it's not necessary to put all of the `EstimatedEffectiveYield`, `EstimatedLoss`, `EstimatedReturn` together, only the `EstimatedLoss` and `EstimatedReturn` would be enough, so I removed the `EstimatedEffectiveYield` bar chart;
- Besides, I realized that the caption boxes of the original story occupied some place, but there were some unused space in the charts themselves. What is more, widescreen is very common now so the vertical space is really precious. As a result, I decided to change the navagator style from "Caption boxes" to "Numbers", and rewrote the most important information of the "Caption boxes" then added them as "text" in or under the blank space of the charts.

Finally, I modified the original 3-steps story into a 5-steps story and changed the navagator style from "Caption boxes" to "Numbers".

## Resources

- [Tableau Online Help](http://onlinehelp.tableau.com/current/pro/desktop/en-us/default.html)
