# Stocks Analysis

## Overview of Project
In this project we are analyzing the total daily trading volume and return of twelve different stocks for 2017 and 2018.  The code we have written will prompt the user to enter the year they desire to look at (either 2017 or 2018) and will generate the results on a different worksheet than the data with conditional formatting for easier analysis.

## Results
From our analysis we can see that all stocks analyzed did worse in 2018 than they did in 2017.  Only two stocks (ENPH and RUN) showed positive returns both years.  However, only one (TERP) showed a negative return both years.

Our original code held the starting and ending price variables as Double, whereas in the new code they were held in arrays as Single - using less memory and speeding up the subroutine.

Original:
    'Initialize varialbes for the starting and ending prices
    Dim startingPrice As Double
    Dim endingPrice As Double

Refactored:
    '1b) Create three output arrays
    Dim tickerVolumes(12) As Long
    Dim tickerStartingPrices(12) As Single
    Dim tickerEndingPrices(12) As Single

Refactoring our code allowed the script to run significantly faster:

2018 .5859 seconds vs .2617 seconds
![image](https://github.com/kchavez05/stock-analysis/blob/main/Resources/VBA_Challenge_2018.PNG) 
2017 .5703 seconds vs .1797 seconds
![image](https://github.com/kchavez05/stock-analysis/blob/main/Resources/VBA_Challenge_2017.PNG)
 
## Summary
1. What are the advantages or disadvantages of refactoring code?
    One clear advantage is that it can allow the code to run faster.  It also allows a second developer to get their eyes on the code to see if there are any redundancies, or ways the code could be re-written to make it more efficient.  A disadvantage could be that the original developer wrote the code a particular way for a particular reason, but failed to comment on it so a change could cause issues down the line.
2. How do these pros and cons apply to refactoring the original VBA script?
    Obviously after we refactored the script it was able to run faster.  I do not see any cons of refactoring the code in this particular instance.  We were able to make it run more efficiently and use more well defined variables rather than just "i" and "j"