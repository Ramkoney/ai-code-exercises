Exercise Part 1: Understanding Project Structure
1. My initial understanding

I first looked at the project structure and README.md without reading the code in detail. I identified the main files and folders and tried to guess what each one was responsible for.

I found that the project is a Task Manager application. The files appear to be separated according to their responsibilities, such as handling tasks, managing task operations, and storing data.

2. Technologies

From the files in the project, I identified the programming language and supporting technologies by looking at the configuration files.

For example:

requirements.txt → Python dependencies
package.json → JavaScript/Node.js dependencies
pom.xml → Java/Maven dependencies

I would confirm which one is actually used by checking the starter project's files and README.

3. Main components

My initial understanding was:

User-> CLI -> Task Manager -> Task Model-> Storage
 
I think the main components are responsible for:

CLI: receives commands from the user.
Task Manager: contains the main task-management logic.
Task model: represents information about a task.
Storage: saves and retrieves task information.
4. Using the AI prompt

I gave my initial understanding and questions to the AI using the "Understanding Project Structure and Technology Stack" prompt.

The AI helped me understand how the different files are connected and what responsibilities they have.

5. What I learned

One misconception I had was that all the task functionality would probably be inside one file.
 I learned that the application separates responsibilities between different components.

An important entry point is the CLI, because this is where user commands enter the application.
 The Task Manager then handles the business logic, while the storage component handles persistence.

 I explored the Task Manager project without going deeply into the code. 
I looked at the README, project folders, and configuration files to understand the technology 
and structure. I identified the CLI, task management logic, task models, and storage as the main 
components. I then used the AI prompt to check my assumptions. The main thing I learned was that the application separates different responsibilities instead of putting everything into one file.