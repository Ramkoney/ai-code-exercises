Step 1: Choose Algorithm 1
Task Priority Sorting Algorithm
Its purposes are as follow:

The module provides a scoring algorithm to automatically determine which tasks should be done first based on multiple factors.
It gives every task a score and then puts the highest-scoring tasks first.

Step 2: Understand the algorithm
Task
 ↓
Calculate score
 ↓
Priority points
+ Due date points
+ Important tag points
+ Recent update points
- Completed/review points
 ↓
Final score
 ↓
Sort highest → lowest
 ↓
Top 5 tasks

Task A = 93  ← first
Task B = 20  ← second

 Learning points

The algorithm does not simply sort tasks by priority.
It calculates a score using several factors.
Urgent and overdue tasks receive higher scores.
Completed tasks receive a large penalty.
Tags such as urgent, critical, and blocker increase the score.
After calculating the scores, tasks are sorted from highest to lowest.
The get_top_priority_tasks() function returns only the first 5 tasks by default.
What are the reflection questions asking?

You don't need complicated answers.

1. How did AI's explanation change my understanding?

Before using AI, I found the scoring system confusing because there were many conditions.
 The AI helped me understand that the algorithm simply calculates points for different 
 task properties and then sorts the tasks using the final score.

2. What was still difficult?

The most difficult part was understanding how the different points affect the final score, 
especially the date calculations and negative scores for completed tasks.

3. How would you explain it to another junior developer?

I would explain it as a points system. Each task gets points based on priority, due date, status, tags, and recent updates.
 The tasks with the highest total scores are considered the most important.

4. Did you test your understanding against AI?

Yes. I asked AI to explain the algorithm and then used an example task to calculate the score myself.
 This helped me confirm that I understood how the scoring worked.

5. How could you improve the algorithm?

I would make the scoring values configurable instead of hard-coded. 
I would also add more tests for different combinations of priority, due dates, and statuses.