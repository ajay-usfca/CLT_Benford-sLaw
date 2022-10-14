# CLT_Benford-sLaw
Intro : 

In this ReadMe, we are going to talk about two topics : one is a requirement for classical CLT - independence, the other is a very interesting application of CLT - benford’s law

Independence 

One of the assumptions of traditional CLT is that the sample needs to be identical and independent. And we are going to focus on the independence criteria. The definition of independent is that two events are independent if the occurrence of one event does not affect the chances of the occurrence of the other event. 

For example, usually pulling cards from a stack is random, but if we can see the previous card, we will know that the probability of the next card will change, i.e if the current turn is a 10, the probability of the next card being a 10 will decrease and the probability of it being some other card will increase. Then how can we get independent events in terms of sending cards? Will there are several ways. One way is that we can choose not to see the cards. Another is that we can pulling cards from a stack that have a infinite number of cards.
 
One thing I want to mention is that don’t go too far from independent variables. Because the definition is very weak, the occurrence of one event does not affect the chances of other event, basically that is saying that we need to judge independence based on our intuition. Some universal thing, some thing that we assume that not usually happen, might happen, and it will affect our independence. if a plane crashed, the next plane might also crashed because there might be bad weather in the air. So be careful about independence.

Mathematical Interpretation

But, what is the mathematical interpretation of Independence. Especially, how can we tell if two given random variables (or any number of random variables) are independent or not. 

Just by knowing the individual distributions of the random variable, we cannot. We need to know their joint pdf to tell if they are independent or not. 

More specifically, two random variables or any number of random variables are independent if:
Their Joint PDF is a product of the marginal PDF’s 
The support set of the Joint PDF must be defined on a multi-dimensional rectangle 

But what does it mean for the joint PDF to be a product of the marginal PDFs or for the support set to be a “rectangle”. Let’s use a simple dataset to illustrate this. 
