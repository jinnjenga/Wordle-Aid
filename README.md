# Wordle-Aid
individual class project

# CS151 PROGRAMMING ASSIGNMENT #5

* 60  POINTS (10pts design, 50pts final)                                  			
* DESIGN DUE: 4/5/23
* FINAL DUE: 4/12/23

## PROBLEM:

The game Wordle is currently very popular. The purpose of this game is to guess a 5 letter English word within 6 tries, getting hints each time by being told which letters you guessed are in the correct location, which letters are not in the word, and which letters are in the word but in the wrong place. If you are unfamiliar with Wordle, you should probably try playing it to get a feel for it before continuing to read this assignment. [Play the Daily Wordle Here](https://www.nytimes.com/games/wordle/index.html).

The purpose of this assignment is NOT to create the game Wordle. Instead, you will be creating a program to aid players in guessing their words. Your program will have four different analyses it can do on the words provided in a file of all five letter English words.

## PURPOSE OF THE ASSIGNMENT

The purpose of this assignment is to give you practice with

1. Input & output
2. Decision making
3. Looping
4. Function design and implementation
5. Error checking
6. Lists
7. Reading from files
8. Writing to files

## REQUIREMENTS ANALYSIS 

The first stage in your programming assignment is the requirements analysis stage.  You need to make sure you understand the below requirements for what needs to be included in your program.

Your program must read in and store all 5 letter words in a list. Then give the user the following options to choose from:

1. Save to a file all words that have a user chosen letter in the word
2. Save to a file all words that have a user chosen letter in a user specified position in the word 
3. Save to a file all words that have a user specified number of vowels in it
4. Another option of your own design

These tasks can all help a user figure out what word to guess while playing Wordle, without completely solving the game for them.

The game should allow the user to choose another option after a task is completed or choose to quit the program. They can keep choosing tasks until they choose to quit.

### Files

You have an input file provided to you in your repository that contains a list of all 5 letter English words. You can open the file in PyCharm to understand its format.

Each task for your program to complete requires writing data to a file. You should never write to the same file that was your input file, as you will overwrite it. Allow the user to choose the name of the file to output to. You can see in PyCharm if it worked, as the file should appear in your files list and you should be able to open it to see the contents. See the demonstration in class as a reminder; you can re-watch the class discussion on Panopto.

You should use all error checking that we've learned about for interacting with files.

### All Words that Have a User Chosen Letter in the Word

This task is the most straightforward of your tasks. The user will provide a single letter to you. You will then find and output every word that has that letter anywhere in the word.

### All Words that Have a User Chosen Letter in a Specified Location

This task builds on the first task, but instead of the letter appearing anywhere in the word, you need to output every word that has the letter in a very specific location. The user provides a single letter, and what location in the word it appears in. Make sure you give clear instructions to the user on how to denote the letter location (is the first letter 0? 1? something else? They won't know what your program expects unless you tell them).

### All Words that Have a User Specified Number of Vowels

Supposedly, a good way to play Wordle is to use a word with lots of vowels as your first guess. For this task you will let the user choose how many vowels they want in their word, and then output all words that have that number of vowels. This task is the hardest of the required tasks, so think about it after you've reasoned through the others. Recall that vowels in English are the letters a, e, i, o, and u.

### Another Option of Your Own Design

There are many other ways you could choose words from the list other than the 3 above. Design your own task for this part of the assignment. You could build on any of the above tasks to make them more complicated, or do something unrelated. Here is a chance to put a unique spin on your program.

Your professor will let you know if your task is an OK choice during the design grading. Be sure to look at your design grade document to see any feedback they give you on your choice.

### User Choices

The user gets to choose the following in your program:

* The name of the input file
* Which option from the 4 tasks the program should complete
* The name of the output file to save the results
* Which task they want to do, including the option to quit the program

Your program should follow rule 7 for those 4 inputs: All input is considered evil until proven otherwise. i.e., you need to have some error checking.

The user will also give input on the information needed for individual tasks, such as the letter or location. That input should only be asked for when that task has been chosen. You do not need to error check the letter inputs, but you should ensure your program does not crash if the user gives an invalid location for Task 2. 

### Iterative development

The best way to design a program is to use iterative development. This means get it working in pieces. For instance, get your program to read the data into a list. Only once that works, figure out how to solve one task. First htink about how to solve that task without writing output to a file, then figure out how to add that part in. Then do the same process for the next task.

### General design requirements

Recall that user input should generally happen in main, then passed as a parameter to the function that will do the work.

## DESIGN

The second stage is to design your solution based on the requirements:

1. Determine the tasks being accomplished in your program. Each of these should be a function. If you find yourself writing the same steps in many places, that is usually a good sign that those steps should be in their own function. A group of steps that are highly related to each other also should be a function. Error checking loops should always be in a function that is called any time that type of error checking is needed.
2. Write an algorithm for each function. This algorithm includes parameters, calculations, and returned values. No code other than import statements and the call to main should exist outside of a function.
3. Make the main part of your program be in a “main” function. The main function never takes parameters, and does not return anything. The main function will call most of your other functions.
4. Double check that you included all of the requirements.


### DESIGN SUBMISSION: 

Submit to GitHub in PA5 repository: the algorithm for your program in designInitial.txt. Remember to note the name, parameters, return value, and algorithm for every function.

*Remember to double check on github.com that your file pushed. If it didn't, you need to push it. Your instructor can only see what is on github.com, not what is only on your computer.*

Your algorithm should follow the requirements of an algorithm, contain all of the requirements, and include your entire program. Everything should be planned out. **There should not be any code.**

## PROGRAMMING STEPS

After your design is complete and correct, it's time to start programming and then testing:

* Fix design issues: If there were issues with your design, either not meeting requirements or in the format, fix that before you start writing your code.
* Implementation: Write your program following the requirements and based on your design.
  * Follow good usability/HCI principles in your input and output (make it clear the type of input you are asking for)
  * Follow good use of functions
  * Remember to state the purpose of the program
  * Remember to have a main function, and to call it.
* Testing: Make sure it works correctly; give it sample input, and check that the output is correct. You should be testing as your work, following iterative development. Only work on coding a new part of the game after you got a simpler part working.

### Programming Tips

For many of your tasks you need to figure out if something exists in a word. Remember that a word is just a string. We learned many different ways to check if a value was in a string, as well as how to determine what was at a particular location of a string. Refer back to your notes or the book if you don't remember how to do something.

You will need loops, and in some cases a for loop may be the easiest way to design it. 

If you follow iterative programming, testing as you go, it will be easier to find bugs in your program and fix them than if you try to program up everything at once.

### Testing Tips

For testing, you could create a smaller version of the input file that has fewer words so that you can tell if it gives the correct answer. For instance, if there are only 10 words in the file, if you ask for all the words with 3 vowels, you can easily see if it found the correct words. 



## ASSIGNMENT REMINDERS

Follow the programming assignment requirements document for comments, formatting, etc. This includes intro comments, function header comments, and comments within each function. Remember to add the new "Input Files" line to your intro comments like we did starting in Lab 8.

## REFLECTION

Write a short reflection about the programming assignment in reflection.txt: what did you learn, what would you do differently next time, what was difficult? What was it like to work with files? Did this project resonate more or less than other project?  This should be no more than a page.

## FINAL SUBMISSION

1. To GitHub:  
    1. Your .py file   
    3. Your final algorithm, including the changes you made based on the design feedback, in designFinal.txt
    3. Your reflection of the programming assignment in reflection.txt.

***Remember to double check on github.com that your files pushed. If they didn’t, you need to push them. Your instructor can only see what is on github.com, not what is only on your computer.***
