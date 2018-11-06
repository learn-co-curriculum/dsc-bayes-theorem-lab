
# Bayes' Theorem - Lab

In this lab, we shall try to put some of the formulas to practice that we came across with in the previous lesson. 

## Objectives
* Understand and describe the Bayesian theorem from conditional probabilities
* Describe the roles of Prior, Likehood and Posterior components of Bayes Theorem 
* Understand and perform simple applications of Bayes Theorem for sensitivity and specificity


## Exercise 1
### If a single card is drawn from a standard deck of playing cards, What is the probability of seeing a king ?


```python
# the probability that the card is a king is 4/52, since there are 4 kings in a standard deck of 52 cards. 
#Rewording this, if  is the event "this card is a king," the prior probability: 
p_king = 4/52 
p_king
```




    0.07692307692307693



### If evidence is provided (for instance, someone looks at the card) that the single card is a **face card**, what would be the posterior probability according to Bayes theorem?


```python
# The posterior probability P(king|Face)can be calculated using Bayes' theorem as

# P(king|face) = P(face|king)P(king) / P(face)

# We also know P(face|king) = 1, as every king is a face card

p_face_given_king = 1

# Since there are 3 face cards in each suit (Jack, Queen, King) , the probability of a face card is P(F) = 3/13
p_face = 3/13

p_king_given_face = p_face_given_king* p_king/p_face
p_king_given_face
```




    0.3333333333333333



## Exercise 2
#### 1. A couple has two children, the older of which is a boy. What is the probability that they have two boys?
#### 2. A couple has two children, one of which is a boy. What is the probability that they have two boys?


```python
# Explain events as:
# A = both children are boys
# B = older child is a boy 
# C = One of the children is a boy 
```


```python
# Part 1
# we need P(A|B)

p_a = 1/4
p_b = 1/2
p_b_given_a = 1

p_a_given_b = p_b_given_a*p_a/p_b
p_a_given_b
```




    0.5




```python
# Part 2 
# We need P(A|C)

# we need P(C) i.e. prior prob. that couple has two boys , which is equal to (1-p_both_girls)
p_c = 1 - 1/4
p_c_given_a = 1

p_a_given_c = p_c_given_a*p_a/p_c
p_a_given_c
```




    0.3333333333333333



## Exercise 3 - Bayesian Disease Diagnosis

[Visit this link for an insight into Bayesian Disease Daignosis](http://doingbayesiandataanalysis.blogspot.com/2013/01/bayesian-disease-diagnosis-with.html)



A disease test is advertised as being 99% accurate 

* If a patient has the disease,they  will test positive 99% of the time.

* If you don't have the disease, they will test negative 99% of the time. 

* 1% of all people have this disease 

#### Now a patient tests positive, what is the probability that you actually have the disease?


```python
# By Bayes' Theorem, the probability you have the disease is

#P(D|Pos) = P(Pos|D)* P(D) / P(Pos) 

# P(Pos) is calculated as :
# You either don't have the disease and tested incorrectly (0.1*0.99), 
# or you don't have the disease and tested incorrectly (0.99 *0.1). 


p_pos = (0.01*0.99) + (0.99 *0.01)

p_d_given_pos = 0.01 * 0.99/p_pos
p_d_given_pos
```




    0.5



## Summary 

In this lab, we saw a few simple examples of Bayesian logic and how we can add prior information to our calculation, in order to update our beliefs about the certain events. Bayesian logic works in numerous ways and it is not within the scope of this section to give you a deep dive in complex Bayesian problems. You are advised to re-visit the provided links when you have a better understanding of Bayesian inference. 
