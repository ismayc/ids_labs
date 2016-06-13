What's your status single?
==============
transition: rotate
transition-speed: slow
css: ../../IDSLabCSS.css

Unit 1 - Lab 2  

Directions: Follow along with the slides and answer the questions in **red** font in your journal.



Where'd we leave off ...
==================

- The first lab ended... 

<img src="unit1lab2-figure/unnamed-chunk-2.png" title="plot of chunk unnamed-chunk-2" alt="plot of chunk unnamed-chunk-2" style="display: block; margin: auto;" />

***

... with these two plots:

<img src="unit1lab2-figure/unnamed-chunk-3.png" title="plot of chunk unnamed-chunk-3" alt="plot of chunk unnamed-chunk-3" style="display: block; margin: auto;" />

Where'd we leave off ...
==================

- This plot has an x-axis with numbers

<img src="unit1lab2-figure/unnamed-chunk-4.png" title="plot of chunk unnamed-chunk-4" alt="plot of chunk unnamed-chunk-4" style="display: block; margin: auto;" />

***

- This plot has an x-axis with categories

<img src="unit1lab2-figure/unnamed-chunk-5.png" title="plot of chunk unnamed-chunk-5" alt="plot of chunk unnamed-chunk-5" style="display: block; margin: auto;" />


Interesting...
==============

- We know then that data comes in _at least_ two different varieties.
- **Numerical variables** have values that are typically measured in units
    - Ex: Feet, inches, pounds, hours, sodas per day, etc.
- **Categorical variables** have values that describe what category the observation belongs to.
    - Ex: Heads or tails, red, green or blue.


Before we start!
================

- Load the CDC data from before by using the following command in the console.
    - Remember how to load this data set for future labs.


```r
data(cdc)
```


Categorical Variables
=====================

- Have _values_ that describe the _category_ an observation belongs to
- For example, view your data by typing `View(cdc)` into the console.
    - Find the `gender` of the first person in the data.
    - Which _category_ of `gender` does the person belong to?
    
Categorical Variables
=====================
- Now type the following command into the console to view the names of the variables.

```r
names(cdc)
```
- **Write down 3 variables that you think are _categorical_ variables and why you think that they're categories**
- **View your data and write down the different _values_ (or categories) for each of the 3 variables you chose**

Bargraphs, a.k.a. Barplots
==========================

- _Bargraphs_ are one of the best ways to _visualize_ categorical variables.
    - One axis (x or y) will have the different categories.
    - The other axis will have the number of observations (or _Frequency_) that fall into each category.
- Type the following into the console to create a bargraph (Hit the _Zoom_ button in the plot pane to make it larger).

```r
bargraph(~helmet, data = cdc)
```
- **Explain what the values on the x and y axis mean. Which categories occured the most & the least often?**

More on Bargraphs
=================

- Bargraphs are sometimes easier to read when the bars are horizontal.
    - Run the following command (Make sure to spell `TRUE` in all capital letters):

```r
bargraph(~helmet, data = cdc, 
         horizontal = TRUE)
```
- **In your opinion, are the vertical bars or horizontal bars easier to read for visualizing the `helmet` data. Why do you think that?**

More on Bargraphs
=================

- We also sometimes want to _split_ each bar in our plot by _grouping_ them into seperate categories.
    - Run the following command to `group` the bars for each category based on each person's `gender` 

```r
bargraph(~helmet, data = cdc, 
         groups = gender, 
         horizontal = TRUE)
```


Your turn
=========

- **Practice making AND interpretting bargraphs using all three of the categorical variables you chose earlier in the lab**
    - **Choose a different categorical variable if you previously chose `helmet`.**
- **Interpret each graph by explaining:**
    - **What the categories are**
    - **Which categories occured more or less often**
- **Be sure to point out any interesting discoveries you make**



Numerical Variables
===================

- Have _values_ that are _measured_ in _units_.    
- For example, view your data by typing `View(cdc)` into the console.
    - Find the `height` of the first person in the data.
    - How tall is this person? What do you think are the units?
    

Watch out!
==========

- Sometimes variables that you think would be _numerical_ are actually _categorical_.
    - You might think that `age` is _numerical_ because it can be measured in _years_.
- View the values of people's ages in the CDC data by running `View(cdc)` again.
    - Since the values contain the words "years old", R inteprets these values to be categories!

Numerical Variables
===================

- List the `names` of the variables again (You can go back to look up the command if you've forgotten)
    - **Write down 3 variables that you think should be _numerical_ variables**
    - **List some possible units of measurements for each variable.**
- View your data
    - **Write down any variables you thought were numeric but were actually categorical (See the warning on the previous slide for help)**


Histograms!
===========

- Just like how we used **bargraphs** to visualize _categorical variables_, histograms are useful for visualizing _numerical variables_
- Type the following to make a histogram for people's `height`


```r
histogram(~height, data = cdc)
```

- **What do the values of the x-axis mean in terms of people's `heights`?**
- **What do the _widths_ of the bins mean?**
- **What does the _height_ of each bar represent?**

More on Histograms
==================

- By changing the width of the _bins_ of a histogram, we can change the amount of detail it shows.
    - Wide bins give us a very broad view of the data.
    - Narrow bins give us a very detailed view.
- A good histogram should strike a balance between being both wide & narrow

More on Histograms
==================

- Run the following commands:

```r
histogram(~weight, data = cdc, 
          nint = 3)
```


```r
histogram(~weight, data = cdc, 
          nint = 30)
```

- **What would you say is the typical weight of these people? How do you think this compares to your class?**
- **Is it unusual to weight less than 65 kilograms? Why?**
- **Fill in the blanks: Most people weight between ___ and ____ kilograms. Explain how you chose your values.**
    
