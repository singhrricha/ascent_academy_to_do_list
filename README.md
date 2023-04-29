# ascent_academy_to_do_list
Initialization and Variable Declarations
At the beginning of the code, several variables are declared and initialized. todoList, comdoList, and remList are arrays that will hold the to-do list items, completed items, and remaining items, respectively. addButton, todoInput, deleteAllButton, allTodos, and deleteSButton are references to various HTML elements that will be used later in the code.

Event Listeners
The code sets up several event listeners to handle user input. addButton, deleteAllButton, and deleteSButton all have click event listeners that will call the add(), deleteAll(), and deleteS() functions, respectively. document has a click event listener that will check which element was clicked and call the appropriate function based on the class or id of the element.

Updating Lists and Counts
The update() function updates the comdoList and remList arrays based on the complete property of each item in todoList. It also updates the text content of the "Remaining" and "Completed" count elements based on the length of remList and comdoList.

Adding Tasks
The add() function takes the input value from todoInput and creates a new object with properties for the task, id (generated using Date.now()), and completion status. If the input value is empty, an alert is displayed and the function returns. Otherwise, the new object is added to todoList, the input field is cleared, and the update() and addinmain() functions are called.

Rendering the Main List
The addinmain() function creates a string of HTML elements for each item in the todoList array, including a unique id, the task text, and two buttons for completing and deleting the task. The string is added to the innerHTML of the allTodos element, which displays the list on the web page.

Deleting Tasks
The deleteTodo() function removes the task object from todoList based on its id. It then calls update() and addinmain() to update the remaining lists and render the new main list.

Completing Tasks
The completeTodo() function toggles the complete property of the task object based on its id. If the task is marked as complete, the line class is added to the task text element to strike through the text. If the task is marked as incomplete, the line class is removed. The function then calls update() and addinmain() to update the remaining lists and render the new main list.

Deleting All and Selected Tasks
The deleteAll() and deleteS() functions remove all completed tasks or selected tasks, respectively, from todoList. They then call update() and addinmain() to update the remaining lists and render the new main list.

Filtering the Main List
The viewAll(), viewCompleted(), and viewRemaining() functions call addinmain() with todoList, comdoList, and remList, respectively, to display the appropriate list on the web page.
