Good way of learning testing is to check the behavior and bondaries of the Function 

Fter Engaging in a conversation with and AI , 
I discovered  
normal behaviours, 

What happens right where the behavior changes, or when the input is unusual?

Answer : it affects the task score by either increase or d

boundaries,

edge cases , 

combinations,
Question
What happens when a task is URGENT + overdue + DONE + has a blocker tag + was recently updated?

selected first test based on a reason than simply picking one randomly 

Question 
If you had to write only one test first, which behavior would you test first, and why?

Answer
 I would Choose Priority because it provides the base score, and then due date, status, tags, and update time modify that score

Good edge cases are:
Situation	Edge case
Due date	Exactly today
Due date	Exactly 2 days
Due date	Exactly 3 days
Due date	Exactly 7 days
Due date	Exactly 8 days

Five test-cases
calculate_task_score()
        
test 1: URGENT priority
test 2: LOW priority
test 3: overdue task
test 4: DONE task
test 5: blocker tag

using pytest


def test_urgent_priority():
    task = Task(
        priority=TaskPriority.URGENT,
        due_date=None,
        status=TaskStatus.IN_PROGRESS,
        tags=[],
        updated_at=datetime.now() - timedelta(days=2)
    )

    score = calculate_task_score(task)

    assert score == 60


def test_low_priority():
    task = Task(
        priority=TaskPriority.LOW,
        due_date=None,
        status=TaskStatus.IN_PROGRESS,
        tags=[],
        updated_at=datetime.now() - timedelta(days=2)
    )

    score = calculate_task_score(task)

    assert score == 10


def test_overdue_task():
    task = Task(
        priority=TaskPriority.LOW,
        due_date=datetime.now() - timedelta(days=1),
        status=TaskStatus.IN_PROGRESS,
        tags=[],
        updated_at=datetime.now() - timedelta(days=2)
    )

    score = calculate_task_score(task)

    assert score == 45


def test_done_task():
    task = Task(
        priority=TaskPriority.URGENT,
        due_date=None,
        status=TaskStatus.DONE,
        tags=[],
        updated_at=datetime.now() - timedelta(days=2)
    )

    score = calculate_task_score(task)

    assert score == 10


def test_blocker_tag():
    task = Task(
        priority=TaskPriority.LOW,
        due_date=None,
        status=TaskStatus.IN_PROGRESS,
        tags=["blocker"],
        updated_at=datetime.now() - timedelta(days=2)
    )

    score = calculate_task_score(task)

    assert score == 18