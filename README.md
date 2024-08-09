# Javascript-TODO-list
TODO list using java script
![Screenshot 2024-08-09 154231](https://github.com/user-attachments/assets/a86b2b65-1743-4d36-91ce-6d4e0cb88c9f)

# Simple To-Do List App 📝

This is a basic To-Do List application built using JavaScript. It allows you to manage your tasks by adding, listing, and deleting them directly from the console.

## Features

- **Add Tasks**: Add new tasks to your to-do list.
- **List Tasks**: Display all the tasks in your to-do list.
- **Delete Tasks**: Remove tasks from your to-do list by specifying the index.

## How It Works

1. The app starts by prompting the user to enter a request.
2. The user can choose to `add` a task, `list` all tasks, or `delete` a task by specifying its index.
3. If the user enters `quit`, the app will exit the loop and end the session.

## Usage

1. **Add a Task**: Type `add` when prompted, then enter the task you want to add.
2. **List Tasks**: Type `list` to display all current tasks.
3. **Delete a Task**: Type `delete` and then enter the index of the task you want to remove.
4. **Quit**: Type `quit` to exit the app.

## Example

```javascript
let todo = [];
let req = prompt("please enter your request");

while(true){
    if(req == "quit"){
        console.log("quitting the app");
        break;
    }
    
    if(req == "list"){
        console.log("------------");
        for(let i=0; i<todo.length; i++){
            console.log(i, todo[i]);
        }
        console.log("------------");
    } else if(req == "add"){
        let task = prompt("please enter the task you want to add");
        todo.push(task);
        console.log("task added");
    } else if(req == "delete"){
        let idx = prompt("enter the task you want to delete");
        todo.splice(idx, 1);
        console.log("task deleted");
    } else {
        console.log("bad request!!");
    }
    req = prompt("please enter your request");
}
