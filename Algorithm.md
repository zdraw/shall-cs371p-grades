This wiki describes the classes and algorithms used to create statistics on a set of grades.

# Introduction #

This program takes in the
> o Number of grades in a class
> o Points possible for each grade
> o Weights of each grade (adds up to 100)
> o Student's ID, unique course number, grader, and then the scores for each grade

The program calculates statistics on the data including
> o Number of students
> o Scores: Max, Mean, Min, Standard Deviation
> o Number of As, Bs, Cs, Ds, and Fs as well as the percentage of each of the number of students
> o Average GPA of the class

The students' data are then printed out including the ID, unique course number, grader, scores which were read in. The student calculates the
> o Total score based on their grades
> o z-Score
> o GPA as a letter

# Details #

To achieve this goal I created two classes, a Course class and Student class.

The Course class retains the number of grades, points possible for each grade, and weights for each grade. Once the vector of Students has been created, the Course class is used to compute the rest of the variables related to the whole class like the max, mean, min, standard deviation, and average GPA.

The Student class holds a vector of the grades, the indexes of which line up with the points possible and weights indexes. Given a Course object, the Student object can update it's score and GPA. The Student object can also calculate it's z-score if give the mean and standard deviation for a Course.

The main body of the program is in grades\_solve. The function contains a loop for receiving input, evaluating based on the input, and then ouputing the results.

There are 5 main functions that are used throughout the program
> o grades\_read
> o grades\_eval
> o grades\_print
> o mycomp
> o myround

The grades\_read function takes in a stream of input to populate the vector of Students and vectors in the Course class.

The grades\_eval function uses variables from both the Course and Student to populate the rest of the Course object.

The grades\_print function formats the output to a visually pleasing format and prints out everything that was calculated.

To help make the output look nice, I created a round function to round scores before outputing them. It was also helpful when I needed to sort the vector of students based on the score and then the ID.