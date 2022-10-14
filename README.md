# CLT_Benford-sLaw
**Intro : **

In this ReadMe, we are going to talk about two topics : one is a requirement for classical CLT - independence, the other is a very interesting application of CLT - benford’s law

**Independence **

One of the assumptions of traditional CLT is that the sample needs to be identical and independent. And we are going to focus on the independence criteria. The definition of independent is that two events are independent if the occurrence of one event does not affect the chances of the occurrence of the other event. 

For example, usually pulling cards from a stack is random, but if we can see the previous card, we will know that the probability of the next card will change, i.e if the current turn is a 10, the probability of the next card being a 10 will decrease and the probability of it being some other card will increase. Then how can we get independent events in terms of sending cards? Will there are several ways. One way is that we can choose not to see the cards. Another is that we can pulling cards from a stack that have a infinite number of cards.
 
One thing I want to mention is that don’t go too far from independent variables. Because the definition is very weak, the occurrence of one event does not affect the chances of other event, basically that is saying that we need to judge independence based on our intuition. Some universal thing, some thing that we assume that not usually happen, might happen, and it will affect our independence. if a plane crashed, the next plane might also crashed because there might be bad weather in the air. So be careful about independence.

**Mathematical Interpretation of Independence**

But, what is the mathematical interpretation of Independence. Especially, how can we tell if two given random variables (or any number of random variables) are independent or not. 

Just by knowing the individual distributions of the random variable, we cannot. We need to know their joint pdf to tell if they are independent or not. 

More specifically, two random variables or any number of random variables are independent if:
Their Joint PDF is a product of the marginal PDF’s 
The support set of the Joint PDF must be defined on a multi-dimensional rectangle 

But what does it mean for the joint PDF to be a product of the marginal PDFs or for the support set to be a “rectangle”. Let’s use a simple dataset to illustrate this. 

<img width="166" alt="image" src="https://user-images.githubusercontent.com/112677445/195774441-5ecc2c36-9fc1-4c5e-bd1c-182eda9aa9fe.png">

In this, let’s try to see if A and B are independent or not. 

This table is what one could call a “joint PDF”, as it gives us the probability of A being equal to some value and B being equal to some value at the same time i.e 
P(A=x and B=y). 

Now, how do we get the “marginal PDF”, you can get that by calculating the probability of each value in each of the columns and plotting it on a graph. Below is what that would look like for A and B: 

<img width="366" alt="image" src="https://user-images.githubusercontent.com/112677445/195774528-f693b70e-b458-4274-bec6-a0c214f0d5b8.png">

Now, let’s try to look at what a support set is. Support set for a random variable is simply put, all possible values for the random variable. So, when you roll a die, we know we can get any of the numbers ranging from 1 to 6 on the face of the die. So, {1,2,3,4,5,6} would be the support set for a die roll. Similarly, for a coin toss, if we treat getting a head as one and tail as 0, the support set would be {0,1}. 

Coming back to our example, support set in our case for both A and B would be {1,2}. But we need the support set of their joint PDF, i.e what are the possible values of A for each value of B or vice versa. We can see from the table that when A is equal to 1, B can have values of 1 or 2, the same is the case when A=2. If we were to plot that on a graph, it would look like below: 

<img width="365" alt="image" src="https://user-images.githubusercontent.com/112677445/195774614-2bd78c51-6cf0-4cd9-89df-f1ba3a8b57aa.png">

Clearly, the green dots which represent the support set of Joint PDF of A and B form a rectangle, which in simple english can be described as for every value of A, all values of B should be possible. 

Is this enough to call A and B independent? No, we need the other requirement i.e joint PDF to be product of marginal PDF’s to be satisfied. Now, how do we check that and what it means for the Joint PDF to be a product of marginal PDF.

It basically means that for each unique value of A (or B), the corresponding values in B (or A) should form a distribution that is same as the marginal distribution of B. We know the marginal distribution of B, which says that B has a 50% probability of being 1 or 2. So, when A=1, we need to check the probability of B being 1 or 2. We can see that it is 33% (for 1) and 66%(for 2). This clearly is not the same as the marginal distribution of B. So, we can say that A and B are not independent. 

It’s important to remember that what we are talking about here is theoretical independence and not statistical independence. Statistical independence is much weaker and requires just the correlation to be 0.


**Benford’s Law **

Now let’s look into an interesting application of Benford’s law.

Benford's law is an observation about the leading digits of the numbers found in real-world data sets. It states that the leading digit being 1 is more frequent than 2 and 2 more than 3 and so on.

<img width="389" alt="image" src="https://user-images.githubusercontent.com/112677445/195774693-ba4e1229-eca2-4e75-9182-cc9cedf2cef5.png">

More precisely, the probability of each occurrence having the leading number ‘d’ is

**Pr(d) = log(1+ 10/d)**


**Benford’s Law compliance:** 
Benford’s law is prominent when the data has several orders of magnitude, like exponential distribution. It needs the distribution to be widely spread. 

Examples that follow Benford’s Law:
Fibonacci series
Factorials
Powers of two

Examples that don’t follow Benford’s Law:
Lists of local telephone numbers 
Distributions that do not span several orders of magnitude will not follow Benford's law
	Ex: Height

**Leading digit of heights of the 58 tallest structures in the world **

<img width="474" alt="image" src="https://user-images.githubusercontent.com/112677445/195774773-8156ec63-ffb6-435b-89d2-38ad04d82371.png">

**Leading digit of 1st 100 elements of Fibonacci Series**

<img width="354" alt="image" src="https://user-images.githubusercontent.com/112677445/195774849-aba8c479-fe7a-4fe1-8a07-0bde003288e3.png">

**How is CLT related to Benford’s Law? **

Central limit theorem says that multiplying more and more random variables will create a log-normal distribution with larger and larger variance, so eventually it covers many orders of magnitude.

Log-normal distributions are positively skewed with long right tails due to low mean values and high variances in the random variables.

<img width="492" alt="image" src="https://user-images.githubusercontent.com/112677445/195774915-08e4acdf-c3a4-4231-a2d8-d17fba3badcf.png">

**Applications of Benford’s Law:**

1) Accounting fraud detection: Based on a plausible assumption that people who fabricate figures tend to distribute their digits fairly uniformly, a simple comparison of first-digit frequency distribution from the data with the expected distribution according to Benford's law ought to show up any anomalous results.
2) Criminal trials
3) Election data

