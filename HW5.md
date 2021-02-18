Math 295: Homework 5
================
Be Sure to Put Your Name Here
Due Sunday, February 28, 2021 by 11:59 pm

  - [1. Joining Student Data Tables \[7
    points\]](#joining-student-data-tables-7-points)
  - [2. Airline Mergers? \[6 points\]](#airline-mergers-6-points)
  - [3. A Fruit Fight \[6 points\]](#a-fruit-fight-6-points)

# 1\. Joining Student Data Tables \[7 points\]

In the data folder of this repository, you will find five small
hypothetical student record tables:

  - “id\_list.csv”: contains names, IDs and birthdates of students

  - “study\_abroad.csv”: records of students’ study abroad participation

  - “admission.csv”: student records compliled by the admission office
    during the application process

  - “acad\_records.csv”: student academic records including major and
    GPA

  - “housing.csv”: student residence information for students living
    on-campus

The questions below ask you to carry out “joins” to create a new tibble
and/or answer a question. The joins you have to choose from include:

Mutating joins:  
\* `inner_join()`  
\* `left_join()`  
\* `right_join()`  
\* `full_join()`

Filtering joins:  
\* `semi_join()`  
\* `anti_join()`

Remember that you may have to specific the key to use and that it may be
necessary to use more than one variable as the key.

**a)** Use `read_csv()` to read these data files into datasets (tibbles)
called **id\_list**, **study\_abroad**, **admission**,
**acad\_records**, and **housing**.

**Answer:**

**b)** Use an appropriate join to add major and college GPA to the
**id\_list** table without changing the order of the rows.

**Answer:**

**c)** For each student in the id\_list table, create a table that also
contains the dorm they lived in. If they lived off campus, the dorm
variable should contain an NA value.

**Answer:**

**d)** Repeat the previous but instead create a table that only contains
students who lived in dorms. Your join should exclude off-campus
students.

**Answer:**

**e)** Carry out a single join that displays just the information in the
**id\_list** for two students: one whose application was accidentally
deleted (don’t worry, it’s on the backup\!) and the student whose name
was misspelled by admissions.

**Answer:**

**f)** Carry out a single join that prints a list of students who did
NOT participate in study abroad.

**Answer:**

**g)** Use appropriate joins and data transformation commands to create
a table that includes all columns in the study abroad table and
additionally their college GPAs, a total of just 4 columns.

**Answer:**

**h)** Use appropriate joins and transformation commands to create a
table that contains a list of all current students containing the
following information in this order: student id, first and last name,
major, college GPA, study abroad site (or NA for non-participants), and
a variable called `housing` that is “ON” if they lived in a campus dorm
and “OFF” otherwise. Do NOT include a column with the name of the dorm
in which they lived. Sort our table by student ID number in increasing
numerical order.

**Answer:**

# 2\. Airline Mergers? \[6 points\]

This question requires use of the datasets discussed in R4DS and
provided in the **nycflights13** package. Be sure to load the package
before trying the problems.

**a)** Is there a relationship between the age of a plane and its
average arrival delays? Use join, and data transformation commands to
prepare the data and then produce a plot using **ggplot2**. Comment on
your plot. (Hint: you’ll have to create a data set with average arrival
delays for each plane, and then merge in age information.)

**Answer:**

**b)** Two airlines seem to run most of the planes which can not be
found in the `planes` data set. Identify those two airlines by name, not
just by code. Here is one possible set of steps:

  - filter the **flights** data to contain only airplanes not found in
    the `planes` data set  
  - create a new variable containing just the last 2 characters in
    `tailnum`  
  - create a data set that contains a row for each different code (based
    on the last 2 digits) and a count of how many times each code
    appears  
  - join with the **airlines** data to identify the codes

**Answer:**

# 3\. A Fruit Fight \[6 points\]

The character vector called `fruit` in **stringr** contains a list of 80
(\!) fruit from around the world. Use regular expressions in
`str_subset()` to find the fruit that satisfy the following conditions.
You might wish to use `str_view()` while experimenting but then use
`str_subset()` to show your results. This will prevent printing the
entire list of 80 each time\! If you get stuck, you can certainly google
and use stack overflow for help. This exercise is intended to push you
to learn a little regexp so you can get a feel for what it can do.

**a)** Find all fruit that have names that begin with the letter `d`.

**Answer:**

**b)** Find all fruit that have names that contain `r`, `n` or `q`.

**Answer:**

**c)** Find all fruit that have names that contain `ia` or `io`.

**Answer:**

**d)** Find all fruit that have names that end with `n` but not `in`.

**Answer:**

**e)** Find all fruit that have names that contain `ur` first and `an`
later in the name.

**Answer:**

**f)** Find all fruit that have names that are exactly 6 letters long.

**Answer:**

**g)** Find all fruit that have names that start and end with the same
letter? (Hint: Test your regexp specification on “abracadabra” and
“leviosa” to make sure the regexp magic is really working but only
when it’s supposed to. Or you could test it on the character vector
corpus of `words` included in **stringr**).

**Answer:**

**h)** What is my favorite fruit? Questions a-f are intended to give you
a strong hint\!

**Answer:**
