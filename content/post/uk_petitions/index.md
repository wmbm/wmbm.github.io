---
title: Does petitioning the Government really work?
description: A winding tale of accessing open-source datasets (Part 1)
date: 2024-01-01
image: ukpetitions.jpg
categories:
    - Datasets
    - Data Visualisation
tags:
    - Webscraping
    - CivTech
    - EDA
comments: true
---

We often see Government petitions on our social media platforms. "Sign this petition to save Tiddles the cat from a pack of hungry dogs", "Free Boris Johnson's overcomb", and so on, but what happens to these petitions? Which ones actually make concrete change?

To answer this question I went to the [UK government petition website](https://petition.parliament.uk/) to access the freely available data. However, as I came to find out, the tricky part is that "open-data" often translates to "data behind multiple hurdles".

> _"open-data" often translates to "data behind multiple little hurdles"_

## The problem

The website directory of [all petitions](https://petition.parliament.uk/petitions) contains over 1000 pages each with indivudal CSV or JSON files (a type of data file format). No-one in their right mind would click through all 1000 pages, download them individually, and them combined them into a single dataset!

Certainly, this portal design may help alleviate potential server load issues for UK government developers and facilitate live updates. However, the inability to allow full-batch downloads remains cumbersome and, I would argue, poses a significant obstacle to open-data portals and government transparency initiatives more generally.

## The solution

Luckily, that's where the **power of webscraping** comes in :muscle: We can write scripts to automate this task. By creating a bot in Python (and the Selenium library), we can (automatically) turn through each page, download the individual data files and then combine them into a single complete dataset. And so this is what we did!

You can access the full dataset [here](https://www.kaggle.com/datasets/wilomentena/uk-government-petitions) and associated codebooks.

So now I've got the data, I can finally begin with the analysis...

## Upcoming analysis

The overall research questions will include:

- Is petitioning the government a pro-active and effective means to change?
- Which petitions are most discussed?
- What are the reasons for petition rejections?
- How has the number of petitions and signatures changed over time
- ...

To be continued...

> Something you'd like to add? If you have any questions or comments, feel free to add your thoughts below!

