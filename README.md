# Shell Fundamentals - Todo List Script

---

## Running `todo.sh`

When we run the script using:

```bash
$ ./todo.sh
```

**Screenshot 1: Script Startup and Invalid Option Handling** <br>
![image](https://github.com/user-attachments/assets/11e97498-8e1a-4e8b-b622-97ceedeadd02)

**Description:**
When the script launches, it greets the user and displays a menu with 4 options:

1. View all tasks
2. Add a new task
3. Delete a task
4. Exit the program

The script includes **input validation** to ensure users can only enter numbers between 1 and 4. For instance:

* Entering `77` or `abc` prompts an error message and re-asks for a valid option.

Additionally, behind the scenes, the script checks if the `~/todo.txt` file exists:

* If it doesn't, the script automatically creates it.
* This ensures that tasks are always saved properly, and the file system is ready for use.

---

## Option 1: View All Tasks

After selecting Option `1` from the main menu:

**Screenshot 2: Viewing an Empty Task List** <br>
![image](https://github.com/user-attachments/assets/dcc1d4f9-ab48-4d0f-9a02-eadccb097c12)

**Description:**
When the todo list file (`~/todo.txt`) is empty, the script clearly informs the user that there are no tasks saved yet.

**Screenshot 3: Viewing Tasks When Populated**
<br>
![image](https://github.com/user-attachments/assets/fda55400-4c30-4d5e-b525-177ac25f693a)

**Description:**
Once tasks have been added, selecting Option 1 displays all tasks with numbered lines. This numbering is essential for deleting specific tasks using Option 3.

This option helps users review their todo items and confirms the script is correctly reading from `~/todo.txt`.

---

## Option 2: Add a New Task

**Screenshot 4: Adding a new task** <br>
![image](https://github.com/user-attachments/assets/cc882d7a-0eef-4c84-abfc-be6647ad42dd)

**Description:**
When the user selects Option 2, the script prompts:

> Enter todo:<br>
> Todo can be empty string

This message indicates that the input is optional, though users are encouraged to provide meaningful content.

In the example shown, the user entered:

> I will complete my kodecamp assignment today

The task is appended to the existing list in `~/todo.txt`. Immediately after, the updated list is displayed with all tasks, including the newly added one at the end.

This feature allows users to add tasks efficiently while confirming their addition in real time.

---

## Option 3: Delete a Task

**Screenshot 5: Deleting a Task with Invalid and Valid Input** <br>
![image](https://github.com/user-attachments/assets/8775cf6f-a881-47ed-82d7-e4f9eb022ac8)

**Description:**
When the user selects Option 3, the script first displays all tasks with their line numbers.

The user is then prompted:

> **Enter the todo index:**

If the input is:

* A number **outside the range** (like `6` when only 5 tasks exist), or
* A **non-numeric value** (like `qwe`),

The script responds with:

> **Oops! Invalid index**

This ensures invalid deletions are caught and the user is safely returned to the menu without breaking the program.

Finally, when the user enters a valid index (e.g., `4`), the script successfully deletes that task and immediately displays the updated todo list, now without the removed item.

This shows that the script includes strong input validation and reflects task changes in real time.

---

## Option 4: Exit the Program

**Screenshot 6: Exiting the application** <br>
![image](https://github.com/user-attachments/assets/4c44e6ee-0a23-4ecf-887e-ab0c7cc62e8c)

**Description:**
When the user selects Option 4, the script confirms their choice with the message:

> << You want to exit the program >>

It then exits gracefully with a farewell message:

> Bye samson.olaide!

This ensures a clean and user-friendly exit from the application.

