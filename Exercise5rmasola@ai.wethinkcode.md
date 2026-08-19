Task Manager

A Python command-line application for creating, managing, prioritising, and completing tasks. 
Tasks can be stored and retrieved from a JSON file.

 Features
 Create new tasks
 Set task descriptions and priorities
 Add due dates and tags
 Update task status
 Mark tasks as completed
 Save and load tasks using JSON storage
 View and manage existing tasks

 Technologies Used

 Python
 JSON
 Python standard library

 Installation

Requirements

 Python 3.14
 Git

Clone the project repository and navigate to the project directory:
<bash>
git clone <https://github.com/Ramkoney/ai-code-exercises/>
cd <rmasola51@aiwethinkcode>

No additional packages are required  project only uses Python's standard library.
Operations may include creating a task, viewing tasks, updating a task, and marking a task as completed.

For example:
python cli.py status <task-id> done

The application uses a JSON file for task storage.
The storage file can be configured when creating the TaskManager:

python
manager = TaskManager("tasks.json")

The default storage file is:
text
tasks.json

 Project Structure
text
TaskManager/
├── cli.py
├── models.py
├── task_manager.py
├── storage.py
└── tasks.json


 Main Components

cli.py — Handles interaction with the user and command-line arguments.
models.py — Defines the Task model and task-related enums such as 
TaskStatus and TaskPriority.
task_manager.py — Contains the main business logic for managing tasks.
storage.py — Handles saving and loading tasks.
tasks.json — Stores task information persistently.

Troubleshooting

 Python command is not recognised

Make sure Python 3 is installed and added to your system PATH.

Invalid date format

Dates should use the following format:

text
YYYY-MM-DD
For example:
text
2026-08-20

 Task data is not being saved

Check that the application has permission to create or modify the 
tasks.json file and that the storage path is correct.

Contributing

1. Create a new branch for your changes.
2. Make your changes.
3. Test the application.
4. Commit your changes with a clear message.
5. Create a pull request for review.

 License

This project is provided for educational purposes.
 Refer to the project's repository or course materials for the applicable license information.


# How to Create a Task in the Task Manager

## Prerequisites

Before creating a task:

1. Make sure Python is installed.
2. Make sure you are in the Task Manager project directory.
3. Make sure the application can access its task storage file.

## Steps

### Step 1: Open the Task Manager

Open a terminal and navigate to the Task Manager project directory.

```bash
cd TaskManager
```

### Step 2: Run the application

Start the application using the appropriate Python command.

```bash
python cli.py
```

### Step 3: Create a task

Use the application's task creation command and provide the task information, such as the title, description, priority, due date, and tags.

For example:

text
Create a task called "Finish project report"


### Step 4: Check the task

View the task list to confirm that the new task was created successfully.

The task should contain the information you provided and should be stored in the application's task storage.

## Common Mistakes

* Using an incorrect command.
* Entering a date in the wrong format.
* Forgetting required task information.
* Running the command from the wrong directory.
* Not having permission to access the task storage file.

Troubleshooting
The application does not start

Check that Python is installed and that you are running the command from the correct project directory.

 The date is rejected

Use the required date format:

text
YYYY-MM-DD

For example:
text
2026-08-20
The task does not appear
Check that the task was saved successfully and that the application has access to its storage file.

 Summary

Creating a task involves starting the Task Manager, entering the task information, 
and checking that the task was successfully saved.

Task Manager FAQ

 About the Project

The Task Manager is a Python application that allows users to create, manage, prioritise, update, and complete tasks.

Target audience:
 Beginners and general users of the Task Manager application.

Areas of focus:
 Creating tasks, setting priorities, managing task status, due dates, storage, and troubleshooting.

 Getting Started

 What is the Task Manager?

The Task Manager is an application for organising and managing tasks.

 How do I start the application?

Run the application's main command from the project directory. For example:

bash
python cli.py

Check the project's README for the exact command used by your version.
 Where are my tasks stored?

Tasks are stored using the application's storage system. In the Python version, tasks are stored in a JSON file such as `tasks.json`.

 Features and Functionality

 How do I create a task?

Use the task creation functionality and provide the required task information, such as the title, description, priority, due date, and tags.

### How do I set a task's priority?

A task can be assigned a priority such as LOW, MEDIUM, HIGH, or URGENT.

 How do I mark a task as completed?

The task's status can be changed to `DONE`. The application also records the completion time.

 Can I add a due date?

Yes. A task can have a due date. When entering a date, use the format required by the application, such as:

text
YYYY-MM-DD

Can I add tags to a task?

Yes. Tags can be associated with tasks to help organise or identify them.

 Troubleshooting

 Why can't I start the application?

Make sure Python is installed and that you are running the application from the correct project directory.

 Why is my date rejected?

Check that the date follows the required format:

text
YYYY-MM-DD
For example:
text
2026-08-20

 Why didn't my task save?

Check that the application has permission to access its storage file and that the storage location is correct.

 What happens if I enter an invalid priority?

The application expects a valid priority value. An invalid value may cause an error, so use one of the supported priority levels.

Task Management

 What happens when I complete a task?

The task status changes to `DONE`. The application records when it was completed and updates the task's modification time.

 Will my tasks still be there after restarting the application?

Yes, provided the task was successfully saved to the application's storage.

Summary

The Task Manager is designed to make it easier to create, organise, prioritise, and complete tasks. If a problem occurs, first check the command being used, the input format, and the application's storage file.


