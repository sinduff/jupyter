# Fundamentals of Data Analytics
### Fundamentals of Data Analytics Tasks Assignments 2020 
Submited by Sinéad Duffy, Student ID - 10016151

Before any coding can begin, it is necessary to import selected libraries from the Python Standard Libaries.  The following libaries were imported

**For calulations:**
- Pandas
- Numpy,
 - Numpy.random, specifically default_rng which was defined as a global variable for use throughout the notebook

**For Plotting:**
- Seaborn
- Matplotlib
 - also included was the 'magic' code *%matplotlib inline* to show the graphs. 

The cell containing the python libaries must be run first, before any of the tasks are attempted.

A brief explanation of each task, including the code used in outlined below.

#### Task 1 - Create a function called counts
**Ask** - create a function called *counts* to take a list as input and return a dictionary of the number of unique items in that list

**Text Cell** - an explanation of the task is contained here.  The cell goes on to outline the different steps that were undertaken to complete the task.  The steps are explained in terms of input / process and output.

References that were used throughout this section are included at the bottom of the cell.

**Code Cells**
*Cell 1* - the first cell of this task contains a function called *counts*.  The function takes in the value of a string, and returns a count of the instances of the characters in the string.  

The steps of the function are:
1. open a blank dictionary called instanceOfChar
2. start a for look on the string passed into the function, and look for an instance 'i'
3. if 'i' is already in the instanceOfChar;
4. add 1 to the total of 'i'
5. otherwise
6. add a new instance of 'i' to the instanceOfChar dictionary, i.e. a new character.
7. return the contents of the dictionary 'instanceOfChar'

*Cell 2* - This cell contains the code to accept user input into the program.  the input is then formatted (by changing to lowercase characters, and by removing any spaces between words).  The string is then passed to a 'print' command, which als callsed the function *counts*.  The output is printed to the screen as an array of characters, with the count value also appearing.

#### Task 2 - dicerolls function
**Ask** - create a function called *dicerolls* to take in two parameters, the number of dice *k*, and the number of times to roll the dice *n*.  Randomly simulate rolling the *n* dice *k* times.  Return a dictionary with the number of possible total face vlaue occured.

**Text Cell** - a detailed explanation of the task is contained here.  The cell goes on to outline the different steps that were undertaken to complete the task.  The steps are explained in terms of input / process and output. The variables that are passed to the function are defined here also.

References that were used throughout this section are included at the bottom of the cell.

**Code Cells**
*Cell 1* - describes the code used to create the function called *dicerolls*. 

The steps of the function are:
1. pass into the function values for
    - **x** is the number of rolls to be made
    - **k** is the number of dice that are to be rolled
    - **DiceRange** the number of potential values that can be rolled, i.e up to 6, 12, 18 etc, depending on the number of dice chosen
2. create an empty dictionary object called *DiceResults*
3. roll the dice x number of times (as defined by the user)
4. calculate the random value of the roll (using a range of 1 to DiceRange)
5. if the result in is in the array add one
6. otherwise .. add the value to the array and add one
7. Sort the value of *DiceResults* by using the Lamdba X: function
8. return the value of *DiceResults*

*Cell 2* - gets the user input for number of rolls and dice to be rolled, and calls the function *dicerolls*.  The resulting dictionary is then printed to the screen.

The variables are defined at the start of the cell, and take in the user input.  The input values are integers.  The variable *DiceFace* defines that a 6 sided dice must be used.  Future versions of the code can also take in user input to define the number of faces on the dice.

The print statement at the end of the cell calls the *dicerolls* function, passed in the defined variables, and prints the returned dictionary fto the screen.

#### Task 3 - Binomial Distribution, Flipping a coin X number of times
**Ask** - flip a coin 100 times, then repeat for 1,000 flips of the coin.  Plot the results 

**Text Cell** - an explanation of the Binomial Distribution is defined and outlined here.  The global variable *rng* defined in the Libaries above is called in the code section.  

The cell goes on to outline the steps the inputs - which are defined by the task, and not by user input.  The process of 'flipping the coin' is explained in teh following section.  How the output is displayed using Matplotlib is detailed in Step 3.  The refrences used to complete this task are outlined at the end of the cell.

**Code Cells**
*Cell 1* - defining the parameters of the experiment namely;
- *noFlips* - number of times that the coin is to be flipped
- *prob* - the probability of how many times 'heads' will be the result.  This is set to 0.5 or 50% of the time
- *sampleSize* - is the number of times that the program is to be run

Next, the code used to return data using the binomial function is outlined.  Finally, an array to store the results of the probabilty of x heads in each 100 flips of the coin is opened.

*Cell 2* - Outlines how the results of the code in Cell 1 is plotted / graphed.  The results are plotted using MatplotLib.

*Cell 3* - outlines an unfinished attempt by the author to plot the results of Cell 1 using the Seaborn package.  The author ran out of time to complete this section.

#### Task 4 - Simpson's Paradox

**Ask** - Create **four data sets**, each with an x array and a corresponding y array, to demonstrate Simpson’s paradox. You might create your **x arrays using numpy.linspace** and create the **y array for each x using notation like y = a * x + b** where you choose the a and b for each x , y pair to demonstrate the paradox.

**Text Cell** - Simpson's Paradox is outlined in the first section of this cell.  The author goes on to outline the scenario that is to be used to demonstrate Simpson's Paradox.  The scenario is flights to Shannon Airport from Dublin and Knock Airports.

*Step 1* of the task relates to the creation of the data for the task.  The variables used are:

*x* is calculated using the *numpy.linspace* calulation.  This is the random data for the task.
*y* is calculated using the **y = a * x + b** notiation as outlined in the Task brief.  
*Coefficient* is created using *np.polyfit*, where the valuses of *x* and *y* are passed to it.

Two datasets are created, one each for Knock Airport and Dublin Airport respectively. Each dataset is given a number 1 or 2, with the combined data being called *x* and *y* respectively. 

*Step 2* - combine the datasets to show Simpons Paradox, and plot the results.  The resulting plot displays Simpson's Paradox.

The refrences used in the code are outlined at the end.

**Code Cells**
*Cell 1* - creates dataset 1 for flights from Dublin Airport to Shannon Airport.  The variables used are;
- x1 = total flights
- y1 = flight delayed
- Coefficient1

*x1*, *y1* and C*oefficient1* are then plotted to the screen 

*Cell 2* - creates dataset 2 for flights from  Knock Airport Shannon Airport.  The process followed is the same as that outlined in the previous section.

*Cell 3, 4 and 5* - combines the datasets, and creates a plot to demonstrate Simpon's Paradox.  The plot is created using Matplotlib.

