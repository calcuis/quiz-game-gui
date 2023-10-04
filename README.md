## Quiz Game (with GUI)

**Update:** initial feedback will be given while you click "Next" with a WRONG answer.

This Python code uses the `tkinter` library to create a simple quiz application. Let's break down the code step by step:

**Importing necessary modules:**
```
from tkinter import *
from tkinter import messagebox
import json
```
Here, the code imports the `tkinter` module for creating the GUI, messagebox for displaying messages, and json for handling JSON data.

**Class Definition:**
```
class Quiz:
    def __init__(self):
        # Initialization code goes here
```
The Quiz class is defined to handle the quiz logic and GUI interactions.

**Constructor (__init__) for the Quiz class:**
```
def __init__(self):
    # Initialization code goes here
```
This initializes the quiz by setting up the question number, displaying the title, displaying the first question, creating `radio` buttons for options, and more.

**Displaying Results:**
```
def display_result(self):
    # Displaying the quiz result
```
Displays the quiz result in a `messagebox`, showing the number of correct and wrong answers, as well as the overall score.

**Checking the Answer:**
```
def check_ans(self, q_no):
    # Checking if the selected answer is correct
```
Checks if the selected answer is correct based on the question number.

**Handling Next Button:**
```
def next_btn(self):
    # Handling the 'Next' button click
```
Handles the behavior when the "Next" button is clicked, updating the question number, checking the answer, and proceeding to the next question or displaying the result if all questions are answered.

**Creating Buttons:**
```
def buttons(self):
    # Creating 'Next' and 'Quit' buttons
```
Creates "Next" and "Quit" buttons using the tkinter Button widget and specifies their behavior upon clicking.

**Displaying Options:**
```
def display_options(self):
    # Displaying the options for the current question
```
Displays the options for the current question as radio buttons.

**Displaying Question:**
```
def display_question(self):
    # Displaying the current question
```
Displays the current question.

**Displaying Title:**
```
def display_title(self):
    # Displaying the quiz title
```
Displays the title of the quiz.

**Creating Radio Buttons:**
```
def radio_buttons(self):
    # Creating radio buttons for options
```
Creates radio buttons for the answer options.

**Creating the GUI:**
```
gui = Tk()
gui.geometry("800x450")
gui.title("Quiz")
```
Creates a `tkinter Tk` instance and sets the geometry and title for the GUI.

**Loading Quiz Data from JSON:**
```
with open('data.json') as f:
    data = json.load(f)
```
Reads quiz data (questions, options, and answers) from a JSON file named 'data.json'.

**Initializing the Quiz and Running the GUI:**
```
question = (data['question'])
options = (data['options'])
answer = (data['answer'])
quiz = Quiz()
gui.mainloop()
```
Initializes the quiz with the loaded data and runs the GUI loop.

Overall, this code sets up a quiz application using `tkinter` with multiple-choice questions, options, and the ability to track and display the user's quiz score. The quiz data is loaded from a JSON file, and the application guides the user through the quiz, allowing them to answer questions and view the results.
