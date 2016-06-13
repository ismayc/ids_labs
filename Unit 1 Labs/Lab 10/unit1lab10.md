Time Match Dot Com
========================================================
transition: rotate
transition-speed: slow
css: ../../IDSLabCSS.css

Unit 1 - Lab 10

Directions: Follow along with the slides and answer the questions in **red** font in your journal.



How do we compare?
==================

- For this lab, we'll be comparing how your class spends their time versus how other Americans spend their time.
- **Load the full American Time Use Survey**

```r
data(atus)
```
- **load your own class' data and call it `my_atus`**.
- Run the following command again to format our data

```r
new_atus <- atus_format(my_atus)
```

What does atus_format do again?
===============================

- The function `atus_format` takes every individual student's data and takes the average of how they spent their time over 5 days.
    - This let's us see how a student spends a **typical** day.
- Every class member will be a single observation in `new_atus`.
    - This is similar to how different individuals are the observations for the larger `atus` data.
    
Let the comparisons, begin!
===========================

- Using what you've learned in prior labs, make comparisons between how your class spends it's time versus how Americans in general spend their time:
- Suggestions
    - **Find some variables that are in both data sets**
    - **How do the typical values for your class compare to Americans in general?**
    - **Create plots of each groups variables. How are they similar? Different?**
    
    
Watch out! 
==========

- You might want to `subset` your data so you compare apples to apples. 
    - For instance, not all Americans are in school, and so will spend 0 minutes doing homework.
    - It would be better to make comparisons using just the subset of the data of people who did at least 1 minute of homework.
    - Then you can compare how much time your class spends on homework against other people who also spend at least some time doing homework.
    
And away you go:
================

- Using what you've learned so far, make comparisons between your classes data and the full ATUS data by using:
    - **Single variable plots**
    - **Multiple variable plots**
    - **2-way frequency tables**
- Answer the following:
    - **How is your classes time use similar to other Americans?**
    - **How is your classes time use different from other Americans?**
- Share your findings with a partner
    - **Did your partner make appropriate plots?**
    - **Did your partner make appropriate conclusions?**