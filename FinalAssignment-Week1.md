# Peer-graded Assignment: Capstone Project - The Battle of Neighborhoods (Week 1)

For this markdown, we're going to define the following:
- A description of the problem and a discussion of the background.
- A description of the data and how it will be used to solve the problem.

You can find the continuation of this markdown in [this notebook](FinalAssignment-Week2.ipynb).

## Introduction

This in the introductory section of the final assignment of [IBM Applied Data Science Capstone course on Coursera](https://www.coursera.org/learn/applied-data-science-capstone). Here, the students are asked to be as creative as they want to implement Foursquare API and clustering algorithm to explore or compare neighborhoods or cities of their choice. Based on that instructions, __I decided to explore and cluster what is nearby each of top 100 world-class universities__.

__I decided to compare neighborhoods in Sydney and London__.

### Background

[Times Higher Education](https://www.timeshighereducation.com/) (THE) is a credibel and trusted insitution which annually releases [world university rankings](https://www.timeshighereducation.com/world-university-rankings/2020/world-ranking#!/page/0/length/100/sort_by/rank/sort_order/asc/cols/stats). This rankings are based on a selective, transparent, and comprehensive [methodology](https://www.timeshighereducation.com/world-university-rankings/world-university-rankings-2020-methodology). Therefore, they always become a reference for the higher education world. Even many prospective students in the world use its rankings to choose their university of destination for undergraduate and postgraduate study.

However, since THE's methodology is based on the education-centric aspects only, sometimes it is not easy for the prospective students to decide which higher education institution has proper neighborhoods for their college life later at the university. Although THE occassionalyly [publishes articles](https://www.timeshighereducation.com/student/best-universities) related to the best universities for certain kind of students, it still does not have any recommendation regarding the neighborhoods of, for example, top 100 world-best universities. Hence, in this article, we're going to explore the neighborhoods of those top 100 and cluster them in order to gain insight which institutions have similar neighborhoods.

### Aim and Objectives

This article aims to explore and cluster the neighborhoods around each of top 100 higher education instituions in the world based on their venue categories. Meanwhile, to meet the aim, the following are this article's objectives:
- To collect the list of world top 100 higher educations from THE website
- To collect the geospatial coordinates of each higher education institution
- To collect venues data in each higher education institution
- To explore venues data in each higher education institution
- To visualize neighboorhoods in each higher education institution
- To cluster neighborhoods in each higher education institution
- To analyze and discuss the generated clusters

### Target Audience

We can expect at least below audiences could benefit from this article:
- Those who will continue their higher education or would like to work at a higher education institution but are still confused to choose
- Those who would like know more about world-top 100 universities
- Those who would like to know the neighborhood similarity among universities
- Those who would like to gain another perspective from universities
- etc.

## Data Acquisiton

In order to satisfy aim and objectives, we need at least the following data:
- The names of each higher education institution
We can collect these names from THE website.

- The city and country names where each higher education institution based in
We can collect these names from THE website as well.

- The geo location of each higher education institution
We can utilize Google maps to get latitude and longitude of each institute.

- The venues of each higher education institution
We can use Foursquare API to collect venues names. We will be using venues data from each higher education institution to cluster them. Afterwards, we can know which neighborhood of institute shares similarity with a neighborhood in another institute.