
# Bayes' Theorem - Lab

## Introduction

In this lab, you'll practice Bayes' Theorem in some simple word problems. 

## Objectives
In this lab you will be able to: 

- Use Bayes' theorem to determine the probability of specific events 

## Define a custom function for Bayes' theorem

To start, write a function, `bayes()`, which takes in the probability of A, the probability of B, and the probability of B given A. From this, the function should then return the conditional probability of A, given that B is true.


```python
def bayes(P_a, P_b, P_b_given_a):
    # Your code here
    return P_a_given_b
```

## Skin Cancer

After a physical exam, a doctor observes a blemish on a client's arm. The doctor is concerned that the blemish could be cancerous, but tells the patient to be calm and that it's probably benign. Of those with skin cancer, 100% have such blemishes. However, 20% of those without skin cancer also have such blemishes. If 15% of the population has skin cancer, what's the probability that this patient has skin cancer? 

> Hint: Be sure to calculate the overall rate of blemishes across the entire population.


```python
# Your code here
```

    0.46875


## Children (I) 

A couple has two children, the older of which is a boy. What is the probability that they have two boys?


```python
# Your solution P(2boys|older child is a boy)
```




    0.5



## Children  (II)

A couple has two children, one of which is a boy. What is the probability that they have two boys?


```python
# Your solution P(2boys|1 of 2 children is a boy)
```




    0.3333333333333333



## A diagnostic test

A diagnostic test is advertised as being 99% accurate 

* If a patient has the disease, they  will test positive 99% of the time 

* If they don't have the disease, they will test negative 99% of the time  

* 1% of all people have this disease 

If a patient tests positive, what is the probability that they actually have the disease?


```python
# Your solution P(Disease | positive test)
```




    0.5



## Summary 

In this lab, you practiced a few simple examples of Bayesian logic and how you can add prior information to update your beliefs about the chance of events.
