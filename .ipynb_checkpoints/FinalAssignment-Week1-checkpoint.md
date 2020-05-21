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

Sydney is the state capital of New South Wales and the most populous city in Australia and Oceania. Located on Australia's east coast, the metropolis surrounds Port Jackson and extends about 70 km (43.5 mi) on its periphery towards the Blue Mountains to the west, Hawkesbury to the north, the Royal National Park to the south and Macarthur to the south-west. Sydney is made up of 658 suburbs, 40 local government areas and 15 contiguous regions. Residents of the city are known as "Sydneysiders". As of June 2019, Sydney's estimated metropolitan population was 5,312,163 and is home to approximately 65% of the state's population.[[1]](https://en.wikipedia.org/wiki/Sydney)

London is the capital and largest city of England and the United Kingdom. Standing on the River Thames in the south-east of England, at the head of its 50-mile (80 km) estuary leading to the North Sea, London has been a major settlement for two millennia. Londinium was founded by the Romans. The City of London, London's ancient core − an area of just 1.12 square miles (2.9 km2) and colloquially known as the Square Mile − retains boundaries that closely follow its medieval limits. The City of Westminster is also an Inner London borough holding city status. London is governed by the Mayor of London and the London Assembly.[[2]](https://en.wikipedia.org/wiki/London)

Imagine you were a Sydneysider who was born and spent your childhood amd teenage life in Sydney. And after you'd finished your undergraduate study there, you were sick enough to continue your life in such city. Therefore, you were planning to seek a job and better life in the capital city of the main country of Commonwealth Realm[[3]](https://en.wikipedia.org/wiki/Commonwealth_realm), i.e. London. Well, you wanted to become a Londoner! However, you knew a little, if not nothing, about London. This made you afraid to step forwards. You were worried you might not fit the weather; you were worried whether London had high crime rate compared to your hometown; you were worried if rent space cost there was high; and you were worried you wouldn't feel at home since there was a lot of diiferences in both neighborhoods. Hence, here, we're going to help you realize your dream.

### Aim and Objectives

This article aims to compare two big and famous cities, i.e. Sydney and London, based on both weathers, crime rates, rent space costs, and similarities. Meanwhile, to meet the aim, the following are this article's objectives:
- To collect weather data in Sydney and London
- To collect crime rate data in Sydney and London
- To collect rent space price data in London
- To collect venues data in Sydney and London
- To cluster neighborhoods in Sydney and London
- To propose a recommendation regarding similarity between neighboorhoods in Sydney and London
- To visualize neighboorhoods in Sydney and London

### Expected Audience

Although this article explicitly mentioned that it is for a Sydneysider who wanted to live in London, we can also expect at least below audiences could benefit from this article:
- Those who will/are plan(ing) to migrate from their home country to their country of detination
- Those who would like to know the similarity between two cities
- Those who would like to collect valuable data from a city
- Those who would like to expand their business
- etc.

## Data Acquisiton

In order to satisfy aim and objectives, we need at least the following data:
- Weather
- Crime rate
- Rent space
- Venues

For weather and crime rate data, the appropriate step to collect such data is to obtain directly from the official data history of weather in both Sydney and London. However, if we cannot find the appropriate ones, Kaggle will come to the resque. For rent space cost data, we will use [Zoopla API](https://developer.zoopla.co.uk/) to collect property price data in London. Lastly, for the data regarding nearby venues in the neighborhoods, we will use [Foursquare API](https://developer.foursquare.com/).

We will be using weather, crime rate, and venues data from Sydney and London to cluster their neighborhoods. Afterwards, we can know which neighborhood in Sydney shares similarity with a neighborhood in London. Meanwhile, the property price data will be using to show the property price comparisons among neighborhoods in London.