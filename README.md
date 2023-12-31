![image](https://github.com/info201a-su23/assignment-02-info201su-sc100922/assets/139248633/4b8703fa-1870-4505-9581-87a76a14a6bb)
# Assignment 2: Protests
In recent years the United States has experienced a surge of protests, in support of Black Lives Matter, gender equity, and many other social or political issues.

In this assignment, you will work with data from [Count Love](https://countlove.org/), data that is ocassionally [cited](https://www.nytimes.com/2020/08/28/us/black-lives-matter-protest.html) by the _New York Times_ when reporting on US demonstrations.

Through this assignment, you will be able to answer questions about protests, including:

* What were the most attended and least attended protests in the US in the last 5 years?
* How many protests occurred in Washington state?
* How did the number of protests in 2019 compare to 2020, and why?
* Why are people protesting in the US? What are the biggest motivators?

## Learning objectives
By completing the assignment, you will develop or skills for:

- **Version control** tools for managing code (git and GitHub)
- Writing documents with **markdown** syntax
- Coding in R
- Thinking critcally about data.

# 1. Critical Analysis & Reflection: Before You Code

Before diving into this (or any) dataset, it's important to know where the data came from, and it's important to have or to seek out _domain familiarity_ — that is, knowledge about the topic of the dataset. Sometimes the topic is very narrow; more often it is expansive, as in the case of CountLove. We don't want to be "strangers in the dataset," as Catherine D'Ignazio and Lauren Klein describe it. To get more familiar, we are going to begin by doing some background reading.

**Note:** Please write your answers below under the heading "Your Responses and Reflections."

- First, please read [this FAQ](https://countlove.org/faq.html) from the CountLove website and the opening of [this blog post](https://www.tommyleung.com/countLove/index.htm).
**(R1a)** Based on the information in these pieces, why did the creators start collecting the CountLove data?
  
  It’s easy to lose track of where and when protests took place and how many people participated. Additionally, searching individual records is difficult. The creators hope that keeping a record of demonstrations accessible helps people make more compelling cases for a diverse, empathetic, and kind country.


- Next, we would like you to read this [New York Times piece that uses CountLove data](https://www.nytimes.com/interactive/2020/06/13/us/george-floyd-protests-cities-photos.html) and that describes the Black Lives Matter protests that occurred in the summer of 2020.
**(R1b)** Please summarize the main point or argument of this article.
  
  This article is about how Black Lives Matter protests spread in America. The death of a black man, Floyd, due to police brutality aroused anger, so people decide to protest against the racial discrimination against black people. This voice has spread to every corner of the United States.

Next, we're going to reflect about who collected this data, and what's actually inside it. 

**(R1c)** Who collected and shared the CountLove data, and what do they do for a living?

Tommy Leung and Nathan Perkins, are engineers, and scientists with a keen interest in civic responsibility and public policy. They make a living from others who cite their data sets for publication, and they use the data themselves for publication.


**(R1d)** As Klein and D'Ignazio remind us, when it comes to data, "what gets counted counts." What types of demonstrations does CountLove include in their data, and what types do they exclude? 

They count public displays of protest that are not part of “regular business.” They typically do not include awareness events, commemorative celebrations, historic reenactments, fundraising events, town halls, or political campaign rallies.


**(R1e)** How and where does CountLove get their data about the protests? 

They crawl local newspaper and television sites on a daily basis, and most of the protest data come from these crawls. The dataset covers protest events in the United States between January 20, 2017, through January 31, 2021.

**(R1f)** How does CountLove make their estimates about the number of people who attended a protest? What potential problems might arise from this method of estimation? 

They record the most conservative attendance number from the news articles. They interpret “a dozen” as 10, “dozens” as 20, “hundreds” as 100, and so forth. If an article does not include an attendance count, they leave the count empty. It is an approximate number and not accurate enough.

**(R1g)** What are two central values of Count Love? Name and briefly describe them. (See the Envisioning Cards for a defintion of "value".)

Two central values of Count Love are civic responsibility and public policy. Count Love embodies these values by recognizing and highlighting the power of protests and demonstrations as a means of communication and expression for citizens to voice their concerns, advocate for their rights, and influence public policy decisions.


**(R1h)** Name and briefly describe one direct stakeholder and one indirect stakeholder (See the Envisioning Cards)? 

Count love creators is the direct stakeholders because they are directly influenced. The government officers and elected presidents would are the indirect stakeholders since the protests occur because of the raised problem in the specific areas that the government or presidents are responsible for.


# 2. Coding in R: Parts 1-6
**Instructions**. Assignment instructions and prompts are in this file: [analysis.R](analysis.R).

**Coding and reflection prompts**. You will find two kinds of prompts in [analysis.R](analysis.R):

* *Coding prompts*, which prompt you to write R code in [analysis.R](analysis.R).
* *Reflection prompts*, which prompt you to think and write in English below, in this file (README.md).

**Formatting Your Responses and Reflections**.

* When formatting your written responses and reflections below, please *retain* all
reflection prompt IDs (e.g., R1a, R2a, etc.).
* Fill in the elipses (...) with your own words. 
* Remove expected word counts.
* To write clearly, use markdown code appropriately (e.g., **bold**, _italics_, and `code`). As appropriate, include images, links, and so forth.

**Questions?** As always, please post on Teams or ask your Instructor or Teaching Assistant.

:computer: Good coding!
   :writing_hand: Good critical thinking!
      :smile: Good-luck!

(_Updated: October 2022, Your Teaching Team_)
**(R3a)**

I think the number of protests in Washington surprises me a lot. Because it is really a large number compared to other states that have large populations but fewer protests number.

**(R3b)**
Using the sapply() function is surprised me since it is power to simplifies the process of applying a function to multiple elements by automatically iterating over the elements and returning the results as a vector or matrix. It saves me a lot  of time.

**(R3c)**
I notice there are some outliers in the table that have very low numbers such as CE and TE only have 1. We can use data cleaning and exclude them to avoid bias.


# 3. Critical Analysis & Reflection: After You Code

In the second chapter of *Data Feminism*, Klein and D'Ignazio describe 4 ways that data scientists can challenge power and take action:
> Taking action can itself take many forms, and in this chapter we offer four starting points:  
> (1) Collect: Compiling counterdata—in the face of missing data or institutional neglect—offers a powerful starting point as we see in the example of the DGEI, or in María Salguero’s femicide maps discussed in chapter 1.  
> (2) Analyze: Challenging power often requires demonstrating inequitable outcomes across groups, and new computational methods are being developed to audit opaque algorithms and hold institutions accountable.  
> (3) Imagine: We cannot only focus on inequitable outcomes, because then we will never get to the root cause of injustice. In order to truly dismantle power, we have to imagine our end point not as “fairness,” but as co-liberation.  
> (4) Teach: The identities of data scientists matter, so how might we engage and empower newcomers to the field in order to shift the demographics and cultivate the next generation of data feminists?  

**(R1h)** How does the CountLove project embody one or more of these 4 forms of challenging power?

Count Love embodies the point of collection. This dataset records many informal, neglected protests, which can be used as cited evidence to support the article's claims. Count Love also embody analysis because it contains many datasets on protests that have a lot to do with inequality and human rights. Therefore, through these data, people can learn about the injustices of different races and challenge authority. Count Love can also serve as a platform to stimulate people's interest in data collection, let more people know the significance and value of this action, play a teaching role, train more data scientists, and devote themselves to the road of calling for equality and justice.

**(R1i)** What is the most interesting or surprising thing you learned from this analysis? Please answer in at least 2-3 sentences (2 points)
I think data analysis is a meaningful thing. In the past, my data analysis was limited to mathematical analysis, and it was rigorous. And now I think that analysis can be linked to other aspects of life such as ethics, which is amazing to me.

**(R1j)** What is a kind of analysis that you would like to do or that would be interesting to do with the CountLove data that you don't have the time or skills to accomplish at this moment? Please answer in at least 2-3 sentences (2 points)

I am very interested in data that records the protests for natural environment protection because environmental protection is a very meaningful topic. Only when more people realize and pay attention to this issue, environmental protection can be implemented more effectively. However, I have not had time to study these data.

## Your Responses and Reflections

### Critical Analysis & Reflection: Before You Code (questions above)

* **(R1a)** ... (about 25-50 words)
* **(R1b)** ... (about 25-50 words)
* **(R1c)** ... (about 25-50 words)
* **(R1d)** ... (about 25-50 words)
* **(R1e)** ... (about 25-50 words)
* **(R1f)** ... (about 25-50 words)
* **(R1g)** ... (bullet points fine; about 50 words)
* **(R1h)** ... (bullet points fine; about 50 words)

### Part 3: Locations (`analysis.R`)
* **(R3a)** ... (about 25-50 words)
* **(R3b)** ... (about 25-50 words)
* **(R3c)** ... (about 25-50 words)

### Critical Analysis & Reflection: After You Code (questions above)
* **(R7h)** ... (100 words or more)
* **(R7i)** ... (50 words or more)
* **(R7j)** ... (50 words or more)
