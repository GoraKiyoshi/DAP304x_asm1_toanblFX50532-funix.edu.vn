#README: Exam Grader Program

Overview

This project is a Python program designed to automate the grading of exam results based on input files containing students' answers. The program performs several tasks, including validating data, grading exams, calculating statistics, and exporting results.

The program is implemented in Python 3.9 and is intended to run in a Jupyter Notebook environment provided by Anaconda Navigator.

Requirements

Python Version: 3.9

Libraries Used:

os

numpy

pandas

Environment: Jupyter Notebook in Anaconda Navigator

Features

File Handling

Allows the user to input the name of a file containing exam data.

Validates whether the file exists.

If the file does not exist, prompts the user until a valid file is provided.

Data Validation

Reads and processes data from the input file.

Ensures that each line of data contains exactly 26 values.

Validates student IDs to match the format N######## (an "N" followed by 8 digits).

Reports invalid lines with appropriate error messages.

Grading Exams

Grades each student based on a predefined answer key.

Scoring Rules:

+4 points for each correct answer.

0 points for skipped answers.

-1 point for incorrect answers.

Tracks skipped and incorrect responses for each question.

Statistics Calculation

Computes class statistics:

Total number of high scores (>80).

Mean (average) score.

Highest and lowest scores.

Range of scores.

Median score.

Identifies questions most frequently skipped or answered incorrectly, with corresponding statistics.

Result Export

Writes a detailed results file containing each student's ID and score.

Names the output file based on the input file (e.g., class1_grades.txt for class1.txt).

Usage Instructions

Step 1: Setup

Ensure that the required Python version and libraries are installed.

Place the Python script lastname_firstname_grade_the_exams.py in the same directory as the input data files.

Input files must be in .txt format and follow the structure described in the Data Format section below.

Step 2: Running the Program

Launch the Anaconda Navigator and open a Jupyter Notebook.

Run the Python script by executing the cells in the notebook.

Follow the on-screen prompts:

Enter the file name (without .txt).

The program will validate the file, process data, and generate a report.

Step 3: Output

The program will display the analysis and statistics on the console.

Results will be saved in a new file named <input_filename>_grades.txt.

Data Format

Input File Format

Each input file should contain lines structured as follows:

The first value is the student ID (e.g., N12345678).

The next 25 values are answers to the exam questions (e.g., B,A,D,D,C,B,D,A,C,C,...).

Answers can be empty to indicate skipped questions.

Example Input:

N12345678,B,A,D,D,C,B,D,A,C,C,D,B,A,B,A,C,B,D,A,C,A,A,B,D,D
N87654321,B,,D,,C,B,,A,C,C,,B,A,B,A,,,,A,C,A,A,B,D,

Output File Format

Each line of the output file contains the student ID and their calculated score, separated by a comma.

Example Output:

N12345678,75
N87654321,68

Example Run

Input

File: class1.txt

N00000001,B,A,D,D,C,B,D,A,C,C,D,B,A,B,A,C,B,D,A,C,A,A,B,D,D
N00000002,B,A,,D,C,B,D,A,C,C,D,B,A,B,A,C,B,D,A,C,A,A,B,D,
N00000003,B,A,D,D,C,B,D,A,C,D,B,A,B,A,C,B,D,A,C,A,A,B,D,D,A,B,C,D,E

Output (Console)

Enter a class file to grade (i.e. class1 for class1.txt): class1
Successfully opened class1.txt
**** ANALYZING ****
Invalid line of data: does not contain exactly 26 values:
N00000003,B,A,D,D,C,B,D,A,C,D,B,A,B,A,C,B,D,A,C,A,A,B,D,D,A,B,C,D,E
**** REPORT ****
Total valid lines of data: 2
Total invalid lines of data: 1

Total student of high scores: 1
Mean (average) score: 71.5
Highest score: 75
Lowest score: 68
Range of scores: 7
Median score: 71.5

Question that most people skip: 3 - 1 - 0.5
Question that most people answer incorrectly: 10 - 1 - 0.5

Output File

File: class1_grades.txt

N00000001,75
N00000002,68

Notes

Ensure all input files strictly follow the expected format.

Handle invalid input files gracefully to avoid crashes.

Adjust scoring rules or analysis parameters as needed by modifying the grade_exams function.

