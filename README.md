# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Overview

For our first project, we're going to take a look at aggregate SAT and ACT scores and participation rates in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to address our problem statement.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

## Problem Statement

As part of JustHangOn Consulting Group, we have been tasked by US Education department to provide recommendation on how might we be able to increase the SAT /ACT participate rate and score , so that the US education ranking system remain competitive and relevant globally.

We will be studying the trends into the effect of individual key category in, and will provide key insights base on the following key category :

States,
Races,
College Major,
Household Income and State Income,
Fee Waiver and Grant

As part of the team undertaking this study, I will be analysing on Intended College Major relation with participation rate and score


### Contents:
- [Background](#Background)
- [Outside Research](#Outside-Research)
- [Datasets Used](#Datasets-Used)
- [Data Dictionary](#Data-Dictionary)
- [Data Clean Up](#Data-Clean-Up)
- [Exploratory Analysis](#Exploratory-Analysis)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry. Lately, more and more schools are opting to drop the SAT/ACT requirement for their Fall 2021 applications ([*read more about this here*](https://www.cnn.com/2020/04/14/us/coronavirus-colleges-sat-act-test-trnd/index.html)).

## Outside Research

Besides choosing which colleges to apply and working towards the goal, it is equally important to choose a college major. Picking a college major will be one of the most important decisions that one will make as a student. Figuring out what path to focus on earlier in life, is a huge step to determine one's career path. There are many factors that contribute to choosing a college major. These factors include: 

Interest and Abilities

Students will need to determine their own interests and abilities. They will need to know their strengths and weaknessess before pursuing their intended college major. 

Program Costs

Students will need to research on the various program costs for the college major that they are interested in. College majors majoring in law ([*read more about this here*](https://www.collegeavestudentloans.com/blog/how-much-does-law-school-cost-average-law-degree-tuition-costs/#:~:text=According%20to%20U.S.%20News%2C%20the,over%20three%20years%20is%20%2484%2C792.)) or medicine have higher tuition fees ([*read more about this here*](https://www.collegeavestudentloans.com/blog/how-much-does-law-school-cost-average-law-degree-tuition-costs/#:~:text=According%20to%20U.S.%20News%2C%20the,over%20three%20years%20is%20%2484%2C792.)) compared to some other college majors in the USA. Hence, this will be one of the considering factor a student will have to consider as there might be some who will need to get student loans if they do decide to pursue in the major that they are interested in.

Future Employability

It is important to keep up with the world as well as to be able to see what skills or jobs that are in demand. Not all jobs have the same prospects. Some jobs are growing and will be in higher demand whereas some will lead to a declination. 

Income Potential

To some, salary is one of the most important factor when choosing a career path. Hence, it is important to ask yourself if this matters to a student's lifestyle and responsibilites that one may have. Sometimes, income potential may not be a factor fro example to an art students who has a deep passion for art itself. ([*Income for different jobs*]

## Datasets Used

* sat_2019.csv: 2019 SAT Scores by State ([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))
* act_2019.csv: 2019 ACT Scores by State ([source](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows))
* sat_2019_by_intended_college_major.csv: 2019 SAT Scores by Intended College Major ([source](https://reports.collegeboard.org/pdf/2019-total-group-sat-suite-assessments-annual-report.pdf))
* act_2019_by_intended_college_major.csv: 2019 ACT Scores by Intended College Major([source](https://blog.prepscholar.com/average-sat-scores-by-state-most-recent))

## Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**intendedcollegemajor**|*object*|sat_college_major_2019|Different college majors| 
|**testtakers**|*int*|sat_college_major_2019|Number of test takers per college major in 2019| 
|**participation_rate**|*float*|sat_college_major_2019|Percentage of test takers per college major in 2019 where 1.0 represents 100%| 
|**total_score**|*int*|sat_college_major_2019|Total score: Math+ReadingWriting| 
|**ebrw**|*int*|sat_college_major_2019|Mean score of evidence based reading and writing per intended college major| 
|**math**|*int*|sat_college_major_2019|Mean score of mathematics per intended college major| 
|**state**|*object*|act_2019|Different states in US| 
|**participation_rate**|*float*|act_2019|State percentages were calculated by ACT based on the number of high school graduates in each state as projected by the Western Interstate Commission for Higher Education (WICHE) where 1.0 = 100%| 
|**total_score**|*float*|act_2019|Composite score is number of correct answers converts to a score that ranges from 1 to 36 for each of the four tests—and composite score is the average of those. | 
|**state**|*object*|sat_2019|Different states in US| 
|**participation_rate**|*int*|sat_2019|Percentage of test takers taking SAT in 2019, 1.0 = 100%| 
|**ebrw**|*int*|sat_2019|Mean score of evidence based reading and writing|
|**math**|*int*|sat_2019|Mean score of mathematics|
|**total_score**|*int*|sat_2019|Total mean score of SAT|
|**intendedcollegemajor**|*object*|act_college_major_2019|Different college majors| 
|**testtakers**|*int*|act_college_major_2019|Number of test takers per college major in 2019| 
|**participation_rate**|*float*|act_college_major_2019|Percentage of test takers per college major in 2019 where 1.0 represents 100%| 

## Data Clean Up

ACT Data: 3 rows were dropped as there were no participation rate and the state was incorrect, changing percentages to float

SAT Data: changing percentages to a float

SAT by Intended College major:changing percentages to a float

ACT by Intended College major: changing percentages to a float, dropping 21 null values 

## Exploratory Analysis

#### SAT Data
Mean participation rate for SAT 2019: 49.06%

Mean score of EBRW for SAT 2019: 560.80

Mean score of Math for SAT 2019: 552.20

Mean total score for SAT 2019: 1113.08

#### ACT Data
Mean participation rate for ACT 2019: 58.67%

Mean composite score for ACT 2019: 21.46

#### SAT by Intended College Major Data
Mean participation rate for SAT 2019 by Intended College Major: 2.56%

Mean score of EBRW for SAT 2019 by Intended College Major: 535.50

Mean score of Math for SAT 2019 by Intended College Major: 523.00

Mean total score for SAT 2019 by Intended College Major: 1058.50

#### ACT by Intended College Major Data
Mean participation rate for ACT 2019 by Intended College Major: 4.0%

## Conclusions and Recommendations

In order to increase the participation rate for SAT, we will see if there are any underlying factors that may contribute to the increase in SAT participation across states. 

From data comparison between SAT and ACT, ACT has higher participation rate compared to SAT in 2019. 
From the SAT scores by Intended College Major data, the top few most participated college majors are: 
health professions, clinical sciences, business, engineering and visual performing arts. 
This might be due to underlying reasons such as: better career prospects and better salary.

There were pretty large number of test takers who are undecided as to which college major that they would like to choose from. Also, there were very little participating rate for college majors such as mechanic, culinary services, construction trades, transportation, librarianship. This might be due to the nature of these jobscope that do not really require a college degree or their median salary is not high compared to other college majors that can result in a higher paying job in the future.

There is not much correlation as to how Intended College majors will be able to increase participation rate for SAT or ACT. One area that can be improved on is to provide necessary support to students prior to taking the SAT or ACT test so that they are able to realise areas or fields that they are interested in or that they are excellent at. This is to minimise the repurcussions in the future where students are not inspired to take SAT/ACT as they have not yet decide on which College Majors that they intend to pursue in. Another area that can be improved is to have more emphasis in inclusion of science in the SAT test as one of the highest SAT participation rate is for Science based as the intended college major. This is also true for the data from ACT participation rate by Intended College Major. As ACT test has a component on Science, by having more emphasis on Science in SAT as well will ensure that students who wants to major in Science will feel more ready to further in it in college. SATvsACT
