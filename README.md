EXAM GRADER PROGRAM

* Overview

This project is a Python program designed to automate the grading of exam results based on input files containing students' answers. The program performs several tasks, including validating data, grading exams, calculating statistics, and exporting results.

The program is implemented in Python 3.9 and is intended to run in a Jupyter Notebook environment provided by Anaconda Navigator.

* Requirements

Python Version: 3.9

Libraries Used: os, numpy, pandas

Environment: Jupyter Notebook in Anaconda Navigator

Data Source: Class Files (1-8).txt

* Features

1. File Handling

- Allows the user to input the name of a file containing exam data.

- Validates whether the file exists.

- If the file does not exist, prompts the user until a valid file is provided.

2. Data Validation

- Reads and processes data from the input file.

- Ensures that each line of data contains exactly 26 values.

- Validates student IDs to match the format N######## (an "N" followed by 8 digits).

- Reports invalid lines with appropriate error messages.

3. Grading Exams

- Grades each student based on a predefined answer key.

- Scoring Rules:

+ (+4) points for each correct answer.

+ (0) points for skipped answers.

+ (-1) point for incorrect answers.

- Tracks skipped and incorrect responses for each question.

4. Statistics Calculation

- Computes class statistics:

+ Total number of high scores (>80).

+ Mean (average) score.

+ Highest and lowest scores.

+ Range of scores.

+ Median score.

+ Identifies questions most frequently skipped or answered incorrectly, with corresponding statistics.

5. Result Export

+ Writes a detailed results file containing each student's ID and score.

+ Names the output file based on the input file (e.g., class1_grades.txt for class1.txt).

6. Usage Instructions

Step 1: Setup

1. Ensure that the required Python version, data files and libraries are installed.

2. Place the Python script lastname_firstname_grade_the_exams.py in the same directory as the input data files.

3. Input files must be in .txt format and follow the structure described in the Data Format section below.

Step 2: Running the Program

1. Launch the Anaconda Navigator and open a Jupyter Notebook.

2. Install the data folder.   

3. Run the Python script by executing the cells in the notebook.

4. Follow the on-screen prompts:

5. Enter the file name (without .txt).

6. The program will validate the file, process data, and generate a report.

Step 3: Output

1. The program will display the analysis and statistics on the console.

2. Results will be saved in a new file named <input_filename>_grades.txt.

You can check your output format with the Expect Output folder for better accuracy.

Notes

Ensure all input files strictly follow the expected format.

Handle invalid input files gracefully to avoid crashes.

Adjust scoring rules or analysis parameters as needed by modifying the grade_exams function.

