What am I doing?
========================================================
transition: rotate
transition-speed: slow
css: ../../IDSLabCSS.css

Unit 1 - Lab 9

Directions: Follow along with the slides and answer the questions in **red** font in your journal.



What am I doing?
================

- In this lab, you'll be analyzing your class' time-use data.
- Some reminders:
    - Remember to **share your data** using the [Web Front End](http://lausd.mobilizingcs.org/landing), if you haven't already. 
    - Look at **lab 1.6: Download, Upload, Load** for help loading your data.
    - Name your data **my_atus** to help distinguish it from the larger **atus** data set.
    
Formatting your data
==================== 

- Your data was collected over 5 days
    - We'll average how each person spent their time over those 5 days.
    - This lets us make comparisons with you and your classmate's **typical** day.
- To format your data (assuming you named it **my_atus**), type the following command:

```r
new_atus <- atus_format(my_atus)
```

Get aquainted with the data
===========================

- Now that your data has been formatted, let's take a look at it

```r
View(new_atus)
```

- **How many observations are in your data?**
    - **How many students are in your class?**
- **Compare the values of _grooming_ for the first two observations**
    - **Who _typically_ spent more time grooming?**
    
And away you go...
==================

- Using the techniques you've learned thus far:
    - **Pick a 3-4 variables to investigate**
    - **Create approriate single variable plots and interpret them.**
    - **Create appropriate multiple variable plots and interpret them.**
    - **Tally some frequency tables and make some conclusions about your classes data**.
- **Write down a fact from your analysis you found most interesting and why.**