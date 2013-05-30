---
layout: post
title: "Microsoft: MRS - Bing Grand Challenge"
date: 2013-03-18 18:38
comments: true
categories: 
tags: 
---
*source:<http://acmmm13.org/submissions/call-for-multimedia-grand-challenge-solutions/msr-bing-grand-challenge-on-image-retrieval-scientific-track/>*  

### Grand Challenge on Image Retrieval: Scientific Track

The Second Microsoft Research (MSR)-Bing challenge (the “Challenge”) is organized into a dual track format, one scientific and the other industrial.  The two tracks share exactly the same task and timelines but independent submission and ranking processes.

For the scientific track, we will follow exactly what MM13 GC outlines at <http://acmmm13.org/submissions/call-for-multimedia-grand-challenge-solutions/>.  The papers will be submitted to MM13, and go through the review process.  The accepted ones will be presented at the conference. At the conference, the authors of the accepted papers will be requested to introduce their solutions, give a quick demo, and take questions from the judges and the audience.  Winners will be selected for Multimedia Grand Challenge Award based on their presentation.

The industrial track of the Challenge will be conducted over the internet through a website maintained by Microsoft. Contestants participating in the industrial track are encouraged to take advantage of the recent advancements in the cloud computing infrastructure and public datasets and must submit their entries in the form of publicly accessible REST-based web services (further specified below). Each entry will be evaluated against a test set created by Bing on queries received at Bing Image Search in the EN-US market. Due to the global nature of the Web the queries are not necessarily limited to the English language used in the United States. The details of the industrial track, including “Measurements and evaluation”, “Dataset”, “Submission” and “Awards” can be found [here](http://web-ngram.research.microsoft.com/GrandChallenge/).

Note that the “Task” for the two tracks is the same, while the submission, evaluation and awards are different, as summarized in the table below.  Teams can participate in either or both of the tracks.

| |Task| Measurements and evaluation | Dataset | Submission | Awards | 
|-|---| ----- | ---- | --- | --- |
|Scientific Track| See below  | research impact | Use entire or partial dataset | To conference as a paper  |  According to MM13 guidelines | 
| Industrial Track | See below |  See Industrial track link  | Use entire dataset | See industrial track link  | Ranked by measurements |
 

## Task

The topic of the Challenge is web scale image retrieval. The contestants are asked to develop systems to assess the effectiveness of query terms in describing the images crawled from the web for image search purposes. A contesting system is asked to produce a floating-point score on each image-query pair that reflects how relevant the query could be used to describe the given image, with higher numbers indicating higher relevance. The dynamic range of the scores does not play a significant role so long as, for any query, sorting by its corresponding scores for all its associated images gives the best retrieval ranking for these images.

## Dataset

The dataset for the Microsoft Image Grand Challenge on Image Retrieval can be downloaded [here](http://web-ngram.research.microsoft.com/GrandChallenge/Datasets.aspx).

## Contact

Yong Rui,    *yongrui -at- microsoft.com*  
Kuansan Wang,     *kuansan.wang -at- microsoft.com*