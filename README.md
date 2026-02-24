📝 To-Do List with CRUD Operations

This project is a simple To-Do List application built using JavaScript. It implements full CRUD (Create, Read, Update, Delete) functionality and uses Local Storage to persist data.

🚀 Features & Implementation

1. Create and Delete Tasks

Users can add new tasks to the list.

Each task includes a delete button to remove it from the list.

2. Save Data to Local Storage

Before saving to Local Storage, the task data is converted into an array.

Once stored as an array (or array of objects), it can be saved using localStorage.

This ensures tasks remain available even after refreshing the page.

3. Edit Task Using Index

When editing a task, the application uses the index of the selected item.

The index helps identify which specific task should be updated inside the array.

4. Mark Task as Done (Using Objects)

Instead of storing tasks as plain strings, each task is stored as an object.

Each object contains:

The task text

A completed (boolean) property

A function checks whether the task is completed or not and updates the UI accordingly.

Example structure:

{
text: "Study JavaScript",
completed: false
}

5. Checkmark Icon for Completed Tasks

When a task is marked as completed:

An <img> element is created using createElement().

The checkmark image is appended to the task using appendChild().

The image appears only when the task is marked as done.

6. Real-Time Task Counter

A <span> element is used to display the total number of tasks.

The total count is calculated using:

todos.length

Since tasks are stored in an array of objects, length correctly reflects the number of tasks.

The counter updates dynamically whenever a task is added or removed.

7. Implement whole box checked for task done

Using with the same logic for the circle button i created an onlick with parent div box so even the box is click for task its automatic implement task done with check mark icon.

🐞 Issues Encountered & Fixes
✅ 1. Local Storage Not Saving Immediately

Issue:
When adding a task, it was not immediately saved to Local Storage. It only saved after editing a task.

Fix:
Ensured that the save-to-localStorage function is called every time a task is added.

✅ 2. Strikethrough Style for Completed Tasks

Improvement:
Added a click event that applies a line-through style to visually indicate that a task is completed.

✅ 3. Edit Modal Implementation

Improvement:
Implemented a modal for editing tasks instead of editing inline, making the UI cleaner and more user-friendly.

✅ 4. Real-Time Task Count

Improvement:
The total task count now updates automatically whenever tasks are added or deleted.

✅ 5. Improved Edit Modal Design

Improvement:
Enhanced the modal design to make it more visually appealing instead of plain styling.

✅ 6. Text is not wrap to balance

Issue:
When adding an task and using long description its too long its expand outside the box width set

Fix:
In text for task i add an text-wrap: balance; when text is too long its adjust based on box width

📚 Concepts Practiced

DOM Manipulation

Event Handling

Array Methods

Objects in JavaScript

Local Storage

Dynamic UI Updates

Modal Implementation

CRUD Operations
