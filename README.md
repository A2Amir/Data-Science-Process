# Introduction

This Repo is about the process used for many data science problems. This will serve us as a useful guide on how to approach future data science problems.
 
Given the large number problems that fall under the umbrella of Data Science and there are a lot of different tools and individual nuances of  a particular company or industry for finding solutions. 

However, there's actually a common process used to find many solutions in Data Science. This process is known as the **Cross Industry Standard Process for Data Mining or CRISP-DM**. This process has been an industry standard for analyzing data for years and it has six major phases. 

##
1. Developing business understanding. 
2. Developing data understanding. 
3. Preparing the data to be analyzed. 
4. Modeling the data. 
5. Evaluating the results to answer the questions of interest 
6. Deploying changes based on the results of the analysis. 

##
I will look at each of these phases a bit closer in upcoming sections.


## 1. Business & Data understanding

In this section I am going to take a look at the first two steps of the CRISP-DM process in a bit more detail. First, CRISP-DM says I need business understanding, meaning understanding the problem. For examples each of these questions falls under business understanding. 

* Are you interested in acquiring new customers? 
* Are you interested in assessing of a new cancer treatment outperforms existing treatments? 
* Are you interested in finding a better way to communicate? 


The second step of the CRISP-DM process is data understanding. This means I need to gain an understanding of the data necessary to answer the question. Sometimes I might have a mountain of data at my disposal that I need to dig through to find insights. 

<p align="right">
<img src="./imgs/1.png" alt="" width="500" height="400">
</p>


Other times I may need to collect data, which means I will have to understand what kind of data I'll be able to provide with the insights I need (meaning to answer the question I should collect data). This is often difficult to know ahead of time, which is why businesses tend to collect all the data they can first, so they can later identify which data they need to use to find their insights. 



throughout this repo, I will get hands-on practice with two datasets from Stack Overflow developer survey results, from 2017. [This dataset](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/survey_results_public.csv) can provide some insight to developers around the world and get an idea of their experiences. Anything from their advice to other developers, to how they learn new skills, to where they live, or what programming languages they use, can all be understood from this dataset.


## Business & Data Understanding – Example

In the rest of this Repo I will be using the following business questions and Stackoverflow survey data to to answer these questions.
##### Business Questions

1.	what do those employed in industry suggest to help others enter the field? (How do I break into the field?)
2.	What are the placement and salaries of those who attended a coding bootcamp?
3.	How well can we predict an individual's salary? What aspects correlate well to salary?
4.	How well can we predict an individual's job satisfaction? What aspects correlate well to job satisfaction?

##### Data Understanding

I will be using the Stackoverflow survey data to get some insight into each of these questions. In order to get a better understanding of the data you can take a look at some of the characteristics of the datasets by checking [this exercise](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/A%20Look%20at%20the%20Data.ipynb). 


## 2. Data Preparation: Gathering & Wrangling

In the previous section were introduced the four questions that I will focus on while working on the remaining steps in the CRISP-DM process. 

The next step in the process is about gathering the data and organizing it in a way that will allow us to answer our business questions. Fortunately Stack Overflow already gathered the data. The wrangling and gathering  process is said to be the most time-consuming, often taking 80 percent of the data analysis process. 

* First, check [this exercise](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/How%20To%20Break%20Into%20the%20Field.ipynb) to take a look at the datasets and see how I might answer the first question about how to break into the field of becoming a developer according to the survey results. 

* Then check this [exercise](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/Bootcamps.ipynb) to see how I answered the second question about the placement and salaries of those who attended a coding bootcamp.

* Third, in this [notebook](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/Job%20Satisfaction.ipynb), I am going to look at  job satisfaction according to the survey results.


As you may have already noticed from answering the first two questions, not every data science problem involves the fanciest deep learning or machine learning algorithm.In the [first](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/How%20To%20Break%20Into%20the%20Field.ipynb) [two](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/Bootcamps.ipynb) nootbooks I only used descriptive and a little inferential statistics to retrieve the results.

Therefore, all steps of CRISP-DM were not necessary for these first two questions. CRISP-DM states 6 steps:


1. Business Understanding
2. Data Understanding
3. Prepare Data
4. Data Modeling
5. Evaluate the Results
6. Deploy

For these first two questions, I did not need step 4. In this [notebooks](https://github.com/A2Amir/Data-Science-Process/blob/master/Code/How%20To%20Break%20Into%20the%20Field.ipynb), I performed steps 3 and 5 without needing step 4 at all. A lot of the hype in data science, artificial intelligence, and deep learning is integrated into step 4, but there are still plenty of questions to be answered not using machine learning, artificial intelligence, and deep learning.

**All Data Science Problems Involve**

1.	Curiosity.
2.	The right data.
3.	A tool of some kind (Python, Tableau, Excel, R, etc.) used to find a solution (You could use your head, but that would be inefficient with the massive amounts of data being generated in the world today).
4.	Well communicated or deployed solution.

**Extra Useful Tools to Know But That Are NOT Necessary for ALL Projects**

5. Deep Learning
6. Fancy machine learning algorithms

With that, you will be getting a more in depth look at these items, but it is worth mentioning (given the massive amount of hype) that they do not solve all the problems. Deep learning cannot turn bad data into good conclusions. Or bad questions into amazing results.


# 3. Modeling

By solving the first two questions, I understood I did not need to do any predictive modeling. I only used descriptive and a little inferential statistics to retrieve the results. Therefore, all steps of CRISP-DM were not necessary for these first two questions.
However, for the last two questions:

1.	How well can we predict an individual's salary? What aspects correlate well to salary?
2.	How well can we predict an individual's job satisfaction? What aspects correlate well to job satisfaction?
I will need to use a predictive model. I will need to pick up at step 3 to answer these two questions,

Predictive models are one type of machine learning algorithm, known as supervised machine learning. A simplified four-step process for modeling using scikit-learn is to 

* First instantiate the model. 
* Second, to fit the model to the training data. 
* Third, predict using the fitted model on some test data and then 
* Finally score the model using a metric to evaluate how well it performs. 

I might use modelling to predict salary for an individual in this data set but a quick look through the dataset shows a number of factors that should be able to help me better understand more about an individual salary. 

They're **quantitative factors** like:
 
* The number of hours a week and individual works 
* How satisfied they are with their job or their career. 

They're also **categorical variables** like:
 
* The country they live in 
* Their company size 
* Their formal education. 

When building supervised machine learning models, I am looking for a way to take all of these inputs and predict an individual value in this case, the individual salary. 

